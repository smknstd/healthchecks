# PHP

Below is an example of making a HTTP request to SITE_NAME from PHP.

```php
file_get_contents('https://hc-ping.com/your-uuid-here');
```

If you'd like to setup timeout and retry options, as discussed in the [reliability tips section](../reliability_tips/), there is a [curl package](https://www.phpcurlclass.com/) available that lets you do that easily:

```php
use Curl\Curl;

$curl = new Curl();
$curl->setRetry(20);
$curl->setTimeout(5);
$curl->get('https://hc-ping.com/your-uuid-here');  
```

Note: this code never throws any exception.
