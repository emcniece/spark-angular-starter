# particle-angular-starter

Provides a starter framework for [Particle Core](https://www.Particle.io/) applications with [Ionic Framework](http://ionicframework.com/) wrapped around an AngularJS app.

## Online Demo
[http://particle-angular-starter-demo.herokuapp.com/](http://particle-angular-starter-demo.herokuapp.com/)

This demo uses browser localstorage and the credentials are not stored remotely - this means that you can access this page from your own browser or mobile device and safely connect your account and cores on private devices.

The main "Dashboard" page is an example of some controls interacting with the Particle JS library.

##Web Tutorial
This tutorial demonstrates the ability to interact with a Particle Core that is connected to a string of NeoPixel LEDs.

1. Flash a Particle Core with the sketch located in the *Particle_firmware* folder
1. Add an account in the Particle/Accounts tab. [[link](http://particle-angular-starter-demo.herokuapp.com/#/tab/Particle/accounts)]
1. Add cores from the Particle/Cores tab. [[link](http://particle-angular-starter-demo.herokuapp.com/#/tab/Particle/cores)]
1. Navigate back to the Dashboard, select a device from the top **Device:** interface
1. Pull down to initialize device and load active data
1. Change colors and patterns to send commands to the device!

##Local Tutorial
You can run this on your own machine! Ensure that [NodeJS](http://nodejs.org/download/) is installed.

1. Clone to a local folder (`git clone https://github.com/emcniece/particle-angular-starter.git`)
1. Enter directory, install NodeJS modules (`cd particle-angular-starter; npm install`)
1. Run local server (`npm start`)
1. Browse to [http://localhost:5000](http://localhost:5000)

##Modular Design

The app file hierarchy is organized so that users are able to pull the core AngularJS Particle folder *(www/components/Particle)* out and drop it into a new project.

- www
  - assets
  - components
    - Particle (modals, pages, tabs, module JS)
  - core (Main Angular app JS)
    - app.js
    - controllers.js
    - misc.js
    - services.js
  - shared (Main Angular app HTML)
    - modals
    - tabs


##Todo
- Make selecting and initializing a device more streamlined, handle non-initted devices better
- Change the _sending_ overlay to a footer growl-esque notification so you can still do things while waiting
- Make the **Listeners** section do things
- Make the **Variables** section do things
- Make the **Functions** section do things


###Notes

- The **Set Color** button on the Dashboard reflects the chosen RGB values after converting them to an additive color scheme, as rendering RGB values in an LED is a bit different than generating colors on the web.
- This app has been tested with [Phonegap](http://phonegap.com/) and works well!
