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
Prerequisites: [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/en/), [bower](https://bower.io/)
and [polymer-cli](https://www.polymer-project.org/2.0/docs/tools/polymer-cli).

## Build Polymer Assets
```sh
polymer build
```
## Demo
### Dependencies
- [Docker](http://docker.io/)
- [Docksal](https://docksal.readthedocs.io/en/master/)
- [Composer](https://getcomposer.org/)
