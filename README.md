# ASL-American-Sign-Language-Translator

This project translates American Sign Language (ASL) alphabet hand signs into English letters using a webcam. The program recognizes ASL alphabet gestures and displays the corresponding letter in real time.

![add image descrition here](direct image link here)

## The Algorithm

This project is written in Python and uses a webcam to capture live video. The video is processed by a machine learning model that was trained using NVIDIA Jetson for 35 epochs. The trained model analyzes each frame from the webcam and predicts the corresponding ASL alphabet letter.

The project only recognizes ASL alphabet hand signs and outputs a single English letter at a time. The program depends on Python and the required libraries used by the project.

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/5eea62c3-8807-4c81-926c-d5e517ee18f0" />

## Running this project

1. Download the ASL dataset from Kaggle:
   https://www.kaggle.com/datasets/mhamad12/asl-american-sign
2. Unzip the dataset.
3. Place the dataset into your NVIDIA Jetson Docker container.
4. Train the model using ImageNet for 35 epochs.
5. After training is complete, connect a webcam to the Jetson.
6. Run the project:
sudo imagenet.py --model=models/askmodelasl/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=data/asldata/labels.txt /dev/video0 file://asl_video_output.mp4 --headless
7. Hold an ASL alphabet hand sign in front of the webcam to see the predicted letter displayed on the screen.

https://drive.google.com/file/d/1ITd2B8BzLkVaBWOUM2MX_8uUTHZ0W2L4/view?usp=sharing
