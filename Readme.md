# FLang
This is the specification for a frontend language, that can replace the 3 main
languages that represent a web application.

### Disclaimer
The contents of this document is my opinion on a laguage that I would like to
write instead of HTML / CSS / JavaScript. It only applies to traditional web
applications: get data from backend, display it in the DOM and style via CSS.

## Requirements
This is the list of requirements that the language should conform by:

  * 90% of the codebase of a traditional web applciations should consists only
    in this language
  * It should
    * describe the state of the application
    * compile down to a single file for production
    * be readable
    * run in the browser only
  * As a programmer I should be able to
    * [comment on the code](features/comment.md)
    * [use CSS units ( px, em, etc.. )](features/units.md)
    * [use CSS color definitions ( rgba, hsla, hex, keyword )](features/colors.md)
    * [use HTTP requests ( XMLHTTPRequest )](features/xhr.md)
    * use WebSocket connections ( WebScoket )
    * [define DOM structure / state](features/dom-structure.md)
    * define reuseable elements
    * bind (and transform) values to display properties
    * describe events
    * describe styles
    * split my application into different files
  * As a programmer I want the language to
    * handle minification
    * handle concatenation
    * handle communication
    * decide if a style definition is inline or not
    * add necessary JavaScript polyfills
    * add necessary CSS prefixes
