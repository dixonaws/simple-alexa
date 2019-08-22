# The simplest way from 0 to Alexa
You can do this from macOS, Windows, or Cloud9 in AWS. 
Tested with Node v6.1.3 and Python 3.6.6 on macOS 10.14.2, using AWS us-east-1.
Make sure to create accounts on aws.amazon.com and developer.amazon.com.

Install and configure the AWS CLI<br>
<code>pip install awscli</code><br>
<code>aws configure</code>

Install the Alexa Skills Kit CLI<br>
<code>npm install -g ask-cli</code>

Initialize the ASK CLI<br>
<code>ask init --no-browser</code>

Create a new Alexa Skill; choose your preferred runtime and template here (the "Fact" template is simple) <br>
<code>ask new --skill-name "my-new-skill"</code>

Deploy your new skill<br>
<code>cd my-new-skill</code><br>&nbsp;</b>
<code>ask deploy</code>

Test your new skill (from within your skill's directory)<br>
<code>ask dialog --locale "en-US"</code>

Modify your skill's intent schema and Lambda function to taste. 
The intent schema is located in <skill-dir>/models/. The Lambda function
is located in <skill-dir>/lambda/py<br> for Python-based skills.

Deploy your modified skill<br>
<code>ask deploy</code>







