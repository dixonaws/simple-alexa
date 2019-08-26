# The simplest way from 0 to Alexa
In this walkthrough, we'll create a fully functional Alexa skill using the Alexa Skills Kit Command Line Interface. We'll make use of a pre-built template to stand up a skill and deploy it to an Amazon Echo device. You'll also be able to test the skill without a physical Echo device using the ASK-CLI or developer.amazon.com site.

Here is what you will need to get started:
1. An AWS account with permissions to create a Cloud9 environment, Lambda functions and obtain user IAM credentials
2. An account on developer.amazon.com
3. Optionally, an Amazon Echo device to test your skill

You can do this from macOS, Windows, or Cloud9 in AWS. 
Tested with Node v6.1.3 and Python 3.6.6 on macOS 10.14.2, using AWS us-east-1.
Make sure to create accounts on aws.amazon.com and developer.amazon.com.

Install and configure the AWS CLI<br>
<code>pip install awscli</code><br>
<code>aws configure</code>

Install the Alexa Skills Kit CLI<br>
<code>npm install -g ask-cli@1.5.2</code>

Initialize the ASK CLI<br>
<code>ask init --no-browser</code>

Create a new Alexa Skill; choose your preferred runtime and template here (the "Fact" template is simple) <br>
<code>ask new --skill-name "my-new-skill"</code>

> If you are using Cloud9 and see an error regarding an invalid security token, perform the following steps to disable temporary credentials:<br>
a. Enter the Cloud9 configuration section by clicking on the gear icon in the upper right corner of the IDE. Select AWS Settings > Credentials and turn off "AWS managed temporary credentials."
b. Configure the AWS CLI with security credentials for an IAM user that has permissions to create Lambda functions. Run <code>aws configure</code> and enter the AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY.<br>
c. Modify the ~/.aws/credentials file and ensure that it <i>does not</i> contain a AWS_SESSION_TOKEN section.<br>

Deploy your new skill<br>
<code>cd my-new-skill</code><br>
<code>ask deploy</code>

Test your new skill (from within your skill's directory)<br>
<code>ask dialog --locale "en-US"</code>

Modify your skill's intent schema and Lambda function to taste. 
The intent schema is located in <code>\<skill-dir\>/models</code>. The Lambda function
  is located in <code>\<skill-dir\>/lambda/py</code><br> for Python-based skills.

Deploy your modified skill<br>
<code>ask deploy</code>







