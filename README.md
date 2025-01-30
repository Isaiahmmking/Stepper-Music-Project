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
When setting up the project I noticed there were many areas that did not have proper error identification. When an error would occur, it would take me an trial and error to find the solutiot. I felt that in SteppermotorMuisc.java there should've been error consideration for incorrect port selection I frequently found that the program diddn't have the correct ports listed to optput the MIDI files to the motors, so to make it easier for a user, I implemented a simple error check for failed port connections.

---
#### Original code:
<img width="811" alt="Screenshot 2025-01-22 at 5 54 05 PM" src="https://github.com/user-attachments/assets/c708f774-50cd-4158-a69f-2729ddc1487c" />

#### Minor Improvement:
<img width="821" alt="Screenshot 2025-01-22 at 5 56 46 PM" src="https://github.com/user-attachments/assets/40dbb160-5bac-4e87-bb61-bb85b821d3f5" />

### MIDI File Handling

Another issue occurred when uploading certain MIDI files. Errors were thrown without specific explanations. Additionally, the program displayed MIDI files not located in the player directory but could not access the files unless they were moved to the correct directory (resulting in an error) To resolve this, I added a warning message guiding users to move the MIDI file to the proper directory.

---

#### Original code: 
<img width="821" alt="Screenshot 2025-01-22 at 6 06 13 PM" src="https://github.com/user-attachments/assets/01630c21-69b2-409b-adc8-fe4647deb0d6" />

#### My Changes:
<img width="903" alt="Screenshot 2025-01-22 at 6 08 46 PM" src="https://github.com/user-attachments/assets/e72f1e38-674f-42f2-b3aa-28078a09cdc7" />



# More important improvmenets
### resource management
The original code for this project originally used a try-catch-finally statement to deal with serial port management. However, I though the code could be improved using a try-with-reasources method instead, this way you could solve isses regarding improperly closed port without having to use a finally statement to close the port. This also made the code much easier to read and understand.

#### Original code:
<img width="903" alt="Screenshot 2025-01-29 at 8 36 17 PM" src="https://github.com/user-attachments/assets/988da51a-743c-4884-9814-2e57a6fcf1ac" />

#### My Changes:
<img width="903" alt="Screenshot 2025-01-29 at 8 38 28 PM" src="https://github.com/user-attachments/assets/7d1218ff-1a3b-48e1-b22e-fa6f86d51b9b" />


