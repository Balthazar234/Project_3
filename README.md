<h1>Deploying web app using Jenkins CI/CD declarative pipeline.</h1>

<h2>Project Description</h2>
This project utilizes Jenkins CI/CD declarative pipeline to automate the deployment process of a web application. The pipeline integrates version control, automated testing, and Docker containerization to streamline the continuous delivery of the web app, ensuring efficient and reliable deployments.
<br />


<p align="center">

  1. First of all, go to the AWS portal, and create a new instance. As

  - Name: jenkins-serve
  -  AMI: ubuntu.
  -  Instance type: t2.micro (free tier).
  -  Key pair login: Create > docker.pem.
  -  Allow HTTP.
  -  Allow HTTPS.
  -  (Download the .pem file.)
  -  Click on Launch Instance.
  
  <img src="https://i.imgur.com/uPvRf2z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

2. Now, connect to the EC2 instance that you have created. Copy the SSH from server:  

<br/>

<img src="https://i.imgur.com/bDJyDRx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. Go to the download folder, where the .pem file is placed and open the terminal in the same location, and paste the SSH.

5. Install Jenkins from the following link:

- https://www.jenkins.io/doc/book/installing/linux/

6. Install Docker by running:
- “Sudo apt-install docker.io”

7. Now check if it got installed by running “jenkins --version” and “docker --version”

<img src="https://i.imgur.com/A2ZGMpH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

8. Goto Jenkins Dashboard and Click on “New Item”
- Name: declarative_pipeline
- Select: Pipeline
- Description: This is a demo pipeline project.

<br/>

<img src="https://i.imgur.com/EBbdEws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

PipelineScript:

 <br/>
<img src="https://i.imgur.com/ZL9vt5Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/jobFZVw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br />
<br />
1
10.  Click on “Save”.

11.  Click on “Build Now”.

 <br/>
<img src="https://i.imgur.com/PkMDz46.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

12.  We can click on “Stage View” to check the results if it is still under process.

 <br/>
<img src="https://i.imgur.com/8jBvz49.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 
 13.  Once it will be completed, It will return as “Success”.

 <br/>
<img src="https://i.imgur.com/CcVCyc6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

14.  Now, Search for the Public IP with port 8001 in the browser,

 <br/>
<img src="https://i.imgur.com/E1kLwC5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<br />

We have built the image of a Web app source code, and deployed that image as a container, using Jenkins Pipelines.

<br/>
</p>
- <b>~Hassanat Hussain</b>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
