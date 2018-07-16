# Simple PHP class to BitBay REST API

## Usage

The BitBayAPI constructor receive public and private key using to authentication. 
```php
<?php

require_once('BitbayApi.class.php');

$api = mew bitbayAPI('1c990eb1-fab5-4890-98fd-3ec4bf185254', 'dd607870-a151-4ffa-a57b-a0c4b70dded3');

$api->callApi('');
```
### Create offer

```php
$params = array(
        "amount" => $amount,
        "rate"=> $rate,
        "price"=> null,     
        "offerType"=> $type,
        "mode" => "limit",
        "postOnly"=> null,
        "hidden"=> $hidden,
        "fillOrKill"=> null               
);
    
$method = "trading/offer/BTC-PLN";
return $api->callApi($method,$params,'POST');
```
