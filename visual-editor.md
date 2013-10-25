# Visual Editor #

*Implement an ALPS editor that is primarily drag-n-drop*

## Summary ##
Create an editor that allows authors to deal directly with descriptors as visual elements on a canvas. 
Similar to (_can't believe i'm writing this_) UML. After adding, editing, moving descriptors on the canvas,
the author can *export* the results as a valid `application/alps` document (XML, JSON, possibly YAML).

*THOUGHT: Is there an internal editor format diff than export formats? proly 'yes'*

## Essential Behavior ##
 * Open editor
 * create a new ALPS document
 * drag a `descriptor` onto the canvas
 * right-click it to add attributes (contextual dialog w/ save)
 * drag a couple more on and edit them.
 * drop one `descriptor` _onto_ another `descriptor` now you have nested `descriptors` (works at multiple levels of nesting)
 
## Other Features ##
 * Implement it as a Web-based app? Desktop?
 * Implement a simple browser-based non-visual app for starters.
 * Allow author to import an existing ALPS document 
 * Support a _validator_ routine to check for non-compliance
 * Support external reference (possibly read-only) to other ALPS documents (local or remote)
 * Implement it as a remote service and provide an API (laggy for visual app, I bet)

 
