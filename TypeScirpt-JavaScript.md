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

### Zig Zag Sequence

***Question:*** [See Question Here](https://www.hackerrank.com/challenges/one-week-preparation-kit-zig-zag-sequence/problem?isFullScreen=true&h_l=interview&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-three)

***Answer:***

`// todo : this answer needs simplifying`

```
    let alpha = 'abcdefghijklmnopqrstuvwxyz'; 
    let res = '';
 
    for(let i = 0; i < s.length; i++){      
      let indexOfChar = alpha.search(new RegExp(s[i], "i"));
      let isCap = false;
      
      if(s[i] === s[i].toUpperCase()){
        isCap = true;
      }     
      
      if(indexOfChar === -1){
         res = res + s[i];
      } else {          
          if((indexOfChar + k) > 26){
            let newIndex = ((indexOfChar + k) - 26);
        
            if(newIndex <= 26){               
              isCap ? res = res + alpha[newIndex].toUpperCase() : res = res + alpha[newIndex];
            } else {
              // go round again ...
            }
        } else {
          isCap ? res = res + alpha[(indexOfChar + k)].toUpperCase() : res = res + alpha[(indexOfChar + k)];
        }        
      }        
    }
    
    return res;
```
