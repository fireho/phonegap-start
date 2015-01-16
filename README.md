# Hello World PhoneGap Application

> A Hello World application built with PhoneGap

## Usage

Create a new app with the following repository:

    https://github.com/fireho/phonegap-start.git

## Work

HAML: `/app/html` -> `www`

SASS: `app/sass`  -> `www/css`

Coffeescript: `app/js` -> `www/js`


## Compile

Use `rake` or `guard` to compile on the fly.


## Contributors

### Updating the Application

The application is based on the [Apache Cordova Hello World][cordova-app] app.

#### 1. Update the Source

    cp cordova-app-hello-world/www www/

__Do not replace `www/config.xml`.__

__Do not replace `www/img/logo.png`.__

#### 2. Update index.html

Replace `<h1>Apache Cordova</h1>` with `<h1>PhoneGap</h1>`.

#### 3. Update PhoneGap Version

    <preference name="phonegap-version" value="x.x.x" />

#### 4. Commit

    $ git commit -am "Version x.x.x"

#### 5. Tag

    $ git tag x.x.x

[phonegap-cli-url]: http://github.com/phonegap/phonegap-cli
[cordova-app]: http://github.com/apache/cordova-app-hello-world
[nitrous-url]: https://d3o0mnbgv6k92a.cloudfront.net/assets/hack-l-v1-3cc067e(https://www.nitrous.io/hack_button?source=embed&runtime=nodejs&repo=phonegap%2Fphonegap-start&file_to_open=README.md
