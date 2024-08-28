<h1>Text Narrator – Amazon Polly </h1>


<h2>Description</h2>
In this project I will be developing a text narrator using Amazon Polly, it will be able to take a piece of text that has been uploaded to an Amazon S3 bucket and convert it to speech, I will be able to adjust the voice, pitch and speed. 
<br />


<h2>Services used</h2>

- <b>Amazon Polly
- <b>AWS Managment Console
- <b>AWS IAM

<h2>Architectural Diagram</h2>

<img src="https://imgur.com/orKdDef.png" height="80%" width="80%"/>

<h2>Project walk-through:</h2>

<p align="center">
First I am going to be creating a IAM role with the suitable policies attached to it. I went to the create IAM role section, chose AWS service and selected Lambda as the use case.  <br/>
<img src="https://imgur.com/01gPFuX.png" height="80%" width="80%"/>
<br />
<br />
Next I added permissions from the list that will be needed for this project (AmazonPollyFullAccess, AmazonS3FullAccess and AWSLambdaBasicExecutionRole) and gave a role name.   <br/>
<img src="https://imgur.com/adzhnEY.png" height="80%" width="80%"/>
<img src="https://imgur.com/7Ad2fuk.png" height="80%" width="80%"/>
<br />
<br />
Next I went S3 bucket to create and configure the bucket I will be using. I gave the backet a name and kept the rest of the options as default.  <br/>
<img src="https://imgur.com/cJGWkYy.png" height="80%" width="80%"/>
<br />
<br />
Next I started creating the Lambda function by going to the Lambda page and clicking on create a function. I gave an appropriate name and set the runtime to Node.js 16.x. In the change default configuration role I checked the "Use an existing role" and selected the role I previously created. <br/>
<img src="https://imgur.com/dBHj5zo.png" height="80%" width="80%"/>
<br />
<br />
Next I started writing the Lambda function code and clicked Deploy <br/>
<img src="https://imgur.com/KV3HTwx.png" height="80%" width="80%"/>
<img src="https://imgur.com/wFWrzef.png" height="80%" width="80%"/>
<img src="https://imgur.com/ePAEHAu.png" height="80%" width="80%"/>
<br />
<br />
Next I checked the output to make sure everything is working by creating a test event <br/>
<img src="https://imgur.com/S7znfW8.png" height="80%" width="80%"/>
<br />
<br />
I next ran the test and made sure it worked <br/>
<img src="https://imgur.com/9ewrREZ.png" height="80%" width="80%"/>
<br />
<br />
Once it has been successfully run it will save the audio file in the bucket I created <br/>
<img src="https://imgur.com/n4gHV9Y.png" width="80%"/>
<br />
<br />

 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

