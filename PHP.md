

```
    if($n <= 9){
        return $n;
    }
    
    $finalStr = '';
    for($i = 0; $i < $k; $i++){
        $finalStr = $finalStr.($nStr = strval($n));        
    }
    
    
    $response = addUpNumbers($finalStr);
    while($response > 9){
        $response = addUpNumbers($response);
    }
    
    return $response;
```
