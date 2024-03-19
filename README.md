# Heartbeat-Anomaly-Detection-Model
This repository provides code for heartbeat anomaly detection model using power and computation efficient libraries (TinyML used here) which allows this code to be easily run on edge devices like Arduino.

The running model can be accessed through this link:
https://smartphone.edgeimpulse.com/classifier.html

The colab notebook containing the code can be found here:
https://colab.research.google.com/drive/1lqrIUG4wLiP2n0dNNAkT8Ra_aXCmOkti?usp=sharing

Training accuracy:

![image](https://github.com/kllaveya/Heartbeat-Anomaly-Detection-Model/assets/97512929/e134bf1f-e652-486d-bccf-0d7bba494c49)

Testing accuracy:

![image](https://github.com/kllaveya/Heartbeat-Anomaly-Detection-Model/assets/97512929/630960fa-829d-4666-902c-146f9c906613)


We tried implementing federated learning in our project as well, though because of lack of enough dataset, we could not get a satisfactory accuracy - only 34.29%.
To tackle the issue of lack of enough data, we considered using data augmentation techniques like time shifting, pitch shifting, time stretching and amplitude scaling. But since heartbeat audio data is extremely sensitive to distortions, the accuracy dropped. Any misclassification of such a sensitive use case can have fatal consequences.

We attribute the lack of availability of heartbeat audio dataset to:
1. It is not common for health institutes to record heartbeat audio since mostly ECG scans are used for testing and diagnosis purposes.
2. The sensitivity of the information also plays a role as not many health institutes deem it appropriate to share their patients heartbeat recordings (if they have them) publicly due to strict privacy regulations surrounding health data.

The colab notebook containing the code for the same:
https://colab.research.google.com/drive/1_2oBTOPNA0Nazrx5ZHxMH8KYVIui8kLT
