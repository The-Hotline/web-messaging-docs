# The Hotline chat widget integration instructions


## Base endpoint URL
`http://chat.thehotline.us/thl-messaging.js`

## Live Demo
https://chat.thehotline.us/demo.html


## Basic Deployment

### Basic deployment example
 * Use this endpoint in your custom implementation: `https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9`
 * or
 * Paste this snippet into the end of your <body></body> in every page you want chat to be able to continue. `<script type="text/javascript" src="https://chat.thehotline.us/thl-messaging.js?key=44033576-e28e-8685-2b21-58sample3d9" charset="utf-8"></script>`

### Deployment info
A WordPress plugin is in development.



## Configure Deployment

### To use a custom button
Set the id or name attribute of the custom button to begin with `thl-messaging-btn` and the endpoint / script tag above will initiate a chat when the custom button is clicked.

 * `id="thl-messaging-btn"`
 * `id="thl-messaging-btn-footer"`
 * `name="thl-messaging-btn"`
 * i.e. `<button class="my-button-class chat-button" id="thl-messaging-btn">Chat Now</button>`
 * i.e. `<button class="my-button-class chat-button" id="header-chat-btn" name="thl-messaging-btn">Chat</button>`
 * i.e. `<button class="my-button-class chat-button" id="footer-chat-btn" name="thl-messaging-btn-footer">Chat with TheHotline.org</button>`

### Query strings
Functionality is configured by query string parameters. Query strings are obtained from the endpoint-URL for the widgeth and from the page-URL of the webpage laoding the widget. If present, page-URL query strings will override those in the endpoint. (i.e. `endpoint-URL:?thllanguage=en` and `page-URL:?thllanguage=es` In this example, the language for the whole site is set to English, but when visiting a Spanish page, the page-URL will be the setting that is resolved)

If a desired configuration is the default, it can be omitted from both URLs.

### Button parameters
This is under development. Pass use-specific parameters to the chat via button attributes.


### Options

#### Deployment key: 'key' (required)
Your unique deployment key.
 * This is the only query string that must be declared in the endpoint-URL. It will not be obtained from the page-URL.
 * `key=44033576-e28e-8685-2b21-58sample3d9`

#### Chat Now button:
By default, if a custom button is not found, a “Need help? Chat now” button is added to the bottom-right corner of every web page that the endpoint is loaded in. This can be disabled.
 * Enabled = `thlchatbtn=true` (default) [DEMO](https://chat.thehotline.us/demo.html) 
 * Disabled = `thlchatbtn=false` [DEMO](https://chat.thehotline.us/demo-custom-button.html)

#### Language: 
 * English = `en` (default)
 * Espanol = `es`
 * `thllanguage=es`
 * In development: `language=es` and `lang=es`. These common language delcarations can be leveraged - with the abilty to overwrite with `thllanguage`.

#### Target:
The Hotline chat widget has different targets based on general purpose of the interaction. We will work with you and your intended use to determine which target to use.
 * Focused on helping those in crisis. = `thl` (default)
 * Focused on providing education on healthy relationships. = `lir`
 * `thltarget=lir`
  
#### Exit Site button:
By default, a red exit button will appear on the top-left corner of the chat frame. This is a safety feature that allows chatters to quickly leave the entire website. Please let us know if you intend to disable this button.
 * Enabled = `thlexitbtn=true` (default)
 * Disabled = `thlexitbtn=false`


### Logging
Reporting for logs is in development.

#### Source: 
This is configurable using a query string. This will accept standard letters, digits, and hyphens and is limited to 255 characters.
 * `thlsource={{basically anything you want}}`
 * `thlsource=course-dating-safety`
 * `thlsource=chatter-type-conversation-type-marketing-effort-website-journey-footer-or-header-time-on-site-anything`

#### Page-URL:
This isn’t a configurable setting. This simply captures the entire page-URL.
 * `https://my-app.com/courses/dating-safety/spring-23/index.html?myParameter=myValue`
 * `https://my-app.com/app.html?course=dating-safety&term=spring-23&myParameter=myValue`


## Demo
Default config
 * https://chat.thehotline.us/demo.html
 
Custom button
 * https://chat.thehotline.us/demo-custom-button.html

Exit button omitted and a Spanish deployment
 * https://chat.thehotline.us/demo.html?thlexitbtn=false&lang=es


## Manage and request keys
Contact the integration team to manage your integration or request a key.
 * **https://www.thehotline.org/partner-with-the-hotline**
