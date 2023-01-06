# The Hotline chat widget integration instructions

#### Please do not finalize your implementation until keys have been obtained.
Some minor details below may change in the final stages of development.

## Base endpoint URL
`http://chat.thehotline.us/thl-messaging.js`



## Configure widget

### Query strings
Query strings are obtained from the endpoint-URL or the URL of the page the widget is loading from. If present, page-URL query strings will override those in the endpoint. If a desired configuration is the default, it can be omitted from both URLs.

### Button parameters
This is under development. Pass use-specific parameters to the chat via button attributes.



## Functionality

### Deployment key: 'key' (required)
Your unique deployment key.
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
By default, a “Need help? Chat now” button is added to the bottom-right corner of every web page that the endpoint is loaded from if a custom button is not found. This can be disabled.
 * Enabled = `thlchatbtn=true` (default)
 * Disabled = `thlchatbtn=false`
  
### Exit Site button:
By default, a red exit button will appear on the top-left corner of the chat frame. This is a safety feature that allows chatters to quickly leave the entire website. Please let us know if you intend to disable this button.
 * Enabled = `thlexitbtn=true` (default)
 * Disabled = `thlexitbtn=false`


## Logging
Reporting for logs is in development.

### Source: 
This is configurable using a query string. This will accept standard letters, digits, and hyphens and is limited to 255 characters.
 * `thlsource={{basically anything you want}}`
 * `thlsource=course-dating-safety`
 * `thlsource=chatter-type-conversation-type-marketing-effort-website-journey-footer-or-header-time-on-site-anything`

### Page-URL:
This isn’t a configurable setting. This simply captures the entire page-URL.
 * `https://my-app.com/courses/dating-safety/spring-23/index.html?myParameter=myValue`
 * `https://my-app.com/app.html?course=dating-safety&term=spring-23&myParameter=myValue`




## Deploy widget
Add the following script snippet to the end of the body tag.

`<script type="text/javascript" src="{{my_custom_endpoint}}" charset="utf-8" thl-chat></script>`

--

Depending on the application's architecture:

Use the same endpoint for the entire app and customize button behavior via button_attributes/page_urls or modify/include the endpoint page-by-page.

By default, a button is embedded in the bottom right corner of each page that says “Need help? Chat now.” and is styled according to The Hotline branding. This default behavior is demonstrated at https://chat.thehotline.us/demo.html. A custom button deployment demo can be found at https://chat.thehotline.us/demo-custom-button.html.

A WordPress plugin is in development.

## Examples

Pure endpoint-URL configs
 * `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9`
 * `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9&thllanguage=es&thltarget=lir&thlsource=course-dating-safety-spring-23`

Endpoint-URL and page-URL config
 * `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9`
 * `https://my-app.com/courses/safe-dating/spring-2023/app.html?myParameter=myValue&thltarget=lir`

## To use a custom button
Set the id or name attribute of the custom button to begin with `thl-messaging-btn` and the endpoint / script tag above will initiate a chat when the custom button is clicked.

 * `id="thl-messaging-btn"`
 * `id="thl-messaging-btn-footer"`
 * `name="thl-messaging-btn"`
 * i.e. `<button class="my-button-class chat-button" id="thl-messaging-btn">Chat Now</button>`
 * i.e. `<button class="my-button-class chat-button" id="header-chat-btn" name="thl-messaging-btn">Chat</button>`
 * i.e. `<button class="my-button-class chat-button" id="footer-chat-btn" name="thl-messaging-btn-footer">Chat with TheHotline.org</button>`



## Demo
Default config
 * https://chat.thehotline.us/demo.html

Custom button
 * https://chat.thehotline.us/demo-custom-button.html

Default button, in spanish, without a close button
 * https://chat.thehotline.us/demo.html?thllanguage=es&thlexitbtn=false

## Manage and request keys
Contact the integration team to manage your integration or request a key.
 * **https://www.thehotline.org/partner-with-the-hotline**
