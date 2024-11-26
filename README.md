<aside>
✅ **OverView of the Project**

- Opening background information 

- General description of the current project 

- Proposed idea for enhancements to the project 

- Value and significance of this project 

- Current limitations 

- Literature review

</aside>

# Title

Ball position detection and assistance in judging foul play on the soccer field

---

# Opening background information

---

- The ball position detection and foul play judgment assistance system in soccer fields has been developed as a result of advancements in sports technology to enhance the fairness of matches and improve fan experience.
Position detection technology:
    
    Real-time tracking of the ball and players' positions using GPS, IMU sensors, video analysis, and RFID tags.
    Foul play judgment:
    
    Identification of fouls or abnormal play patterns through data analysis, AI, and machine learning technologies.
    Application cases:
    
    Reviewing controversial situations through the VAR system and providing real-time data to fans to increase immersion.
    Ethical considerations:
    
    Discussions on privacy protection and ethical issues are necessary, and the technology should contribute to enhancing fairness.
    This system is being applied to various sports beyond soccer, improving the quality of games.
    

# General description of the current project

<aside>
This project aims to develop an auxiliary system that detects the ball's position in real-time on the soccer field and assists in judging foul play. Through this, we aim to enhance the fairness of the game and provide a better experience for players and fans.

</aside>

---

### **Proposed idea for enhancements to the project**

<aside>
Accurate ball position tracking:
• Integration of various technologies: Combining GPS, IMU sensors, RFID tags, and video analysis technologies to track the ball's position with high precision.
• Real-time data collection: Enables rapid analysis through immediate data collection during the game.

</aside>

---

### Value and signifiance of the project

<aside>
Enhancing game fairness:
• Reduction of foul play: Real-time detection and analysis of foul play increases the fairness of the game and promotes honest play among players.
• Reliable judgments: Data-driven decisions improve the reliability of referee judgments.

1. Improved fan experience
2. Advancement of sports technology
3. Player protection and adherence to ethical standards
4. Educational value

Due to these significant aspects, this project will contribute not only to technological advancement but also to the overall development and maintenance of fairness in soccer and other sports.

</aside>

---

### **Current limitations**

Data accuracy and consistency: It is difficult to maintain consistent accuracy across various environments and conditions.

Challenges in real-time processing: Immediate data processing and analysis during the game require high-performance computing resources.

Technical limitations: There are technical constraints such as sensor accuracy and network latency.

Cost issues: Significant expenses are involved in acquiring advanced equipment and building the system.

Regulatory and ethical issues: Consideration is needed for player privacy protection and ethical aspects of technology use.

---

### **Literature review**

The review of major literature and research related to this project yielded the following results:

- **Ball position tracking technology:** Research has been conducted on ball position tracking systems integrating various technologies such as GPS, IMU sensors, RFID tags, and video analysis. The accuracy and real-time performance of these technologies have also been evaluated.
- **Foul play detection using AI and machine learning:** Studies have been performed using deep learning algorithms to analyze players' movement patterns and identify abnormal behaviors. This can be utilized to assist referees in making decisions.
- **Real-time data processing and analysis:** Research has been conducted on technologies for processing and analyzing large amounts of data collected during games in real-time. This enables immediate judgment and feedback.
- **Ethical considerations:** Research has been carried out on the protection of players' personal information and the fairness of technology use. These are essential aspects to consider when implementing the system.
- **User experience research:** Studies have been conducted on the technology acceptance and user experience of players, referees, and fans. This is a key element in the practical application of the system.

Through this literature review, we can strengthen the technical foundation of the project and identify potential problems in advance to seek solutions.

---

Ball detected by AI

![00000262.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/e0d57b3c-2918-497d-8bc7-ddcfe5f32eaf/00000262.png)

# ## Image acquisition method:
- **Artificial intelligence video acquisition: We found the top 5 Korean University legendary goal videos on YouTube and acquired them using DarkLabel2.4 from Yolov5.**
1. **Dark Label**
- **Data Extraction**: Extract the collected video as an image from **DarkLabel**.

[DarkLabel2.4.zip](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/a61f8074-eee8-4940-ad80-3be76a74ccf2/DarkLabel2.4.zip)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/b24c09a2-e2db-474e-8c3b-cca7ae27f498/Untitled.png)

**If the video resolution is different, crop it to fit.**

[비디오 리사이저 - 온라인에서 무료로 비디오 해상도 변경](https://online-video-cutter.com/ko/resize-video)

**If it is 640x640, cut the video to fit the resolution and save it.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/f874b525-73ea-48f3-b1da-9076c62fe36a/image.png)

# When you run the ZIP file, this will appear. Here, open the YAML file and add the classes for the contents to be extracted.

<aside>
💡 my_classes2: ['lane','ball']

</aside>

<aside>
💡 format1:    # darknet yolo (predefined format]
fixed_filetype: 1                 # if specified as true, save setting isn't changeable in GUI
data_fmt: [classid, ncx, ncy, nw, nh]
gt_file_ext: "txt"                 # if not specified, default setting is used
gt_merged: 0                    # if not specified, default setting is used
delimiter: " "                     # if not spedified, default delimiter(',') is used
classes_set: "my_classes2"     # if not specified, default setting is used
name: "darknet yolo"           # if not specified, "[fmt%d] $data_fmt" is used as default format name

</aside>

**Class files and format files**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/bcfc6b5d-cdc8-4f54-a009-486f82725620/image.png)

### Open Video: Load the desired video or photo.
Open Image Folder: Opens a folder containing multiple photos.
0.pascal voc's select bar: Formatting Specifies the format. Here you can select the class name you want to label.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/b613ba16-9757-4469-b5b9-ed2de753c614/Untitled.png)

### How to extract a video image
Open open video and select the video you want to extract.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/d83e723d-0c9f-442d-b0f5-b0bc91989def/image.png)

**Open the video, create a file to save the image to be extracted, and extract the image.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/d9083827-a90a-4b3a-8f0f-c30843fc1288/image.png)

**Check Box + Label and label lane and ball.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/8b1bd829-ddbd-452d-8c72-5b144ad0a128/image.png)

# learning

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/2932e38b-4d82-4a45-a530-0465ac042fbd/image.png)

### After downloading yolov5
Go into the installed yolov5 file and install the package.
Then, the images and labels extracted from the yolov5 file created in this way are collected and the training is performed.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/3309e5ec-5c4c-47e9-ab24-4e8a51cc89f1/image.png)

**Include both photos and labeling in the train and valid files.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/2eb5abb5-b8e2-44d8-8886-3493f780d80a/image.png)

### learning outcomes

![00000189.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/5a1fd234-528e-4dc8-b842-5c7756e09f4e/00000189.png)

```
##검증 데이터 만들기
import os
import shutil
from sklearn.model_selection import train_test_split
```

**Trained label output train_batch**

![train_batch0.jpg](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/77a439de-0c01-4ff2-a3e0-c737de6b79b5/train_batch0.jpg)

![train_batch1.jpg](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/a7ce366f-91c4-44e9-ac47-081b8c640181/train_batch1.jpg)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/ac62d1ad-d581-4088-9930-7324c5c274b5/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/89e0682c-a91d-4929-aaba-b2e0beebb64d/image.png)

학습 결과를 비디오로 

[한국국대 레전드 골 top5 (1)_gt.mp4](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/87cc9e96-825a-420e-bb75-0e1c6150ca31/%ED%95%9C%EA%B5%AD%EA%B5%AD%EB%8C%80_%EB%A0%88%EC%A0%84%EB%93%9C_%EA%B3%A8_top5_(1)_gt.mp4)
