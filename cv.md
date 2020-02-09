# EUGENE BERTOSH
![My photo](/img/P7ecLMFydl8.jpg)
## About me
I am 20 years old. I'm currently study at the Belarusian State University.
My speciality is web programming and internet technologies and I am a part - time third - year student.
I can describe myself as an energetic, responsible, creative and highly - motivated person.
My major strength is the ability to work under pressure. I can deal with difficult situations.
## PROFESSIONAL SKILLS
Programming languages:
* C++ (Medium: good theoretical knowledge, practical skills)
* Java (Medium: good theoretical knowledge, practical skills)
* JavaScript (Medium: good theoretical knowledge, practical skills)
* PHP (Medium: good theoretical knowledge, practical skills)
## AND:
* HTML (Great: good theoretical knowledge, practical skills)
* CSS (Great: good theoretical knowledge, practical skills)
## LANGUAGES:
* English (B1)
* Polish (B1)
## PERSONAL SKILLS:
1. Analytical thinking
2. Hardworking
3. Ability to work efficiently both individually and in a team
4. Quick learning
5. Attentive
6. Responsible
7. Pedantic
## CODE EXAMPLE
#### Advanced zeros
The get Errors Count function, which takes
any integer (1 <= number <= 10^7) as the first argument and any
integer base (2 <= base <= 256) as the second argument.
She needs to count the number of trailing zeros in the number,
the factorial of a number in base system.
```javascript
module.exports = function getZerosCount(number, base) {
                                let factorials = [];
                                let k = 2;
                                while(k < base) {
                                  while (base % k === 0 ){
                                    factorials.push(k);
                                    base /= k;
                                  }
                                  k++;
                                }
                                if (base > 1) {
                                  factorials.push(base);
                                }
                                factorials.sort((a, b) => a - b);
                                let zeros = [];
                                let count = 1;
                                for (let i = 0; i < factorials.length; i+= count){
                                  let counter = 0;
                                  for(let j = i; j <factorials.length; j++) {
                                    if (factorials[i] === factorials[j]){
                                      counter++;
                                    } else {
                                      count = counter;
                                      break;
                                    }
                                  }
                                  let result = 0;
                                  let j = factorials[i];
                                  while (true) {
                                    result += (number - number % j)/ j;
                                    j *= factorials[i];
                                    if (j > number){
                                      break;
                                    }
                                  }
                                  zeros.push((result - result % counter) / counter);
                                }
                                return Math.min.apply(Math, zeros)
                               }
```
#### Money Exchange
The make Exchange method,
which determines the minimum number of coins required to make
changes to a given amount in us currency.
```javascript
                             module.exports = function makeExchange(currency) {
                                if(currency > 10000) return {error: "You are rich, my friend! We don't have so much coins for exchange"};
                                if(currency <= 0) return {};
                                var h = Math.floor(currency / 50);
                                var currency = currency % 50;
                             	var q = Math.floor(currency / 25);
                             	var currency = currency % 25;
                             	var d = Math.floor(currency / 10);
                             	var currency = currency % 10;
                             	var n = Math.floor(currency / 5);
                             	var currency =currency % 5;
                             	var p = currency;
                             	var result = {};
                             if (h > 0) result["H"] = h;
                             if (q > 0) result["Q"] = q;
                             if (d > 0) result["D"] = d;
                             if (n > 0) result["N"] = n;
                             if (p > 0) result["P"] = p;
                             return result;

                            }
```
## PERSONAL INFORMATION
###### Email: betoshevgieniy@gmail.com
###### Tel: +375297965686