# CyberDefenders
<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->


<!-- PROJECT LOGO -->
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h1 align="center">CyberDefenders</h1>
  <br>
  

  <img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/cyberdefenders_og%20copy.png">

<h3 align="center">Project Module - Blue Teaming</h3>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

The Cyberdefenders platform is an educational and training tool for cybersecurity that attempts to provide users real-world experience defending against cyberattacks. The website is made for people who wish to learn more about cybersecurity or develop their skills in this area, including professionals and students.

The Cyberdefenders platform has a number of features and tools available, such as:<br>

● Cybersecurity simulations: The software offers accurate representations of online threats and enables users to practice thwarting them in a secure setting.
<br>

● Learning materials: To assist users in learning about cybersecurity ideas and best practices, the platform provides a variety of instructional tools, including        articles, videos, and interactive content.
<br>

● Programs for certification: Cyberdefenders provides certification opportunities for users to show off their cybersecurity expertise.
<br>

● Support from the community: The site provides a user and mentor community that may help those who are studying and using cybersecurity techniques.
<br>

In general, Cyberdefenders is a thorough platform that offers users a variety of tools and possibilities to study and practice cybersecurity. CyberDefenders allow users to demonstrate their cybersecurity expertise and understanding.


<p align="right">(<a href="#top">back to top</a>)</p>

# 1. L'espion<br>
Category : Threat Intel

According to Crowdstrike, 'Threat intelligence is data that is collected, processed, and analyzed to understand a threat actor’s motives, targets, and attack behaviors. Threat intelligence enables us to make faster, more informed, data-backed security decisions and change their behavior from reactive to proactive in the fight against threat actor.'

In this challenge, a client has asked users to look into the incident and identify the attacker after their network was compromised and taken offline. Currently on the scene and having completed a preliminary investigation are incident responders and digital forensic investigators. Their research demonstrates that the attack was launched from a single user account, most likely an insider.
### Process
We are going to solve this case without using any terminal.
After we downloaded the challange contents, We will be provided with a zip file with all the preliminary data that can aid us in our investigation.


<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/pass.png"><br>

  
  After extracting the zip file we can see that there are three files. One of them is a text file named "Github". The name of the other two image files are "Office" and "WebCam".<br>

  
<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/files.png"><br>

  
If we open the file named "Github", we can see that the file contains the URL of an certain Github account.<br>

  
<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/URL.png"><br>

  
The URL address leads us to an github account of the user "EMarseille99". After visiting the github profile we can see that the user has 14 repositories that we can check manually one by one.


<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/github-profile.png"> 


Now let's try to solve some question with the information we already have.

**<h3>Question1</h3>**
<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q1.1.png">


  Our main goal here is to find out the API key added to the respiratories. Since we've checked all 14 repositories one by one, we found something interesting in the repository named "Project Build — Custom-Login-Page". This repository has two files. As soon as we open the "Login Page.js" file, we can see the API key in the code's top-most section. 


<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q1.png">
  
  * Answer
  ```sh
  aJFRaLHjMXvYZgLPwiJkroYLGRkNBW
  ```
**<h3>Question2</h3>**
<p align="center">

<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/ques-2.png">


 Srolling down the same file we can see that there is a password written in base64.
<p align="center">

<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q2..png">
We need to decode it for the answer.<br>
 
 <img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/decode.png"><br>
 * Answer
  ```sh
  PicassoBaguette99
  ```
**<h3>Question3</h3>**
<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q3.1.png">


Since we went through each repository one at a time a while back, we did come across various frameworks and tools that are connected to crypto-mining. It includes **XMRig**. **XMRig** is open-source software designed for mining cryptocurrencies like Monero or Bitcoin. <br>
 <img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q3.png">

 * Answer
  ```sh
 XMRig
  ```
We have solved first three question by analyzing given github profile. NOw, if we search insiders username which we got from github in google then we will see that the insider also have a linkedin and an instagram profile along with github.

<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/social%20media.png"> 

If we visit to the linkedin and instagram profile, we will find more information about him/her. 


**<h3>Question4</h3>**

<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q4..png"><br>

 We can see that the tread actor studied at the Sorbonne University.<br>

<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q4.png"><br>

 * Answer
  ```sh
Sorbonne
  ```
  **<h3>Question5</h3>**

<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/Q-5.png"><br>

 We can also see from his/hers linkedin bio that he/she is on **steam**.
**Steam** is a video game digital distribution service and storefront from Valve.<br>

<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q5..png">

<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q5.png"><br>
There is also a post with a qr code which leads to a gaming website in insiders instagram acccount.<br>
      <p align="center">
  <img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/qr.code.png"><br>

 
 * Answer
  ```sh
  Steam
  ```
 
 **<h3>Question6</h3>**
<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q.no6.png"><br>
If we go to the insiders instagram account, we will find the link to the insiders instagram profile.
<p align="center">
<img src="https://github.com/dreadb0t/CyberDefenders/blob/main/L%2Cespion-images/q6.png"><br>
 
  * Answer
  ```sh
  https://www.instagram.com/emarseille99/
  ```
  
  **<h3>Question7</h3>**
