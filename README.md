# ga-ecommerce-tracking-php
Use for Google Analytics ecommerce conversion tracking. Create a server side hit using the measurement protocol via PHP.

Designed for but not limited to PayPal conversion tracking in Google Analytics.
You can use as an alternative to client side ecommerce conversion tracking e.g tag manager, which is unreliable for PayPal due to the customer not always returning to the site after making payment.

Either implement on PayPal IPN script (as this always get called), or use Zapier (https://zapier.com) to call it when a successful order is placed.
