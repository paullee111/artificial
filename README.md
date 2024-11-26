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
![00000262](https://github.com/user-attachments/assets/02a8c0c5-ef53-4842-8298-eedd6598c08c)



# ## Image acquisition method:
- **Artificial intelligence video acquisition: We found the top 5 Korean University legendary goal videos on YouTube and acquired them using DarkLabel2.4 from Yolov5.**
1. **Dark Label**
- **Data Extraction**: Extract the collected video as an image from **DarkLabel**.

[DarkLabel2.4.zip](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4449964-ec8f-4727-af39-ee4a29ebc257/a61f8074-eee8-4940-ad80-3be76a74ccf2/DarkLabel2.4.zip)

![Untitled](https://github.com/user-attachments/assets/d05d1c73-557d-4b30-88cb-9892d466987d)


**If the video resolution is different, crop it to fit.**

[비디오 리사이저 - 온라인에서 무료로 비디오 해상도 변경](https://online-video-cutter.com/ko/resize-video)

**If it is 640x640, cut the video to fit the resolution and save it.**

<img width="619" alt="image" src="https://github.com/user-attachments/assets/41a85574-bf64-425a-94cd-96e8e726b5b9">


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


<img width="168" alt="image (1)" src="https://github.com/user-attachments/assets/a43e65f7-3ca8-4e8a-a1d1-98e1d8d880af">


### Open Video: Load the desired video or photo.
Open Image Folder: Opens a folder containing multiple photos.
0.pascal voc's select bar: Formatting Specifies the format. Here you can select the class name you want to label.


<img width="140" alt="Untitled (1)" src="https://github.com/user-attachments/assets/e53161ed-57df-486d-8da3-3fed0b25d958">

### How to extract a video image
Open open video and select the video you want to extract.


<img width="626" alt="image (2)" src="https://github.com/user-attachments/assets/64fa3b5d-08e3-4620-9baf-c904dde184cd">

**Open the video, create a file to save the image to be extracted, and extract the image.**


<img width="827" alt="image (3)" src="https://github.com/user-attachments/assets/21d79c92-b8f2-42b6-b3a3-e0e9d9968170">

**Check Box + Label and label lane and ball.**


<img width="827" alt="image (4)" src="https://github.com/user-attachments/assets/01d50d61-78aa-4b68-8710-8815f89940f5">

# learning


<img width="569" alt="image (5)" src="https://github.com/user-attachments/assets/7872b340-a91c-4175-ba37-cf77a1504380">

### After downloading yolov5
Go into the installed yolov5 file and install the package.
Then, the images and labels extracted from the yolov5 file created in this way are collected and the training is performed.


<img width="833" alt="image (6)" src="https://github.com/user-attachments/assets/a191ceea-d7da-452f-8bb9-9977c5752c9e">

**Include both photos and labeling in the train and valid files.**


<img width="250" alt="image (7)" src="https://github.com/user-attachments/assets/bae682f8-5713-439e-9be7-f77b1552766c">

### learning outcomes


![00000189 (1)](https://github.com/user-attachments/assets/5c7400c8-0ff0-4825-bd52-4f44e50ba036)

```
##검증 데이터 만들기
import os
import shutil
from sklearn.model_selection import train_test_split
```

**Trained label output train_batch**


![train_batch0 (1)](https://github.com/user-attachments/assets/ffd55b94-343f-4acc-80aa-edb6013dc46c)


![train_batch1 (1)](https://github.com/user-attachments/assets/5bf8a622-685a-45b5-89e0-f17e71bb2d87)

<img width="489" alt="image (8)" src="https://github.com/user-attachments/assets/fec589f9-a8be-4d28-b3fc-02b4a13ea7b8">

<img width="606" alt="image (9)" src="https://github.com/user-attachments/assets/815988a6-216b-46b1-a16b-7a99acab3fce">

학습 결과를 비디오로 


https://github.com/user-attachments/assets/b20f4d64-5664-41c5-96e4-c0073ef2c6e2


