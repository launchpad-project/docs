# Ruby

###### Launch a Ruby application in few steps.

<div class="guide-btn-cta">
  <a class="btn btn-accent btn-sm" href="http://boilerplate-ruby.wedeploy.io" target="_blank">
    <span class="icon-16-external"></span>See Live Demo
  </a>
</div>

<div class="guide-aux-cta">
  or read the <a href="https://github.com/wedeploy/boilerplate-ruby/" target="_blank">source code</a>.
</div>

<!-- <article id="install-dependencies"> -->

## Install dependencies

This section assumes that you already have the **WeDeploy CLI** installed and **Docker** running. Make sure to [visit the installation guide](/docs/intro/using-the-command-line.html) if you need help setting that up.

<!-- </article> -->

<!-- <article id="running-locally"> -->

## Running locally

1. Clone this repository:

  ```text
git clone https://github.com/wedeploy/boilerplate-ruby.git
cd boilerplate-ruby
  ```

2. Build the container:

  ```text
we build
  ```

3. Link this container with the local infrastructure:

  ```text
we dev --project <projectID>
  ```


4. Now your container is ready to be used:

  ```text
http://ruby.<projectID>.wedeploy.me
  ```

<!-- </article> -->

<!-- <article id="deploying-to-the-cloud"> -->

## Deploying to the cloud

1. [Fork this repository](https://github.com/wedeploy/boilerplate-ruby/fork).
2. Go to the [Dashboard](http://dashboard.wedeploy.com).
3. [Create a project](http://dashboard.wedeploy.com/new).
4. In the sidebar, click on *Deployment*.
5. Using your local machine, clone your Github fork:
  ```text
git clone https://github.com/<username>/boilerplate-ruby
  ```
6. Get into the folder: `cd boilerplate-ruby`.
7. Using the content on *Deployment* page. Add the WeDeploy remote url:
  ```text
git remote add wedeploy http://git.wedeploy.com/<projectID>.git
  ```
8. Push your data to wedeploy git server: `git push wedeploy master`.
9. Once you see it in the Dashboard, your container will be ready to be used.

  ```text
http://ruby.<projectID>.wedeploy.io
  ```

<!-- </article> -->

## What's next?

* Now you can start building your ruby based application.
