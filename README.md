# Covid-Face-Mask-Mail-Alert
The Project detects a person without a safety mask in real time using CV, OpenCV in Python and sends an email alert to the supervisor immediately along with a warning message on the screen.

This Code Packet is written in Python, written, tested on the local machine using Jupyter Notebook and trained on colab. The packet contains a python notebook, an output video and a Haarcascade frontal face detector classifier XML file.

 

Key Libraries used in the project is OpenCV, Keras, sklearn, Tkinter, Numpy, smtplib, and Matplotlib.

 

Note: This can only be run if the machine has Tensorflow 2.2.0 version or higher.

          You need to disable two-step verification on your Gmail account along with allowing access to less secure apps on your Gmail account to run this.

 

This Project aims to provide a pragmatic safety service in the prevalent pandemic condition. In order to ensure that every person wears a mask while entering a public or private place, a camera(web-camera in my case to show) will be the placed on the entry and whenever a person without a mask enters, a pop-up warning message displays on the Monitoring screen informing of the person and an alert email is sent to the authority concerned using Tkinter library of python.

The key Concept involved is Computer Vision using which a CNN model is created.

 

Dataset and its Creation

Dataset used contains 1376 images divided into 2 categories: a person wearing a mask and a person without a mask. The dataset was created by Prajna Bhandary. The Dataset was created by Ms. Prajna by web scraping different facial images of different angles like frontal, left and right angles, up and down, etc. Then the key facial points like of the nose, both ears, chin, lips and face width, etc were found and plotted on the faces. With the help of these facial points, a mask was superimposed on the faces of each 1376 images and hence an artificial face mask data was created.

 

The broad sequence of how the task was approached and achieved in the code packet is as follows:

1.  Defining data path reading and categorizing data and labels.

2. Normalizing the images, converting to grayscale, resizing, and making it input ready.

3. Converting to one-hot encoding and saving the respective data and target arrays.

4. Creating our Convolutional Model using Keras

5. Dividing our data into test/train and then training it.

6. Plotting accuracy and loss separately per epoch

7. Loading best model during training and applying face detecting classifier.

8. Opening the webcam feed and predicting per frame on the region of interest after resizing the frame according to the input size.

9. If no mask detected, pops a warning message till a person wears a mask(root window of Tkinter was initialized before for that)

10. Using the SMTP server, send emails from the mentioned sender and receiver with predefined Subject and Email Body.

11. Close the web feed with a trigger key.

 



