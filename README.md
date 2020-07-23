# Our Temporary Website

[ http://picketstudio.com ](http://picketstudio.com)

This is/was intended as a placeholder site deployed when we set-up Picket 2.0, to cover off the basics of what we were offering and mention a few clients. It has subsequently been [updated](https://github.com/picketstudio/site/commit/b7ad83f967b6e5edc968677568e56685568c6e7f) with the new logo but will probably be replaced in its entirety by a [new site](https://github.com/picketstudio/home) in due course.

## Infrastructure

The site is static and deployed to Netlify via their direct integration with Github. Builds/deployments happen automatically whenever anything is pushed to the `production` branch on Github (configuration is [here](https://app.netlify.com/sites/picketstudio/settings/deploys)).

Netlify requires a `netlify.toml` file in the project root for configuring various aspects of the build and/or other server-side behaviour (including for local development). More can be learned about that [here](https://docs.netlify.com/configure-builds/file-based-configuration/).

## Contributing

To work with this site, you can simply clone the repository into a local folder on your computer. You shouldn't need any external services other than `git` and `npm` for package management.

~~~ sh
$ git clone https://github.com/picketstudio/site.git
$ cd site
~~~

## Installation

This site uses `npm` with a `package.json` specifying project details, dependencies and scripts. To get started with development, you'll need to run the following command:

~~~ sh
$ npm install
~~~

This will download and install all required dependencies.

## Local Development

Netlify has a tool for simulating their server enviroment locally, called [`netlify-cli`](https://docs.netlify.com/cli/get-started/). This has been added as a `devDependency` in `package.json` and is included in the `dev` script mentioned below, which will start the Netlify development server for you and consume the `netlify.toml` file.

~~~ sh
$ npm run dev
~~~
