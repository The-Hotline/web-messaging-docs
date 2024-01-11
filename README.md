# The Hotline chat widget integration instructions


### Base endpoint URL
`http://chat.thehotline.us/p/24-1/thl-messaging.js`

### Live Demo
Basic configuration
 * https://chat.thehotline.us/p/24-1/demo.html

Spanish deployment
 * Include `thllanguage=es` in the endpoint.
 * `{{base_endpoint}}?key=44033576-e28e-8685-2b21-58sample3d9&thllanguage=es`

Scope / target
 * To determine inquiries focused on domestic violence crisis support or health relationship inquiries.
 * `thltarget=thl` = The Hotline: Primary scope, domestic violence crisis support.
 * `thltarget=lir` = Love Is Respect: Health relationship inquiries.
 * `{{base_endpoint}}?key=44033576-e28e-8685-2b21-58sample3d9&thltarget=thl`

Auto load
 * To automatically load a new session when the page loads, update your endpoint to include `thlautoload=yes`
 * `{{base_endpoint}}?key=44033576-e28e-8685-2b21-58sample3d9&thlautoload=yes`

## Basic Deployment
Use this endpoint in your custom implementation:
 * `{{base_endpoint}}?key=44033576-e28e-8685-2b21-58sample3d9`
or paste this snippet into the end of your <body></body> in every page you want a chat to be able to start and continue/reconnect.
 * `<script type="text/javascript" src="{{base_endpoint}}?key=44033576-e28e-8685-2b21-58sample3d9" charset="utf-8"></script>`

### Deployment key: 'key' (required)
Your unique deployment key. This is the only query string that must be declared in the endpoint-URL. It will not be obtained from the page-URL.
 * `key=44033576-e28e-8685-2b21-58sample3d9`

### Approved Domains (requried)
Each unique deploy key is connected to a list of approved domains. We will build an interface for this as we add more partners.
 * For now, connect with us via email to add, remove, or see a list of approved domains.

## Custom Deployment
The following configurations are all optional.

### To use a custom button
Set the id or name attribute of the custom button to begin with `thl-messaging-btn` and the endpoint / script tag above will initiate a chat when the custom button is clicked.

 * `id="thl-messaging-btn"`
 * `id="thl-messaging-btn-footer"`
 * `name="thl-messaging-btn"`
 * i.e. `<button class="my-button-class chat-button" id="thl-messaging-btn">Chat Now</button>`
 * i.e. `<button class="my-button-class chat-button" id="header-chat-btn" name="thl-messaging-btn">Chat</button>`
 * i.e. `<button class="my-button-class chat-button" id="footer-chat-btn" name="thl-messaging-btn-footer">Chat with TheHotline.org</button>`
