Bigstock API Client
===================

PHP Client for interacting with the Bigstockphoto API.

This library contains a few simple functions to easily perform search, detail, purchase and download of images. Initialize the library with your API ID and Secret Key, then set production or test mode.


**Initialization**

    $config = array(
	'account_id'=>123456, 
	'secret_key'=>'secret key'
	);

    $bigstock_api = new BspApi($config);

**setTestMode()**
Set to test mode to use the test API end point.

**setProdMode()**
Set to production mode to use the standard API.

**search( $params )**
Perform a search using the parameters passed. Valid parameters are listed in the documentation http://help.bigstockphoto.com/entries/20843622-api-overview.

**image( $image_id )**
Retrieve information about a single image based on image ID.

**purchase( $image_id, $size_code )**
Purchase a license for an image using the image ID and the size to be purchased. The authorization key is automatically generated and submitted to the API. Response will contain a download ID that can be used for downloading the licensed image.

**getDownloadUrl( $download_id )**
Get the download URL of the licensed image based on the download ID returned by the purchase function.

