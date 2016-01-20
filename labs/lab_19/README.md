All instructions can be found at: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html

##Prerequisites

Before you begin, be sure that you've completed the steps in Setting Up with Amazon EC2.
> http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/get-set-up-for-amazon-ec2.html

## Step 1: Launch an Instance

You can launch a Linux instance using the AWS Management Console as described in the following procedure. This tutorial is intended to help you launch your first instance quickly, so it doesn't cover all possible options. For more information about the advanced options, see Launching an Instance.

To launch an instance

* Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

* From the console dashboard, choose Launch Instance.

* The Choose an Amazon Machine Image (AMI) page displays a list of basic configurations, called Amazon Machine Images (AMIs), that serve as templates for your instance. Select the HVM edition of the Amazon Linux AMI. Notice that this AMI is marked "Free tier eligible."

* On the Choose an Instance Type page, you can select the hardware configuration of your instance. Select the t2.micro type, which is selected by default. Notice that this instance type is eligible for the free tier.

Note
T2 instances, such as t2.micro, must be launched into a VPC. If your AWS account supports EC2-Classic and you do not have a VPC in the selected region, the launch wizard creates a VPC for you and you can continue to the next step. Otherwise, the Review and Launch button is disabled and you must click Next: Configure Instance Details and follow the directions to select a subnet.
* Choose Review and Launch to let the wizard complete the other configuration settings for you.

* On the Review Instance Launch page, under Security Groups, you'll see that the wizard created and selected a security group for you. Instead, select the security group that you created when getting set up using the following steps:

* Choose Edit security groups.

* On the Configure Security Group page, ensure that Select an existing security group is selected.

* Select your security group from the list of existing security groups, and then choose Review and Launch.

* On the Review Instance Launch page, choose Launch.

* When prompted for a key pair, select Choose an existing key pair, then select the key pair that you created when getting set up.

* Alternatively, you can create a new key pair. Select Create a new key pair, enter a name for the key pair, and then choose Download Key Pair. This is the only chance for you to save the private key file, so be sure to download it. Save the private key file in a safe place. You'll need to provide the name of your key pair when you launch an instance and the corresponding private key each time you connect to the instance.

*Caution*
Don't select the Proceed without a key pair option. If you launch your instance without a key pair, then you can't connect to it.
When you are ready, select the acknowledgement check box, and then choose Launch Instances.

* A confirmation page lets you know that your instance is launching. Choose View Instances to close the confirmation page and return to the console.

* On the Instances screen, you can view the status of the launch. It takes a short time for an instance to launch. When you launch an instance, its initial state is pending. After the instance starts, its state changes to running and it receives a public DNS name. (If the Public DNS column is hidden, choose the Show/Hide icon in the top right corner of the page and then select Public DNS.)

* It can take a few minutes for the instance to be ready so that you can connect to it. Check that your instance has passed its status checks;you can view this information in the Status Checks column.

## Step 2: Connect to Your Instance

There are several ways to connect to a Linux instance. We will connect using your browser. Alternatively, you can connect using PuTTY or an SSH client. For more information, see Connecting to Your Linux Instance from Windows Using PuTTY or Connecting to Your Linux Instance Using SSH.

To connect to your Linux instance using a web browser

* You must have Java installed and enabled in the browser. If you don't have Java already, you can contact your system administrator to get it installed, or follow the steps outlined in the following pages: Install Java and Enable Java in your web browser.

* From the Amazon EC2 console, click Instances in the navigation pane.

* Select the instance, and then choose Connect.

* Choose A Java SSH client directly from my browser (Java required).

* Amazon EC2 automatically detects the public DNS name of your instance and populates Public DNS for you. It also detects the key pair that you specified when you launched the instance. Complete the following, and then click Launch SSH Client.

* In User name, enter ec2-user.

* In Private key path, enter the fully qualified path to your private key (.pem) file, including the key pair name.

  * (Optional) Choose Store in browser cache to store the location of the private key in your browser cache. This enables Amazon EC2 to detect the location of the private key in subsequent browser sessions, until you clear your browser's cache.

* If necessary, choose Yes to trust the certificate, and choose Run to run the MindTerm client.

* If this is your first time running MindTerm, a series of dialog boxes asks you to accept the license agreement, confirm setup for your home directory, and confirm setup of the known hosts directory. Confirm these settings.

* A dialog prompts you to add the host to your set of known hosts. If you do not want to store the host key information on your local computer, choose No.

* A window opens and you are connected to your instance.

Note
If you chose No in the previous step, you'll see the following message, which is expected:
Verification of server key disabled in this session.
If you can't connect to your instance, see Troubleshooting Connecting to Your Instance for assistance.

## Step 3: Clean Up Your Instance

After you've finished with the instance that you created for this tutorial, you should clean up by terminating the instance. If you want to do more with this instance before you clean up, see Next Steps.

Important
Terminating an instance effectively deletes it; you can't reconnect to an instance after you've terminated it.
If you launched an instance that is not within the AWS Free Tier, you'll stop incurring charges for that instance as soon as the instance status changes to shutting down or terminated. If you'd like to keep your instance for later, but not incur charges, you can stop the instance now and then start it again later. For more information, see Stopping Instances.

## To terminate your instance

In the navigation pane, choose Instances. In the list of instances, select the instance.

Choose Actions, then Instance State, and then choose Terminate.

Choose Yes, Terminate when prompted for confirmation.

Amazon EC2 shuts down and terminates your instance. After your instance is terminated, it remains visible on the console for a short while, and then the entry is deleted.
