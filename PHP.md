
# TypeScirpt-JavaScript Challenges

## Basic 

### Recursive Digit Sum 

***Question:*** [See Question Here](https://www.hackerrank.com/challenges/one-week-preparation-kit-recursive-digit-sum/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-four)

***Answer:***

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
