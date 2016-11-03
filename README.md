# Penpal – Email templates for SaaS startups | startup-boilerplate.co
Penpal is a collection of open-source email templates built on top of [Foundation's inky templating engine](http://foundation.zurb.com/emails), consisting of 20+ commonly needed email templates for all parts of the startup funnel from newsletter signup, to first sale, to lifetime value emails of a customer.

Penpal is part of [startup boilerplate](http://startup-boilerplate.co), an opinionated set of solutions for commonly used startup challenges, including email templates, marketing/sales funnels & integrations, as well as common frontend/backend solutions for things any app needs, such as login forms, email verifications, user permissions, and so on. These solutions are built on top of Polymer, Meteor and GraphQL.

For details on how to use the individual inky components, please refer to the [Foundation for Email docs](http://foundation.zurb.com/emails/docs/)


### Using the CLI

Install the Foundation CLI with this command:

```bash
npm install foundation-cli --global
```

### Cloe repo & install npm dependencies 

First clone the repo:

```bash
git clone ...
```

Then install the necessary npm dependencies:

```bash
npm install
```

## Build Commands

Run `npm start` to kick off the build process. A new browser tab will open with a server pointing to your project files.

Run `npm run build` to inline your CSS into your HTML along with the rest of the build process.

Run `npm run litmus` to build as above, then submit to litmus for testing. *AWS S3 Account details required (config.json)*

Run `npm run zip` to build as above, then zip HTML and images for easy deployment to email marketing services. 

## Litmus Tests (config.json)

Testing in Litmus requires the images to be hosted publicly. The provided gulp task handles this by automating hosting to an AWS S3 account. Provide your Litmus and AWS S3 account details in the `example.config.json` and then rename to `config.json`. Litmus config, and `aws.url` are required, however if you follow the [aws-sdk suggestions](http://docs.aws.amazon.com/AWSJavaScriptSDK/guide/node-configuring.html) you don't need to supply the AWS credentials into this JSON.

```json
{
  "aws": {
    "region": "us-east-1",
    "accessKeyId": "YOUR_ACCOUNT_KEY",
    "secretAccessKey": "YOUR_ACCOUNT_SECRET",
    "params": {
        "Bucket": "elasticbeanstalk-us-east-1-THIS_IS_JUST_AN_EXAMPLE"
    },
    "url": "https://s3.amazonaws.com/elasticbeanstalk-us-east-1-THIS_IS_JUST_AN_EXAMPLE"
  },
  "litmus": {
    "username": "YOUR_LITMUS@EMAIL.com",
    "password": "YOUR_ACCOUNT_PASSWORD",
    "url": "https://YOUR_ACCOUNT.litmus.com",
    "applications": ["ol2003","ol2007","ol2010","ol2011","ol2013","chromegmailnew","chromeyahoo","appmail9","iphone5s","ipad","android4","androidgmailapp"]
  }
}
```

For a full list of Litmus' supported test clients(applications) see their [client list](https://litmus.com/emails/clients.xml).

**Caution:** AWS Service Fees will result, however, are usually very low do to minimal traffic. Use at your own discretion.


