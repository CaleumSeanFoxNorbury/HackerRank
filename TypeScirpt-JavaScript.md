# TypeScirpt-JavaScript Challenges

## Basic 

### Lonely Integer

***Question:*** [See Question Here](https://www.hackerrank.com/challenges/one-week-preparation-kit-lonely-integer/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-two)

***Answer:***

```
    return a.filter((x:number) => a.filter((y: number) => x ===y).length === 1)[0];
```

### Diagonal Difference

***Question:*** [See Question Here](https://www.hackerrank.com/challenges/one-week-preparation-kit-diagonal-difference/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-two&h_r=next-challenge&h_v=zen)

***Answer:***

```
    let a: number[] = [];
    let b: number[] = [];
    arr.forEach((x: number[], ix: number) => {
        
        x.forEach((y: number, iy: number) => {
            if(ix === iy){
                a.push(arr[ix][iy]);                
            }        
            
            if(b.indexOf(arr[ix][((arr.length - 1) - ix)]) < 0){
                b.push(arr[ix][((arr.length - 1) - ix)])                
                
            }
        });
    });
    
    let resA = a.reduce((partialSum, a) => partialSum + a, 0) 
    let resB = b.reduce((partialSum, a) => partialSum + a, 0);
    
    if(resA > resB){
        return resA - resB;
    } else {
        return resB - resA;
    }    
```

