https://www.tiny.cloud/blog/node-js-send-email/

Sending Option 1: Nodemailer + SMTP
Before we get into the pros and cons of using Nodemailer and SMTP, it’s important to understand what SMTP is. SMTP, or Simple Mail Transfer Protocol, is the method by which emails are sent over the internet. It was established back in the 1980’s and is still in use today. 

When you send an email, SMTP is used to relay the email to the recipient’s email server. Nodemailer creates an SMTP connection within your app, so the emails can be sent from your SMTP server.

Pros of sending through Nodemail + SMTP
There are two main cases when someone would use SMTP to send email from within their app.

To leverage existing infrastructure
If you already have your own SMTP server that’s fully operational, why reinvent the wheel by adding another third party vendor to the mix?
You’re in an industry that’s heavily regulated (such as healthcare or government).
SMTP offers more fine-tuning and control over every aspect of how your emails are sent, including how data is stored and transferred.
Cons of sending through Nodemail + SMTP
Using SMTP also comes with some drawbacks, like: 

Needing to maintain, upgrade and troubleshoot your own SMTP server
Needing to constantly monitor your sender reputation
The scalability challenges that come with managing your own servers.
Sending Option 2: Third party transactional email API service
With the explosion of SaaS platforms in the past decade, there was a need to “outsource” the transactional act of sending emails, in order to free up development resources for more high-value activities. This is when services like Amazon SES (Simple Email Service), SendGrid and others came onto the scene.

These services remove the need for inhouse expertise and time taken to set up and maintain an SMTP server. Instead, by using APIs, they take care of all the nitty gritty details so you don’t have to. And like any Cloud service, you pay based on usage, rather than fixed hardware costs.

Pros of sending through a transactional email API service
The main advantages of these services are: 

Cost savings
The ability to scale as you grow without investing additional capital
Don’t need an inhouse email expert – most backend developers can pick up the basics with little effort.
Lastly, these services have many value-add features that help you manage your sender score, troubleshoot issues, generate reports and manage subscriptions. They’re all things that you’d otherwise have to manage, if running your own SMTP server.

Cons of sending through a transactional email API service
The main drawback to this approach is:

You’re tied to another third party 
Switching can be a pain if you’ve already built API calls for one service into your app and you need to switch to another provider.
And if you work in a highly sensitive area (e.g. the secret service), a transactional email service may not be for you. Instead, you’ll likely want full control of your data and not have it pass it through third parties.

Lastly, if you’re already running your own SMTP server and have the team to support it, why incur another cost and set up yet another dependency?

Now, on to the tutorials. Both tutorials assume you’re using Node.js and have some JavaScript experience.