# Tutorial: Deploying a basic Sapper app on Jekyo

Demo app [here](https://sapper-demo.jekyo.app/)

### Prerequisites

Make sure you have [NodeJS](https://nodejs.org/en/download/), [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) and [git](https://github.com/git-guides/install-git) installed.

If it's your first time using **Jekyo**, you can **install** it by running the following command in your terminal:

`npm install -g jekyo`

### Sign in to Jekyo

You can sign in to Jekyo by running `jekyo user:signin`

```
➜  ~ jekyo user:signin 
Your email?: **************
Your password?: **********
You have successfully signed in!
```
If you don't have a Jekyo account, you can create one in the terminal by running `jekyo user:signup`. 

## 1. Create a basic Sapper app

You can start your Sapper project by using `jekyo create`

Using the **arrows** on your keyboard, select **sapper** and press **enter**.  
```
? Select template
  None Creates only the application
  expressjs A basic app skeleton using [Express](https://expressjs.com/)     
  nuxt-js A boilerplate SSR application using [Nuxt.js](https://nuxtjs.org/) 
❯ sapper A basic starter app using [Sapper](https://sapper.svelte.dev/)
```
When prompted, enter the desired name for your Sapper app. 

`Application name?: sapper-tutorial`

This will create a basic Sapper app in the current directory by cloning this [Sapper starter app](https://github.com/jekyo/sapper-getting-started) repository.

```
Cloning source code... OK
Application created!
```

### Deploy the Sapper app on Jekyo

To deploy the app, first navigate to the newly created directory:

`cd sapper-tutorial`

Now you can deploy this app to Jekyo by running: 

`jekyo deploy`

After a while, you should see something like this:

```
➜  Fetching source code ... OK
➜  Building application, this might take a while ... OK
➜  Publishing application, this might take a while  ... OK
➜  Deploying application ... OK        
➜  Waiting for application to start ... OK
➜  Visit your app on: https://sapper-tutorial.jekyo.app ... OK
```

You can now browse to your Sapper app on https://sapper-tutorial.jekyo.app (replace 'sapper-tutorial' with your app name)

## 2. Deploying an existing Sapper app

Navigate to your local Sapper app directory

`cd my-sapper-app`

Initialize a git repository if you haven't already done so by running `git init`. 

### Create an empty Jekyo app:

`jekyo create` 

Select 'none' using the **arrows** on your keyboard and press **enter**. This will create an app using your current directory. 

```
? Select template (Use arrow keys)
❯ None Creates an application from your current directory
```

Name your app: 

`Application name?: my-sapper-app`

Run `jekyo link` to link your local app to the remote Jekyo app. Select 'my-sapper-app' using the **arrows** on your keyboard and press **enter**.

```
? Select application (Use arrow keys)
❯ my-sapper-app
```
### Now you can deploy this app to Jekyo by running: 

`jekyo deploy`

After a while, you should see something like this:

```
➜  Fetching source code ... OK
➜  Building application, this might take a while ... OK
➜  Publishing application, this might take a while  ... OK
➜  Deploying application ... OK        
➜  Waiting for application to start ... OK
➜  Visit your app on: https://my-sapper-app.jekyo.app ... OK
```

You can now browse to your Sapper app on https://my-sapper-app.jekyo.app (replace 'my-sapper-app' with your app name)

## Pushing local changes to Jekyo 

Add the newly modified file(s) to the git index by using [git add](https://www.atlassian.com/git/tutorials/saving-changes)

`git add filename`

Create a [git commit](https://github.com/git-guides/git-commit)

`git commit -m "your commit message"`

Now, simply deploy your app again:

`jekyo deploy`

You will see your changes on your live app after a short while. 