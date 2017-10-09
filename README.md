# Obra theme for Drupal 8
A Polymer starting point for new Drupal 8 themes. 

## Mission Statement
Provide a baseline Drupal 8 theme that leverages Polymer with cross-browser compatitability that is easily extensible by users. The theme will update overtime to accomodate browser maturity (HTTP2 Server Push, PWA, etc). 

## Goals
- [ ] Polymer
- [ ] Cross-browser compatibility
- [ ] PWA shell out of the box
- [ ] Instruction and compatibility with Twig
	- [ ] Demo Theme

## Why Polymer?
Polymer itself is syntatical sugar over W3C Web Components that especially leverages Shadow DOM. 
This upcoming browser feature (already a part of Chrome and polyfills exist for other browsers), allows for style encapsulation, events, etc. Polymer, unlike other Javascript frameworks/libraries, is quite close to the browser platform allowing it's implementations be agnostic of orchestration layers. 

## Installing Development Dependencies
- [NPM](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/en/)
- [Bower](https://bower.io/)
- [Polymer CLI](https://www.polymer-project.org/2.0/docs/tools/polymer-cli).

## Build Polymer Assets
```sh
polymer build
```
## Demo
### Dependencies
- [Docksal](https://docksal.readthedocs.io/en/master/) (helper for [Docker](http://docker.io/))
- [Drupal Composer](https://github.com/drupal-composer/drupal-project)  (helper for [Composer](https://getcomposer.org/))

<!-- setup demo drupal application, provide phpunit testing base, TravisCI (run, npm test if there are scripts, etc) --> 
<!-- do not add extra cruft. people just need clear instrucitons how to setup theme locally. --> 
