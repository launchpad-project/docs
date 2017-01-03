# Data

###### Leverage a NoSQL database with search and real-time capabilities using *WeDeploy™ Data*.

<div class="guide-btn-cta">
  <a class="btn btn-accent btn-sm" href="http://data-demo.wedeploy.io" target="_blank">
    <span class="icon-16-external"></span>See Live Demo
  </a>
</div>

<!-- <article id="install-dependencies"> -->

## Install Dependencies

This section assumes you already have the **WeDeploy CLI** installed and **Docker** running. Make sure to [visit the installation guide](/docs/intro/using-the-command-line.html) if you need help setting that up.

We also feature code snippets using the API Client, [visit this guide](/docs/intro/using-the-api-client.html) in order to start using it.

<!-- </article> -->

<!-- <article id="running-locally"> -->

## Running Locally

1. Clone this repository:

  ```text
git clone -b js https://github.com/wedeploy/boilerplate-data.git boilerplate-data-js
cd boilerplate-data-js
  ```

2. Run this container locally:

  ```text
we dev
  ```

3. Now your container is ready to be used:

  ```text
http://datademo.wedeploy.me
  ```

<!-- </article> -->

<!-- <article id="deploying-to-the-cloud"> -->

## Deploying to the Cloud

1. [Fork this repository](https://github.com/wedeploy/boilerplate-data/fork).
2. Go to the [Dashboard](http://dashboard.wedeploy.io).
3. [Create a project](http://dashboard.wedeploy.io/new).
4. In the sidebar, click on *GitHub Integration*.
5. Type your repository URL and `js` branch.
6. Click on *Update Project*.
7. Click on *Build All Repos* and wait a few seconds.
8. Once you see it in the Dashboard, your container will be ready to be used.

  ```text
http://datademo.wedeploy.io
  ```

<!-- </article> -->


## Next Steps

Now that you have *WeDeploy™ Data* API settled up, you can interact [saving new data](/docs/data/saving-data.html).
