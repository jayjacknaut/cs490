//   cs490  middle part

<?php

$data = array(
               'username' = urlencode($username),
               'password' = urlencode($passwd),
              );
$ch = curl_init($url);
$payload = json_encode(array("user" =$data));

curl_setopt ($ch, CURLOPT_POSTFIELDS,$payload);
curl_setopt ($ch, CURLOPT_CUSTOMERQUEST, "POST");
curl_setopt ($ch, CURLOPT_HTTPHEADER, array());

curl_setopt ($ch, CURLOPT_ RETURNTRANSFER, true);

$result = curl_exec($ch);

curl_close($ch);
