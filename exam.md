---
title: Exam Logistics
layout: page
nav_order: 0
nav_exclude: true
---


# Exam Logistics

{% assign current_exam = site.data.exams[site.data.exams.current_exam] %}

The {{ site.data.exams.current_exam }} is on <strong>{{ current_exam.date }}</strong>.<br>

If you need to take the exam remotely at that time, or if you need to take an alternate exam, or if you have another exam at the same time, or if you need DSP accommodations, please fill out this [{{ site.data.exams.current_exam }} accomodations form]({{ current_exam.form }}) by <strong>{{ current_exam.form_deadline }}</strong>. We will respond to all form submissions after the form closes. The form will remain open until {{ current_exam.form_open_until }}, but we cannot guarantee any requests submitted after {{ current_exam.form_deadline }}.<br>

The scope of the {{ site.data.exams.current_exam }} is as follows: <strong>{{ current_exam.scope }}</strong>.<br>

The exam will be closed-book, closed-notes, and closed-Internet. No calculators are allowed (no questions should require a calculator). However, you may use {{ current_exam.num_cheatsheets }} cheat sheets (each two-sided) of your own design. The cheat sheets must be handwritten on standard A4 or letter paper (8.5 x 11 inches). Handwritten tablet notes may be printed and used. If you need to print for free, you can access a [list of instructional printers](https://wprint.eecs.berkeley.edu:9192/user). Each student has $12.00 in their printing account for each semester, which is enough for 200 single-sided black and white printed sheets or 120 double-sided black and white printed sheets. Learn more about [EECS printers](https://inst.eecs.berkeley.edu/cgi-bin/pub.cgi?file=printers.help).


## In-Person Logistics

- We will email you your exam location a day or two before the exam.
- Please try to arrive early (around {{ current_exam.arrival }}), so that we can start on time. If you arrive late, you will not be granted any extra time.


## Remote Logistics


**Staff reserves the right to assign you a grade of 0 on the exam if you do not follow these policies.**

- Before the exam:
    - We will send you an email with a zoom link to record with before the exam.
    - Make sure to test your zoom recording. As long as it has a webcam feed, audio, and screen share, you should be good to go.
    - Make sure you have a stable internet connection for the cloud recording.
- On the day of the exam:
    - Join the Zoom meeting on the computer you will be using and share your entire screen.
    - Set up a camera showing your workspace (e.g. join Zoom on your phone, or turn on a webcam feed on your computer). Access examples of [sample setups and ways](https://fa22.cs161.org/sample-setups) to position your phone camera.
    - Make sure you share audio.
    - Make sure some form of time stamp is visible.
    - Multiple monitors are not permitted. If you must use another monitor, please "duplicate" the screens and show us evidence that this setting is enabled before you start the exam.
    - Show your Cal ID to the camera. If you do not have a Cal ID, show some proof of identification (CalCentral works).
    - Show a 360 degree view of the room you are taking the exam in.
    - At {{ current_exam.remote_release }}, you will be emailed a PDF of the exam, and an answer sheet assignment will appear on Gradescope. ([Here's a demo.]({{ site.data.exams.gradescope_demo }}))
    - If you need to print the exam, you must print it within the first 15 minutes of the exam and log it on [this google form]({{ current_exam.clarif_bathroom }}). You will not be compensated with extra time if you choose to print the exam.
    - You should only have the exam PDF, clarifications document, clarifications google form, and the Gradescope answer sheet on your screen during the exam.
    - If you have clarification questions, submit it to [this google form]({{ current_exam.clarif_bathroom }}). The top of your answer sheet has a link to the clarifications.
    - Please log on the same form if you use the bathroom.
    - The Gradescope answer sheet will close at 9pm PT for students with 100% time, 10pm PT for 150% time, and 11pm PT for 200% time. We will cross check your most recent edit to the Gradescope answer sheet with when you leave the Zoom call.
    - After the exam, your recording will automatically be uploaded and shared with CS161 staff. 
    Additionally, if you encounter any issue with your recording, please submit [a link to your recording]({{ current_exam.recordings }}). It’s okay if it takes a couple hours to upload your feed; just send us the recording as soon as you can.

- Technical difficulties:
    - If your camera is not set up correctly, or staff cannot hear your audio, make sure you're paying attention to the zoom chat in case a proctor asks you to fix your setup.
    - If you encounter any logistics problems during the exam, email [cs161-staff@berkeley.edu](mailto:cs161-staff@berkeley.edu).
    - If you encounter Internet problems, write your answers locally and send them to [cs161-staff@berkeley.edu](mailto:cs161-staff@berkeley.edu) as soon as the exam is over.
    - If you need to use the bathroom, leave your phone in camera view, and leave the video and audio feed on while you're away. Make sure to fill out [this google form]({{ current_exam.clarif_bathroom }}) and log the times you were away from the exam.
    - If you have issues submitting your recording, please email [cs161-staff@berkeley.edu](mailto:cs161-staff@berkeley.edu) as soon as possible.
- Privacy:
    - Course staff will respect your privacy and not disclose any information from the proctoring session after the exam, except in suspected cases of academic dishonesty.


## Academic Integrity


- Any form of communication or collaboration is cheating. Providing answers, receiving answers, and even just talking with others about course material during the exam windows are all violations of the Berkeley honor code.
- Every case of potential academic dishonesty will be manually reviewed, and you’ll be able to discuss the situation with an instructor.
- We may ask some students to take a short verbal exam after the exam and explain how to solve one or more problems that are similar to an exam question they got right.
- Please be mindful to not discuss the exam until solutions are released. Keep in mind that we still have alternates and DSP exams after the normal exam ends.
