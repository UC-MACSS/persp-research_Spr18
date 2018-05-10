# Problem Set #3

## Part 1: Image classification (5 points)

1. Set your random seed to `1234`
    * R
        ```r
        set.seed(1234)
        ```
    * Python
        ```python
        import random
        random.seed(1234)
        ```
1. Load the MNIST dataset
    * Preprocess the data by converting the data to a 2D tensor with individual values between 0 and 1
    * Randomly split the training data into 50,000 training observations and 10,000 validation observations
1. Implement a series of neural network models
    1. Initial test
        * 5 dense, fully-connected layers
        * `relu` activation except for the last layer (use `softmax`)
        * Initialize with 512 hidden units apiece (except for the last layer)
        * Use `rmsprop` optimizer
        * Use categorical crossentropy for loss function
        * Track validation set accuracy during training process
        * Train with `batch_size = 512` and 200 epochs
        * Plot the validation set accuracy and loss over the epochs
        * Identify the epoch where the model's performance degrades based on the validation set
    1. Implement dropout
        * Implement layer dropout after each layer from model 1 (except the last)
        * Use a dropout rate of `0.5`
        * Estimate the model, and graphically compare the validation loss across epochs to the initial model. How does this new model perform relative to the old model?
    1. Weight regularization
        * Reestimate the initial model with L1 weight regularization on each layer (except the final layer) with a `0.001` penalty for each weight coefficient
        * Reestimate the initial model with L2 weight regularization on each layer (except the final layer) with a `0.001` penalty for each weight coefficient
        * Plot the validation loss for the initial model vs. the dropout vs. the L1 regularized model vs. the L2 regularized model - which model appears to perform the best?
    1. Final model
        * Select the best model from the ones you have estimated so far - this should have the lowest validation loss score at any potential epoch
        * Reestimate that model using all of the training data (no validation set) with the same batch size and the number of epochs necessary to achieve the lowest validation loss in the previous step
        * Calcuate the test set loss and accuracy. How well does your model perform to the baseline from chapter 2.1 in the book?

## Part 2: Scalar regression (5 points)

* Use the Boston housing dataset from chapter 3.6 to predict median housing markets using a deep learning model
* Use 10-fold cross validation to monitor validation set performance
* At the end of your notebook, report the test set MSE based on your final model trained using all of the training data
* Scoring
    * 3 points for proof of model testing (maintain a notebook with a history of your tests of different models)
    * Remaining 2 points awarded based on relative performance within the class as measured by test set MSE
        * 2 points - 1-5 place
        * 1.5 points - 6-15 place
        * 1 point - 16-30 place
        * 0.5 points - 31-40 place

## Estimating your deep learning models

You can use any computing platform to complete this assignment. However the best performance will come from using a GPU-enabled computer. I recommend using an Amazon AWS EC2 instance as I explained in class. You can use an alternative platform (e.g. Google Cloud, RCC, your laptop), but I will not offer technical support for any other environment.

### Setup Amazon AWS EC2 instance

> You can refer to Appendix B in Deep Learning for Python/R for more detailed instructions. As I mentioned in class, it is easier to use the AMI I link to in the instructions below.

* Create an account on [Amazon AWS](https://aws.amazon.com/)
* Request an increase for `p2.xlarge` instances via [these instructions](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-resource-limits.html#request-increase). **This will take several hours to process before you can proceed to the next step.**
* [Create a new instance using this AMI with a `p2.xlarge` instance](https://aws.amazon.com/marketplace/pp/B0785SXYB2)
* Download your key and store it in a dedicated folder
* Open the terminal and `cd` to the folder with your key
* SSH into the instance once active
    * `ssh -i "<key.pem>" ubuntu@<ec2>`

### For Python and Jupyter Notebook

* You need to first install the most recent version of TensorFlow and Keras
    ```python
    sudo pip3 install tensorflow-gpu
    sudo pip3 install keras
    ```
* Launch `jupyter notebook`
    * Note the url/token displayed in the terminal
* Log into Jupyter Notebook server
    * Open a new local terminal
    * `cd` to the folder with your key
    * SSH a new connection
        ```bash
        ssh -N -L 8888:localhost:8888 -i <key.pem> ubuntu@<ec2>
        ```
    * Use your web browser to go to the link provided in the previous terminal window. This link will work as long as the Jupyter Notebook server is running and your SSH connection to `localhost:8888` is active.

### For R and RStudio Server

* SSH into the instance
    ```bash
    ssh -i <key.pem> ubuntu@<ec2>
    ```
* Install Python `virtualenv`
    ```bash
    sudo apt-get install python-virtualenv
    ```
* Create a new user account
    ```bash
    sudo adduser <username>
    ```
* Login to RStudio Server
    * Open a new local terminal
    * `cd` to the folder with your key
    * SSH a new connection
        ```bash
        ssh -N -L 8787:127.0.0.1:8787 -i <key.pem> ubuntu@<ec2>
        ```
    * Go to `127.0.0.1:8787` in your web browser
    * Login using the username/password you just created
* Reinstall `keras` to the most recent version
    * `devtools::install_github("rstudio/keras")
* Install Keras and Tensorflow (the Python libraries)
    ```r
    library(keras)
    install_keras(tensorflow = "gpu")
    ```

### Warnings

* You are charged \$.90 per hour whenever your instance is running. When you are finished, **stop the instance** in the AWS console to avoid overcharging.
* Make sure to store all your work in a Git version controlled repository. **Make sure to clone your course project repo, store all your files in there, and commit/push back to GitHub before you stop the instance.**

## Submission format

* Submit your solution to each part as a separate Jupyter Notebook (if Python) or R Markdown document (if R)

## Submission deadline

Push your commit to your `PS3` folder in your `MACS30200proj` repo before class on Wednesday, May 16 (11:30 am).
