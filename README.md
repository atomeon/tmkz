http://techmeetup.co/
=========

## TECH Meetup Kazakhstan.

Based on work of [Thinkmill's](http://www.thinkmill.com.au) demo of [KeystoneJS](http://keystonejs.com).

### Coding Guidelines

If you're contributing code, please do your best to follow the conventions established in the codebase already. This makes pull requests much easier to review and merge.

We have generally followed the guidelines set out in [AirBnB's Javascript Style Guide](https://github.com/airbnb/javascript), with the exception of using real tabs for indentation.


## Getting Started

To run the site locally, there are a few things to set up.

Because we have some private keys for our MongoDB, Cloudinary accounts, you'll need to set up your own equivalents before the site will run properly.

### Install Node.js and MongoDB

You'll need node 0.10.x and npm 1.3.x installed to run SydJS. The easiest way is to download the installers from [nodejs.org](http://nodejs.org).

You'll also need MongoDB 2.4.x or higher.

If you're on a Mac you'll also need Xcode and the Command Line Tools installed or the build process won't work.

### Setting up your copy 

Get a local copy of the site by cloning this repository, or fork it to work on your own copy.

Then run `npm install` to download the dependencies.

Before you continue, create a file called `.env` in the root folder of the project (this will be ignored by git). This file is used to emulate the environment config of our production server, in development. Any `key=value` settings you put in there (one on each line) will be set as environment variables in `process.env`.

The only line you **need** to add to your `.env` file is a valid `CLOUDINARY_URL`. To get one of these, sign up for a free account at [Cloudinary](http://cloudinary.com) and paste the environment variable if gives you into your `.env` file. It should look something like this:

	CLOUDINARY_URL=cloudinary://12345:abcde@cloudname

### Running your isntance

Once you've set up your configuration, run `node keystone` to start the server.

By default, [Keystone](http://keystonejs.com) will connect to a new local MongoDB database on your localhost called `sydjs`, and create a new Admin user that you can use to log in with using the email address `user@keystonejs.com` and the password `admin`.

If you want to run against a different server or database, add a line to your `.env` file to set the `MONGO_URI` environment variable, and restart the site.

When it's all up and running, you should see the message `SydJS is ready on port 3000` and you'll be able to browse the site on [localhost:3000](http://localhost:3000).

### Here be ~~fireflies~~ errors

#### or, how you don't have any content yet

The first time you run the site, the homepage will warn you that it expects there to be at least one meetup, and your database won't have any. Don't freak out, just go to [/keystone](http://localhost:3000/keystone), sign in as the admin user, and create one.

You'll probably want to add some other content too (blog post, members, etc) to get all the pages looking right.

... happy hacking!
