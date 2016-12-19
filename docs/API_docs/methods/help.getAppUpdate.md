## Method: help.getAppUpdate  

### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|


### Return type: [help\_AppUpdate](../types/help\_AppUpdate.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) {
    $this->bot_login($token);
}
if (isset($number)) {
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$help_AppUpdate = $MadelineProto->help->getAppUpdate();
```