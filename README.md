# The Hotline chat widget integration instructions


## Base endpoint URL
`http://chat.thehotline.us/thl-messaging.js`



## Configure widget

### Query strings
Query strings are obtained from the endpoint-URL or the URL of the page the widget is loading from. If present, page-URL query strings will override those in the endpoint. If a desired configuration is the default, it can be omitted from both URLs.



## Functionality

### Deployment key: 'key' (required)
Your unique deployment key obtained.
 * This is the only query string that must be declared in the endpoint-URL. It will not be obtained from the page-URL.
 * `key=44033576-e28e-8685-2b21-58sample3d9`


### Language: 
 * English = `en` (default)
 * Espanol = `es`
 * `thllanguage=es`
 * In development: `language=es` and `lang=es`. These common language delcarations can be leveraged - with the abilty to overwrite with `thllanguage`.

### Target:
The Hotline chat widget has different targets based on general purpose of the interaction. We will work with you and your intended use to determine which target to use.
 * Focused on helping those in crisis. = `thl` (default)
 * Focused on providing education on healthy relationships. = `lir`
 * `thltarget=lir`

### Chat Now button:
By default, a “Chat Now” button is added to the bottom-right corner of every web page that the endpoint is loaded from if a custom button is not found.
 * Enabled = `thlchatbtn=true` (default)
 * Disabled = `thlchatbtn=false`
  
### Exit Site button:
By default, a red exit button will appear on the top-left corner of the chat frame. This is a safety feature that allows chatters to quickly leave the entire website. We will work with you to determine if disabling this button is allowed.
 * Enabled = `thlexitbtn=true` (default)
 * Disabled = `thlexitbtn=false`


## Logging

### Source: 
This is configurable using a query string. This will accept standard letters, digits, and hyphens and is limited to 255 characters.
 * `thlsource={{basically anything you want}}`
 * `thlsource=course-dating-safety`
 * `thlsource=chatter-type-conversation-type-marketing-effort-website-journey-footer-or-header-time-on-site-anything`

### Page-URL:
This isn’t a configurable setting. This simply captures the entire page-URL.
 * `https://my-app.com/courses/dating-safety/spring-23/index.html?myParameter=myValue&thltarget=lir`




## Deploy widget
Depending on your desired development approach, you can simply point to your custom endpoint or add the following script snippet to every page in your website or application.
A WordPress plugin is in development.

`<script type="text/javascript" src="{{your_custom_endpoint}}" charset="utf-8"></script>`

By default, a button that says “Need help? Chat now.” and is styled according to The Hotline branding. This default behavior is exhibited on this page.


## Examples

Pure endpoint-URL configs
 * `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9`
 * `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9&thllanguage=es&thltarget=lir&thlsource=course-dating-safety-spring-23`

Endpoint-URL and page-URL config
 * `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9`
 * `https://my-app.com/courses/safe-dating/spring-2023/index.html?myParameter=myValue&thltarget=lir&thllanguage`

## If you want to use a custom button
Simply set the id or name attribute of the custom button to `thl-messaging-btn` and the endpoint / script tag above will initiate a chat when the custom button is clicked.

 * `id="thl-messaging-btn"`
 * `name="thl-messaging-btn"`
 * i.e. `<button class="my-button-class chat-button" id="footer-btn-1" name="thl-messaging-btn">Chat Now</button>`
 * If you’re using a custom button and you want to disable the default button from showing up on pages there isn’t a custom chat button, include the query string `thlchatbtn=false`.




## Manage and request keys
Contact the integration team to manage your integration or request a key.
 * **https://www.thehotline.org/partner-with-thehotline**
