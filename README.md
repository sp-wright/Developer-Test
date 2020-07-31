# Limesharp Developer Test

Please, **don't fork this repo**, clone it or download it locally and then commit changes after each task into a new repo of your own, and send us the link. We will get back to you shortly.

Languages accepted: Javascript or PHP.

### Task 1:

Make this work (repeat 3 times the contents of an array):

```javascript
repeat([1, 2, 3]); //[1,2,3,1,2,3,1,2,3]
```

Your solution:

```
const repeat = (arr) => {

//set function scoped variables
//set the number of repeats
const repeats = 3
const repeatedArr = []

      //iterate a for loop for the number of repeats
      for (let i = 0; i < repeats; i++){
          //push the array to the repeated arr
          repeatedArr.push(...arr);
      }

      //return the repeated array
      return repeatedArr;

};
repeat([1,2,3]);
```

###### If we type in our console your function and repeat([1,2,3]) then the result should be [1,2,3,1,2,3,1,2,3]

### Task 2:

Make this work (no vowels, lowercase except the first letter):

```javascript
reformat('liMeSHArp DeveLoper TEST'); //Lmshrp dvlpr tst
```

Your solution:

```
const reformat = (str) => {
    //set array of vowels and other function scoped variables
    const vowels = ['a', 'e', 'i', 'o', 'u'];
    let firstChar = true;
    let outputString = '';

    //convert the string lowercase and split it into array of substrings
    splitStr = str.toLowerCase().split('');

    //map over the array of single characters
    splitStr.map((char) => {
        //uses the vowel array to check it is not a vowel
        if (!vowels.some(v => char === v)){
            //if it is the first character it capitalises the character else it outputs the string
            if (firstChar){
                outputString = `${outputString}${char.toUpperCase()}`;
                firstChar = false;
            }else {
                 outputString = `${outputString}${char}`;
            };
        };
    });

    //return the string
    return outputString;

};
reformat('liMeSHArp DeveLoper TEST');

```

###### If we type in our console your function and reformat("liMeSHArp DeveLoper TEST") then the result should be Lmshrp dvlpr tst

### Task 3 (optional, for bonus points):

Make this work (without using any built in functions, only a `for` loop, return the next binary number in a string or as an array)

```javascript
next_binary_number([1, 0]); // [1,1]

// possible test cases:
// [1,0] => [1,1]
// [1,1] => [1,0,0]
// [1,1,0] => [1,1,1]
// .......
// [1,0,0,0,0,0,0,0,0,1] => [1,0,0,0,0,0,0,0,1,0]
```

Your solution:

###### If we type in our console your function and next_binary_number([1,0,0,0,0,0,0,0,0,1]) then the result should look like 1,0,0,0,0,0,0,0,1,0 (or as an array).

---

If you get invited to the first interview read the "What to expect.md" file.
