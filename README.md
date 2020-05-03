PHP visitors tracking system
99% accurate visitors tracking system for PHP >= 7.0

composer require ghostff/php-visitors-tracking
USAGE
$visitor = new VisitorTracking;

$visitor->ip; //outputs clients IP address

$visitor->browser->name; //outputs clients Browser name
$visitor->browser->version; //outputs clients Browser version
$visitor->browser->OS; //outputs clients Operating system

$visitor->continent; //outputs clients continent name
$visitor->continent_code; //outputs continent code
$visitor->country; //outputs clients country name
$visitor->country_code; //outputs clients country code
$visitor->state; //outputs clients region name
$visitor->state_code; //outputs clients region code
$visitor->city; //outputs clients city
$visitor->postal_code; //outputs clients postal code
$visitor->metro_code; //outputs clients metro code
$visitor->latitude; //outputs clients latitude
$visitor->longitude; //outputs clients longitude
$visitor->timezone; //outputs clients timezone
$visitor->datetime; //outputs clients datetime
Initializer __constructor(?Closure $on_fail, ?string $ip)
$on_fail: A callback function that will be called if error occurred with IP data query.
$ip : An explicit IP.
new VisitorTracking(function (string $error) {
    var_dump($error);
});
Initializer __toArray()
Returns array of all user properties.

$visitor = new VisitorTracking(null, '85.13.6.242');
var_dump($visitor->__toArray());
