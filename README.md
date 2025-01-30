# Stepper-Music-Project
*TL:DR at end*

## Basic description:
This is a project I built to help my understanding of javascript. It is a musicial instrument made from stepper motors. 

---
# Project idea 
  I first came up with the idea to create this project when during me freshman year of university. I was building a personal project and required more materials from the parts store. There, I saw a display that used a stepper motor. in this display, they were rotating a heavy weight to show the strength of the motor, but what was more intriguing to me was the noise the motor was making. although it was impressive that the motor was very strong, it was also releasing a pitch similar to an electric piano. So instead of puchasing the parts I originally went to the store for, I purchased a few stepper motors and decided to try and make a new stepper motor piano!

To my enjoyment, I found that this project has been completed by a few other people, specifically, I watch this video (https://www.youtube.com/watch?v=mFHpNFJlB0w) about someone implementing MIDI files through JS to connect the motors to specific pitches based on their rotational speed. I followed his original ideas and obtained the necessary parts to build the project. I had very little experience with an arduino so this project was very educational for me in that way. 

# Basic improvements

###  Error handling 
After constructing the circuit, I noticed areas where the setup could be improved. Specifically, when setting up the project I noticed there was little consideration for error in the code. Specifically, I felt that in SteppermotorMuisc.java there should've been error consideration. When setting up the project I frequently found that the UI diddn't have the correct ports listed to optput the MIDI files to the motors, so to check if the error was due to a wrongly selected port, I implemented a simple error check. 

---
#### Original code:
<img width="811" alt="Screenshot 2025-01-22 at 5 54 05 PM" src="https://github.com/user-attachments/assets/c708f774-50cd-4158-a69f-2729ddc1487c" />

#### Minor Improvement:
<img width="821" alt="Screenshot 2025-01-22 at 5 56 46 PM" src="https://github.com/user-attachments/assets/40dbb160-5bac-4e87-bb61-bb85b821d3f5" />

### MIDI File Handling

Another issue occurred when uploading certain MIDI files. Errors were thrown without specific explanations. Additionally, the UI displayed MIDI files not located in the player directory but could not access them unless they were moved to the correct directory. To resolve this, I added a warning message guiding users to move the MIDI file to the proper directory.

---

#### Original code: 
<img width="821" alt="Screenshot 2025-01-22 at 6 06 13 PM" src="https://github.com/user-attachments/assets/01630c21-69b2-409b-adc8-fe4647deb0d6" />

#### Minor Improvement:
<img width="903" alt="Screenshot 2025-01-22 at 6 08 46 PM" src="https://github.com/user-attachments/assets/e72f1e38-674f-42f2-b3aa-28078a09cdc7" />







