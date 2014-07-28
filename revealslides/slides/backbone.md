# Why not Backbone
- We used backbone on another project (show google trends graph of backbone, angular, ember)
- backbone and dust.js and grails
- nested views in backbone are problematic
- two way data-binding not quite there
- still using the Jquery view of the world

notes:
 	- Leaned on research Linked In did when building out their mobile site.
 	- dust.js template were tied into grails resource pipeline for pre-compiling (slowed development down)
 	- we implemented a postRender function to allow us to trigger functionality after view was rendered. Worked fine in pre-prod, but failed in the wild.
 		Many 'type is undefined' errors when trying to use jquery validator
 	- There were some plugins to help with this, but not easy to deal with
 	- Still needed to use Jquery for DOM manipulation, form validation, etc... 