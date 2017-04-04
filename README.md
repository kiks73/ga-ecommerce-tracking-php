# ga-ecommerce-tracking-php
Use for Google Analytics ecommerce conversion tracking. Create a server side hit using the measurement protocol via PHP.

Designed for but not limited to PayPal conversion tracking in Google Analytics.
You can use as an alternative to client side ecommerce conversion tracking e.g tag manager, which is unreliable for PayPal due to the customer not always returning to the site after making payment.

Either implement on PayPal IPN script (as this always get called), or use Zapier (https://zapier.com) to call it when a successful order is placed.

```php
<?php
require_once 'ga-ecommerce-tracking.php';

$ga_ecommerce = new ga_ecommerce_tracking( 'UA-XXXXXXXX-X', 'Test Order', false );

$order_arr = array(
  // transaction id
  'ti'=>'1234',
  
  // affiliation
  'ta'=>'Test',
   
  // revenue
  'tr'=>100.00,
   
  // tax
  'tt'=>20.00,
   
  // shipping
  'ts'=>0,
   
  // prod action
  'pa'=>'purchase',
   
  // prod 1 id
  'pr1id'=>'ABC123',
   
  // prod 1 name
  'pr1nm'=>'TEST PROD',
   
  // prod 1 cat
  'pr1ca'=>'TEST CAT'			   
);

$ga_ecommerce->send_hit( $order_arr );
?>
```
