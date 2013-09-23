## Info

Help to deliver emoji enabled remote push notification to APNs . 

## Usage 

### Code Part

```php
	include('emoji.php');

	$message = emoji_replace( $_POST['message'] );

	$payload  = array(
					'aps' => array(
		                'alert' => $message, 
		                'badge' => 1,
		                'sound' => "default"
		            ));

	// ... and the rest of the code to communicate with APNS
```

### Composing Message Part

First: Select the emoji you want to send  http://code.iamcal.com/php/emoji/ 

Seleting by Copy the name , like "black sun with rays" , and put it between ":" like ->  ":black sun with rays:". 

Below is an example : 

```php
	include('emoji.php');

	$message = emoji_replace("Have a nice Day. :black sun with rays:");

	$payload  = array(
					'aps' => array(
		                'alert' => $message, 
		                'badge' => 1,
		                'sound' => "default"
		            ));

	// ... and the rest of the code to communicate with APNS
```

