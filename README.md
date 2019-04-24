# Node Stripe Membership SaaS

This project is an updated boilerplate of [eddywashere/node-stripe-membership-saas](https://stripe.com) express app for creating a membership/subscription site with [Stripe](https://stripe.com), [Mailgun](https://mailgun.com/signup), mongodb and swig. Inspired by [sahat/hackathon-starter](https://github.com/sahat/hackathon-starter) and [RailsApps/rails-stripe-membership-saas](https://github.com/RailsApps/rails-stripe-membership-saas). It also handles stripe webhooks.


### System Requirements
- mongodb
- nodejs

### Getting Started

First update `/server/config/secrets.js` with the following credentials:

- Stripe [API keys](https://dashboard.stripe.com/account/apikeys) and [plan info](https://dashboard.stripe.com/test/plans)
- [Mailgun](https://mailgun.com/signup) for sending forgot/reset password confirmations.
- session secret
- google analytics id

Install dependencies with `npm install`.

Start the server with `node server`.

Note: Stripe webhooks can be recieved at `https://your-url.com/stripe/events`.

### Heroku Deployment

```
heroku create your-awesome-saas-product
heroku addons:add mongohq
heroku config:set SESSION_SECRET='your_secret';
heroku config:set STRIPE_KEY='sk_test_example'
heroku config:set STRIPE_PUB_KEY='pk_test_example'
heroku config:set MAILGUN_DOMAIN='example.org'
heroku config:set MAILGUN_KEY='key-secret'
heroku config:set GOOGLE_ANALYTICS='UA-XXXXXX-1'
```

Want add a heroku deploy button? Pull requests welcome :]
