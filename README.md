# Obra theme for Drupal 8
A Polymer starting point for new Drupal 8 themes. 

## Mission Statement
Provide a baseline Drupal 8 theme that leverages Polymer with cross-browser compatitability that is easily extensible by users. The theme will update overtime to accomodate browser maturity (HTTP2 Server Push, PWA, etc). 

## Goals
- [ ] Polymer
  - [X] Setup Basic WebComponents.org elements
  - [ ] Setup custom bundled elements interoperability
- [ ] Pure Web Component example (no Polymer - for option?)
- [ ] Verify cross-browser compatibility (perhaps with Sauce Labs, etc)
- [ ] Twig-related
  - [X] Interoperable, thus Web Components are orchestrated by Twig
  - [ ] Document basic use case
- [ ] Theme-related
  - [ ] Base Theme (extends core/stable)
  - [ ] Demo Theme (extends obra_theme + app-layout WebComponent)

## Stretch Goals
- [ ] PWA shell out of the box
- [ ] CI/CD options for custom Polymer Elements

## Why Polymer?
Polymer itself is syntatical sugar over W3C Web Components that especially leverages Shadow DOM. 
This upcoming browser feature (already a part of Chrome and polyfills exist for other browsers), allows for style encapsulation, events, etc. Polymer, unlike other Javascript frameworks/libraries, is quite close to the browser platform allowing it's implementations be agnostic of orchestration layers. 

## Installing Development Dependencies
- [NPM](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/en/)
- [Bower](https://bower.io/)
- [Polymer CLI](https://www.polymer-project.org/2.0/docs/tools/polymer-cli).


## How to Develop

### Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

### Viewing Your Element(s)

```
ROOT     $ cd elements  
elements $ polymer serve
```

### Running Tests

```
ROOT $ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). 
Run `polymer test` to run your application's test suite locally.

### Build Polymer Assets
```sh
ROOT $ polymer build
```

### Enable Twig Debugging
Edit `sites/default/services.yml` as prescribed in link: 
[https://www.drupal.org/docs/8/theming/twig/debugging-twig-templates](https://www.drupal.org/docs/8/theming/twig/debugging-twig-templates).
Twig will orchestrate HTML tag allocation per typical Drupal 8. When looking to apply WebComponent tags, 
find the proper Twig file by inspecting (in Chrome or Firefox) an HTML element. Edit the producing Twig file for markup changes.
Example below:
```html
<div>
  <!-- THEME DEBUG -->
  <!-- THEME HOOK: 'block' -->
  <!-- FILE NAME SUGGESTIONS:
     * block--obra-theme-main-menu.html.twig
     * block--system-menu-block--main.html.twig
     x block--system-menu-block.html.twig
     * block--system.html.twig
     * block.html.twig
  -->
  <!-- BEGIN OUTPUT from 'core/themes/stable/templates/block/block--system-menu-block.html.twig' -->
  <nav role="navigation" aria-labelledby="block-obra-theme-main-menu-menu" id="block-obra-theme-main-menu" class="contextual-region">
     <h2 class="visually-hidden" id="block-obra-theme-main-menu-menu">Main navigation</h2>
     <div data-contextual-id="block:block=obra_theme_main_menu:langcode=en|menu:menu=main:langcode=en" class="contextual" role="form"><button class="trigger focusable visually-hidden" type="button" aria-pressed="false">Open Main navigation configuration options</button>
     <!-- THEME DEBUG -->
     <!-- THEME HOOK: 'links__contextual' -->
     <!-- FILE NAME SUGGESTIONS:
      * links--contextual.html.twig
      x links.html.twig
     -->
     <!-- BEGIN OUTPUT from 'core/themes/stable/templates/navigation/links.html.twig' -->
     <ul class="contextual-links" hidden=""><li class="block-configure"><a href="/admin/structure/block/manage/obra_theme_main_menu?destination=node">Configure block</a></li><li class="entitymenuedit-form"><a href="/admin/structure/menu/manage/main?destination=node">Edit menu</a></li></ul>
     <!-- END OUTPUT from 'core/themes/stable/templates/navigation/links.html.twig' -->
     </div>
     <!-- THEME DEBUG -->
     <!-- THEME HOOK: 'menu__main' -->
     <!-- FILE NAME SUGGESTIONS:
        * menu--main.html.twig
        x menu.html.twig
     --> 
     <!-- BEGIN OUTPUT from 'themes/custom/obra_theme/patterns/02-organisms/menu.html.twig' -->
     <ul><li><a href="/" data-drupal-link-system-path="<front>" class="is-active">Home</a></li></ul>
     <!-- END OUTPUT from 'themes/custom/obra_theme/patterns/02-organisms/menu.html.twig' -->
  </nav>
<!-- END OUTPUT from 'core/themes/stable/templates/block/block--system-menu-block.html.twig' -->
</div>
```   

## Demo
### Dependencies
- [Docksal](https://docksal.readthedocs.io/en/master/) (helper for [Docker](http://docker.io/))
- [Drupal Composer](https://github.com/drupal-composer/drupal-project)  (helper for [Composer](https://getcomposer.org/))

<!-- setup demo drupal application, provide phpunit testing base, TravisCI (run, npm test if there are scripts, etc) ? --> 
<!-- do not add extra cruft. people just need clear instrucitons how to setup theme locally. Base is bare, Demo is possible starting point --> 
