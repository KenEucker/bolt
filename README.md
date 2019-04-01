# bolt
A dynamic web component generator and publishing repository.

Bolt's frontend allows developers to include web components anywhere they want to on existing websites, or to create entire websites of web components that interact with each other through Bolt.

Bolt's backend takes a JSON object as input and, using templates and code snippets, builds a singular output of Html, CSS, and Javascript. With these three files, and whatever accompanying assets, web components can be published to Amazon AWS S3 or to Google Cloud Storage for external integration with websites. Additionally, components can be published to a marketplace that enables Bolt integrated websites to install web compoents at the click of a button.

# Philosophy
Web components should be isolated, self-contained, modular, consistent, pluggable, injectable, renderable, updatable, and testable. These things mean different, but separate, solutions for different people - but those differences between developers shouldn't hold hostage the stack and course of development in order to accomplish small website features and frontend solutions for larger applications. Data layer interactions, state management, api interactions, and the setup and teardown of components shouldn't be handled by the components themselves; this is a given.

To think that language, stack, or framework used to create a website should also dictate the framework, language, and implementation of components within that website is limiting. As long as you know how to plug things together on the backend and where to place things on the frontend then you should be enabled to implement your website however you see fit.

The architecture of view and view model separated by how data is stored and retrieved and how the combination of the two is rendered has always been littered with business rules and data processing before and after long term storage retrieval. There must be a way to separate business rules from the process of combining website components to complete a specific task.

Bolt is a web component delivery, maintenace, and deployment package that provides both a component marketplace and an on-property component management interface. Much like hypernova will render a view from a set of data and respond with the code to present to the UI -- Bolt delivers a fully rendered component that is able to plug into a websites existing UI infrastructure. However, what Bolt does differently is that it provides a marketplace of components that allows you to view the source code as well as view and test components which can be added to your website at the click of a button. Much like google tag manager will deliver code to a website that runs after initial load, Bolt can load code for these web components from external sources after initial load or even hotloaded at another point in time.

# Development History

## 0.0.0 / 2019-4-1

* init1 - Another write-from-scratch solution to solve same problem as similar projects that have come before it in which I have been the sole architect and developer:
  * [Quasi](https://github.com/KenEucker/quasi), (January 2017), is the frontend templating MVP that includes routing, authentication, and may eventually tie together "bolt" components to provide a seemless integration of web components and dependencies in a single "page" application. Quasi is clientside focused, thus the architecture and server are not fully developed.
  * [Quasar](https://github.com/KenEucker/quasar), (November 2017), is the build runtime MVP that produces singular outputs, from web components to entire websites, leveraging any templating paradigm (React, Sass, Mustache, Pure HTML-JS-CSS, etc... ). Quasar is serverside and render focused, thus the UI is not fully developed.

# Roadmap
Version 0.1 :: Architecture
* Input via json manifest.
* Ouput to local filesystem.
* Mechanism for including snippets in templates.
* Mechanism for including data in templates and snippets.
* Asset compilation and bundling on input.
* Asset mutation on output (minification, tree shaking, code splitting, uglification).
* Library for all actions pertaining to bolt component construction for both serverside and clientside render.

Version 0.5 :: MVP
* Generates web components from templates and code snippets; into a singular output.
* Can be used a standalone library or consumed by gulp as a plugin.
* Takes input from a CLI or from a JSON manifest to create and publish components.
* Integrates with Amazon AWS S3 and Google Cloud Storage for storing published assets.
* Pulls in additional data for output from external JSON endpoints.

Version 1.0 :: Stable
* Fully documented API and consumable npm package.
* Publish to server and serverless environments.
* Bolt.js client library for managing Bolt components encapsulated within an existing website.
* Bolt component library website for publishing, downloading, and consuming bolt components.
