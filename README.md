# Penpal – Email templates for SaaS startups
Penpal is a collection of open-source email templates built on top of [Foundation's inky templating engine](http://foundation.zurb.com/emails), consisting of 20+ commonly needed email templates for all parts of the startup funnel from newsletter signup, to first sale, to lifetime value emails of a customer.

Penpal is part of [startup boilerplate](http://startup-boilerplate.co), an opinionated set of solutions for commonly used startup challenges, including email templates, marketing/sales funnels & integrations, as well as common frontend/backend solutions for things any app needs, such as login forms, email verifications, user permissions, and so on. These solutions are built on top of Polymer, Meteor and GraphQL.

For details on how to use the individual inky components, please refer to the [Foundation for Email docs](http://foundation.zurb.com/emails/docs/). Major props to sendwithus for writing an amazing guide on [how to send emails like a startup](https://www.sendwithus.com/resources/guide). The email templates are heavily influenced by this guide.

**Alright, let's have a look at some templates ʕ•͡ᴥ•ʔ**


#### Lifetime Value Emails
<img src='https://cloud.githubusercontent.com/assets/3836411/19974111/5c2ee6b4-a222-11e6-89ae-a73b1824f470.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974112/5c305076-a222-11e6-9f47-91e705346861.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974116/5c5c9b40-a222-11e6-809f-b94ce632dd5b.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974114/5c30d528-a222-11e6-8965-1b45bcb820de.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974110/5c2ce6e8-a222-11e6-8f74-34a866537883.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974113/5c307ee8-a222-11e6-9fba-6dd1eb125a5e.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974115/5c333e80-a222-11e6-9579-058963d9f01b.jpg' width='400'>

#### Welcome Emails
<img src='https://cloud.githubusercontent.com/assets/3836411/19974125/5c932e62-a222-11e6-9062-988890c1eef0.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974126/5c931724-a222-11e6-8c8d-a2a0463f449b.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974129/5c95561a-a222-11e6-8d0c-ab4b371c659b.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974127/5c9405c6-a222-11e6-94e8-7745160297e4.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974128/5c948f28-a222-11e6-94b2-dddf6377ecb7.jpg' width='400'>

#### Onboarding Emails
<img src='https://cloud.githubusercontent.com/assets/3836411/19974120/5c624234-a222-11e6-863d-8a86407e1f44.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974121/5c63822a-a222-11e6-9509-a88356fbd70c.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974118/5c60e74a-a222-11e6-9a98-d029bc3797ee.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974117/5c6047cc-a222-11e6-88a3-810419feb6f3.jpg' width='400'>

#### Other Transactional
<img src='https://cloud.githubusercontent.com/assets/3836411/19974123/5c8f3e42-a222-11e6-9fde-04a9f504e28a.jpg' width='400'>
<img src='https://cloud.githubusercontent.com/assets/3836411/19974119/5c6151da-a222-11e6-8ecc-489232f6aac1.jpg' width='400'>

**Currently available templates are:**
* Welcome: New signup for newsletter
* Welcome: New app signup, intro via welcome video
* Welcome: New app signup, intro via multiple options
* Welcome: New app signup, intro via quick 1,2,3 steps
* Welcome: New app signup, intro via detailed 1,2,3 steps
* Welcome: Referral by other users to sign up
* Onboarding: New user, suggest demo to continue
* Onboarding: New user, trial expiring soon, update your billing
* Onboarding: New user, trial expired and was never used, renew for 30 days
* Onboarding: New user, trial expired and was used, renew for 7 days
* Lifetime: Newsletter
* Lifetime: Product Updates
* Lifetime: Net Promoter score questionaire
* Lifetime: Follow up on old user, reiterates benefits
* Lifetime: E-Book download
* Lifetime: In-depth article to share
* Transactional: Reset password
* Transactional: Receipt/invoice

### Todos
- [ ] Fine-tune paddings
- [ ] E-Mail client testing via Litmus
- [ ] Write sample content for emails
- [ ] Design sample graphics for emails


### Using the CLI

Install the Foundation CLI with this command:

```bash
npm install foundation-cli --global
```

### Cloe repo & install npm dependencies 

First clone the repo:

```bash
git clone https://github.com/startup-boilerplate-co/penpal.git
```

Then install the necessary npm dependencies:

```bash
npm install
```

### Navigating the templates

* Once your server is run, each template can be found via localhost:3000/pagename.html
* Individual pages/templates can be found in the pages folder
* Reusable partials such as the header and footer can be found in the partials folder
* Custom CSS is found in app.scss


### Build Commands

Run `npm start` to kick off the build process. A new browser tab will open with a server pointing to your project files.

Run `npm run build` to inline your CSS into your HTML along with the rest of the build process.

Run `npm run litmus` to build as above, then submit to litmus for testing. *AWS S3 Account details required (config.json)*

Run `npm run zip` to build as above, then zip HTML and images for easy deployment to email marketing services. 

### Litmus Tests (config.json)

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


