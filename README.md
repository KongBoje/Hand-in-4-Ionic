# Handin 4 - Ionic

>## Explain the concept of: Hybrid Mobile App Development

- Native Apps are specific to a given mobile platform (iOS or Android) using the development tools and language that the respective platform supports. Native apps look and perform the best
- HTML5 Apps use standard web technologies, like JavaScript and CSS to create cross platform mobile applications. Limitations from this strategy is, session management, no secure offline storage, no access to native device functionality (camera, calendar etc.)
- Hybrid Apps make it possible to embed HTML5 apps inside a thin native container, combining the best (and worst) elements of Native and HTML5 apps.

To get native-like functionality in fake HTML apps, we can use a tool such as Cordova.

Apache Cordova enables software programmers to build applications for mobile devices using CSS3, HTML5, and JavaScript instead of relying on platform-specific APIs like those in Android, iOS, or Windows Phone.[4] It enables wrapping up of CSS, HTML, and JavaScript code depending upon the platform of the device. It extends the features of HTML and JavaScript to work with the device. The resulting applications are hybrid, meaning that they are neither truly native mobile application (because all layout rendering is done via Web views instead of the platform's native UI framework) nor purely Web-based (because they are not just Web apps, but are packaged as apps for distribution and have access to native device APIs).

>## Explain the Pros & Cons of using Hybrid Mobile App Development compared to Native App Development

Pros:
- Cross platform
- Faster development
- Better maintainability

Cons:
- Performance could suffer
- Possibly miss out on extra native apis that are not supported by Cordova

>## Explain about the "building blocks" involved in an Ionic Hybrid Application

- AngularJS for presentation layer.
- Cordova for communication with phone hardware.
- HTML5 & Sass for styling and display of components.
- ADB to communicate with phone and enables debugging.
- Node.js to bring it all together.

>## Explain and demonstrate ways to debug Hybrid Mobile Applications Running on a real device

With Ionic you can debug your app through your browser using the sockets and ports that the phone uses to communicate with the browser, this enbables you to see the console and debug live.

If you use: "ionic run android".

Open Chrome and navigate to: "chrome://inspect/#devices"

>## Explain how and why, it is possible for a Hybrid Application to access native phone devices like location, calendar etc. 

Cordova or PhoneGap act as a common interface that can be used to expose native functionality.

>## Explain, using an example you have implemented, the "fundamentals" of an Ionic application.

Ionic uses AngularJS and Cordova to create Hybrid Apps, for the styling of this app Ionic uses CSS and JavaScript like BootStrap does. When creating the HTML for a the app, Ionic specific directives is used like this.

```
  <ion-side-menu side="left">
    <ion-header-bar class="bar-dark">
      <h1 class="title">Projects</h1>
      <button class="button button-icon ion-plus" ng-click="newProject()">
      </button>
    </ion-header-bar>
    <ion-content scroll="false">
      <ion-list>
        <ion-item ng-repeat="project in projects" ng-click="selectProject(project, $index)" ng-class="{active: activeProject == project}">
          {{project.title}}
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-side-menu>
```

>## Explain using an example how your Hybrid Application communicates with a backend 

>## Explain, with focus on location, technologies related to locations used on:

### Your app (client side)

### Your backend
