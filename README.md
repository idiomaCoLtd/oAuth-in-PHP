oAuth authorization in PHP
==========================

oAuth authorization for PHP. Full OAuth 1.0 protocol specification you can see at http://trac.tools.ietf.org/html/rfc584.

Basic usuage
============
  
    $consumer_key = "...";
    $consumer_secret = "...";
    $token_key = "...";
    $token_secret = "...";
  
	$this->signatureMethod = new OAuthSignatureMethod_HMAC_SHA1();
	$this->consumer = new OAuthConsumer($consumer_key, $consumer_secret);
	
	if (!is_null($token_key))
		$this->token = $this->setToken($token_key, $token_secret);
	else
		$this->token = null;

