# Important! :warning::warning::warning:
❗ When asked to login to a Canvas account, you will need to create a new account. This is the AWS Canvas account, and will not be the same as your USD Canvas account.

- In AWS Learner Labs once you reach $50 all of your code will be automatically destroyed. In addition, AWS Learner Labs has occasional issues where your environment is not accessible.
- **Be sure that you are ALWAYS storing your code in GitHub. You will not be given extra time to complete an assignment due to your Learner Lab deleting your code.**
- In order to make it easy to complete labs and work on your project, it is highly reccomended that you follow the below process, and at the step where you will create a JupyterLab Space, create two (one for a `lab` one for a `project`. Be sure you are saving your work from the `project` JupyterLab Space to your own GitHub repository.


# Setup Instructions
[<img src="https://github.com/MADS508/labs/blob/main/img/youtube_screen.png" width="100%">](https://youtu.be/-fm_Blh1m7c)


## 1. Login to AWS Learner Labs

![Console](https://github.com/MADS508/labs/blob/main/img/aws_console.png)
Be sure to read the [AWS Academy Learner Lab Student Guide.pdf](https://github.com/MADS508/labs/files/12005191/AWS.Academy.Learner.Lab.Student.Guide.pdf)


## 2. Launch the AWS Lab
Within the Learner Lab Setup Guide follow the steps in the [Using Your Learner Lab](https://ole.sandiego.edu/bbcswebdav/pid-2625324-dt-content-rid-35250884_1/xid-35250884_1) section.

1. From the Dashboard select your course. Then click `modules`
![LearnerLabStep1](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep1_2.png)

2. Click `Launch AWS Academy Learner Lab`
![LearnerLabStep2](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep2_2_1.png)

3. In the top right click `Start Lab` This will take 2-3 minutes. Be sure to monitor your budget, once you reach $100 all of your code will be automatically destroyed. **Be sure that you are ALWAYS storing your code in GitHub. You will not be given extra time to complete an assignment due to your Learner Lab deleting your code.**
![LearnerLabStep3](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep3.png)

4. Once the lab has loaded you will see a green dot to the right of the AWS status, click it to open the AWS console.
![LearnerLabStep4](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep4.png)


## 3. Launch Amazon SageMaker AI

In the AWS Console search bar, type `SageMaker` and select `Amazon SageMaker AI` to open the service console.

Search for and select `Amazon SageMaker AI`
![Search Box - SageMaker](https://github.com/MADS508/labs/blob/main/img/search-box-sagemaker.png)

Select `Studio` and then click the button `Set up for organization`
![Notebook Instances](https://github.com/MADS508/labs/blob/main/img/setup.png)

Select the `Set up for organizations` option.
![Quick Start](https://github.com/MADS508/labs/blob/main/img/sm-quickstart-iam-existing-2_1.png)

- For the domain name enter `lab`
- For How do you want to access studio, choose Login through IAM
- Leave Who will use Sagemaker blank
- Choose Next.
- If there is a red warning banner that complains about `There is an issue when requesting the service quota. Please try again.`, Ignore it it will not impact your Lab.
![Users](https://github.com/MADS508/labs/blob/main/img/usersandMl20.png)

For Configure roles and ML activities
- Select `Use an existing role`
- Be sure LabRole is selected
- Choose Next.
![Users](https://github.com/MADS508/labs/blob/main/img/usersandMl3.png)

Under `SageMaker Studio` select `SageMaker Studio New`. Under `JupyterLab`, turn on `Enable idle shutdown`.
![ConfigureApplications1](img/ConfigureApplications1a.png)

Expand the Canvas section and disable Amazon Q and disable both MLOps settings and disable `Enable local file upload`
![Canvas](img/Canvas.png)

Under `Canvas Ready-to-use models configuration` select `Use an existing execution role`
- Find your AWS ID by clicking on your username in the top right of the screen.
- ![Find AWS ID](https://github.com/MADS508/labs/blob/main/img/FindAWSID.png)
- Replace `834486164294` from `arn:aws:iam::834486164294:role/LabRole` with your account ID (removing the `-`s)
![Time Series](https://github.com/MADS508/labs/blob/main/img/CanvasIAM.png)

For the `Customize Studio UI` step, leave the defaults and click Next.

For Network, choose public internet access.  Select the existing VPC and all subnets, select the security group named `default`, then choose Next. 
![Network](https://github.com/MADS508/labs/blob/main/img/Network.png)

On the Storage screen, leave the settings as is and click next.
![Storage](https://github.com/MADS508/labs/blob/main/img/Storage.png)

On the Review and create screen, confirm all of the settings followed the above, and click Submit.
Wait 10-15 minutes for the studio to build. It only takes this long on initial setup, in the future it will take 2-3 minutes to access an existing studio.
![Pending Studio](https://github.com/MADS508/labs/blob/main/img/studio_pending.png)

Open the studio by clicking `Domain` and then select your domain name.
![Open Studio](https://github.com/MADS508/labs/blob/main/img/SelectDomain.png)

Select `User profiles` and then click `Add user`
![Add User](https://github.com/MADS508/labs/blob/main/img/AddUser.png)

Leave the `General Settings` as is, execution role must be `LabRole`, click next.
![User step 1](https://github.com/MADS508/labs/blob/main/img/User1.png)

Under `SageMaker Studio` select `SageMaker Studio New`. Under `JupyterLab`, turn on `Enable idle shutdown`.
![ConfigureApplications1](https://github.com/MADS508/labs/blob/main/img/ConfigureApplications1a.png)

Expand the Canvas section and disable Amazon Q and disable both MLOps settings and disable `Enable local file upload`
![Canvas](https://github.com/MADS508/labs/blob/main/img/Canvas.png)

Under `Canvas Ready-to-use models configuration` select `Use an existing execution role`
- Find your AWS ID by clicking on your username in the top right of the screen.
- ![Find AWS ID](https://github.com/MADS508/labs/blob/main/img/FindAWSID.png)
- Replace `834486164294` from `arn:aws:iam::834486164294:role/LabRole` with your account ID (removing the `-`s)
![Time Series](https://github.com/MADS508/labs/blob/main/img/CanvasIAM.png)

- On the `Customize Studio UI` screen click Next.

- On the `Data and Storage` screen, do not change anything, click Next.

- On the review screen, click Submit.

Click `User Profile` and on your user click `Launch` and select `Studio`
![Launch](https://github.com/MADS508/labs/blob/main/img/Launch2.png)

On the left click the `JupyterLab` icon, then click the `Create JupyterLab Space` button on the top right
![JupyterLab1](https://github.com/MADS508/labs/blob/main/img/JupyterLab1.png)

Enter a name for your space and click `Create Space` *It is suggested to make one named `lab` and one named `project`.*
![JupyterLab2](https://github.com/MADS508/labs/blob/main/img/NewJupyterLab2.png)

Change instance to `ml.m5.xlarge` and change storage to `25` then click Run Space
![JupyterLab3](https://github.com/MADS508/labs/blob/main/img/JupyterLab3.png)

Once your JupyterLab space has been created, click the `Open` button.
![JupyterLab4](https://github.com/MADS508/labs/blob/main/img/JupyterLab4.png)

## 4. Launch a New Terminal within JupyterLab

Click `File` > `New` > `Terminal` to launch a terminal in your Jupyter instance.
![Terminal Studio](https://github.com/MADS508/labs/blob/main/img/studio_terminal2.png)


## 5. Clone this GitHub Repo in the Terminal

Within the Terminal, run the following:
`git clone -b main https://github.com/mechristenson/aai-540-labs.git`

If you see an error like the following, just re-run the command again until it works:
```
fatal: Unable to create '.git/index.lock': File exists.

Another git process seems to be running in this repository, e.g.
an editor opened by 'git commit'. Please make sure all processes
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier:
remove the file manually to continue.
```
_Note:  Just re-run the command again until it works._

## 6. Navigate to Lab 01
- On the Left hand side click the icon of the folder
- Click `labs`
- Click `01_oreilly_book`
- Double Click `01_Setup_Dependencies.ipynb`
- Use the default kernel `Python 3 (ipykernel)`

# Shutting Down Sagemaker: Important! :warning::warning::warning:
When you are done working for the day (or more than 1 hour) you must shutdown both Jupyter Labs AND Learner Labs, else you will continue to spend budget. This video shows how.
[<img src="https://github.com/MADS508/labs/blob/main/img/youtube_screen.png" width="100%">](https://youtu.be/DczkVcBFkUg)

# Creating a Public S3 Bucket
In order to easily share your source files, you may want to upload them to S3. In order to do this one group member will need to make a public S3 bucket and load the source files to it. This will allow other group members to read (not write to the bucket) the raw files, in order to copy them to their Sagemaker space/own bucket for processing.
[<img src="https://github.com/MADS508/labs/blob/main/img/youtube_screen.png" width="100%">](https://youtu.be/ZvOR2RgGLNY)
You can use this bucket policy as a starting spot, be sure to change the bucket name to your bucket name.
```
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "GetFiles",
			"Effect": "Allow",
			"Principal": "*",
			"Action": "s3:GetObject",
			"Resource": [
				"arn:aws:s3:::scoyne-test202507",
				"arn:aws:s3:::scoyne-test202507/*"
			]
		},
		{
			"Sid": "ListFiles",
			"Effect": "Allow",
			"Principal": "*",
			"Action": "s3:ListBucket",
			"Resource": [
				"arn:aws:s3:::scoyne-test202507",
				"arn:aws:s3:::scoyne-test202507/*"
			]
		}
	]
}
```

# Using Github with Sagemaker for your project
If you are having trouble connecting your project github repo to Sagemaker, give this a watch.
[<img src="https://github.com/MADS508/labs/blob/main/img/youtube_screen.png" width="100%">](https://youtu.be/D6U8BkEAM1c)

# Creating Athena Tables for Multiple Datasets
If you use AWS Athena and have more than one file format, its important they you copy your source data from your public bucket into your sagemaker generated S3 bucket, and structure them into folders so that Athena can read the data. This short video explains how.
[<img src="https://github.com/MADS508/labs/blob/main/img/youtube_screen.png" width="100%">](https://youtu.be/dPrV-qEYQPk)
