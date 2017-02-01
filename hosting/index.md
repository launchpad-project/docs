# Hosting

###### Serve static files easily using *WeDeploy™ Hosting*.

<div class="guide-btn-cta">
  <a class="btn btn-accent btn-sm" href="http://boilerplate-hosting.wedeploy.io" target="_blank">
    <span class="icon-16-external"></span>See Live Demo
  </a>
</div>

<div class="guide-aux-cta">
  or read the <a href="https://github.com/wedeploy/boilerplate-hosting" target="_blank">source code</a>.
</div>

<!-- <article id="install-dependencies"> -->

## Install dependencies

This section assumes that you already have the **WeDeploy CLI** installed and **Docker** running. Make sure to [visit the installation guide](/docs/intro/using-the-command-line.html) if you need help setting that up.

<!-- </article> -->

<!-- <article id="running-locally"> -->

## Running locally

WeDeploy™ provides a way to run your project locally using a sandbox system.

1. Start local infrastructure:

  ```text
we run
  ```

2. Clone this repository:

  ```text
git clone https://github.com/wedeploy/boilerplate-hosting.git
cd boilerplate-hosting
  ```

3. Link this container with the local infrastructure:

  ```text
we link --project demo
  ```

4. Now your container is ready to be used:

  ```text
http://hosting.demo.wedeploy.me
  ```

Inside this project folder, you can find a `container.json` with the container ID used in this case: `hosting`.

<!-- </article> -->

<!-- <article id="deploying-to-the-cloud"> -->

## Deploying to the cloud

1. [Fork this repository](https://github.com/wedeploy/boilerplate-hosting/fork).
2. Go to the [Dashboard](http://dashboard.wedeploy.com) and create a project.
3. In the sidebar, click on *Deployment*.
4. Using your local machine, clone your Github fork:
  ```text
git clone https://github.com/<username>/boilerplate-hosting
  ```
5. Get into the folder: `cd boilerplate-hosting`.
6. Using the content on *Deployment* page. Add the WeDeploy remote url:
  ```text
git remote add wedeploy http://git.wedeploy.com/<projectID>.git
  ```
7. Push your data to wedeploy git server: `git push wedeploy master`.
8. Once you see it in the Dashboard, your container will be ready to be used.

  ```text
http://hosting.<projectID>.wedeploy.io
  ```

<!-- </article> -->

<!-- <article id="error-pages"> -->

## Error pages

Files put into the special directory `/_error` are mapped as the error files to be served in case of an error. They must take the form of `<error code>.html`.

<!-- </article> -->

<!-- <article id="using-node-js"> -->

## Using Node.js

There’s a simple easy trick to publish your static assets if you already have Node.js in your build pipeline (for instance with [Grunt](http://gruntjs.com/) or [Gulp](http://gulpjs.com/)). In fact there’s a nice package on npm called [*gh-pages*](https://www.npmjs.com/package/gh-pages) originally intended to work with GitHub Pages that can be easily configured to work with WeDeploy.

In order for publishing to work remember that if your compiled site resides in a different directory (typically *dist/* or *build/*) you need to copy the *container.json* file in it too.

With Gulp you can for example do it as simply as this:

```js
gulp.task('container',  function() {
  return gulp.src('container.json')
    .pipe(gulp.dest('<YOUR-DIST-PATH>'));
});

gulp.task('build', [ 'container', ... ]);
```

To actually deploy with *gh-pages* you need to correctly point the `repo` and `branch` configuration properties.

An example (with Gulp.js) is the following:

```js
var ghpages = require('gh-pages');

gulp.task('build', [ ... ]);

gulp.task('deploy', ['build'], function(done) {
  ghpages.publish(path.join(__dirname, '<YOUR-DIST-PATH>'), {
    repo: 'http://git.wedeploy.com/<PROJECT-ID>.git',
    branch: 'master'
  }, done);
});
```

<!-- </article> -->


## What's next?

* Now you can start adding new static files and grow your application.
