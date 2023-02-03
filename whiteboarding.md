Question #1: Turning Strings to URLs

URLs cannot have spaces. Instead, all spaces in a string are replaced with %20. Write an algorithm that replaces all spaces in a string with %20.

You may not use the replace() method or regular expressions to solve this problem. Solve the problem with and without recursion.
Example

Input: "Jasmine Ann Jones"

Output: "Jasmine%20Ann%20Jones"

let input = "Jasmine Ann Jones"
Working:
function stringToUrl(input) {
  let arr = input.split(" ");
  let arrOut =  arr.join("%20");
  return arrOut
}

OG:
function stringToUrl(input){
  let arr = input.split(" ");
  for (let i = 1; i < arr.length; i += 2) {
    arr.splice(i, 0, "%20");
  }
  let outUrl = arr.toString()
  outUrl = outUrl.replaceAll(',' , '')
  return outUrl;
}

Recursive:
function recursive(input){
  if (successful){
    return 
  } else {
    recursive();
  }
}

=============================================================================================


Question #2: Array Deduping

Write an algorithm that removes duplicates from an array. Do not use a function like filter() to solve this. Once you have solved the problem, demonstrate how it can be solved with filter(). Solve the problem with and without recursion.
Example
Input: [7, 9, "hi", 12, "hi", 7, 53]
Output: [7, 9, "hi", 12, 53]

without filter()
input = [7, 9, "hi", 12, "hi", 7, 53]

//works, but will push empty values
function deDupe(input){
  input.sort();
  let check = [];
  
  for (let i=0; i<input.length; i++){
    if (input[i] != input [i+1])
    check[i] = input[i]
  }
  return check;
}

//cleaner & faster! arguably faster with a forEach()?
function deDupe2(input){
  let uniqueSet = new Set();
  for (let i=0; i<input.length; i++){
    uniqueSet.add(input[i])
  }
  return uniqueSet;
}



=============================================================================================
Question #3: Compressing Strings

Write an algorithm that takes a string with repeated characters and compresses them, using a number to show how many times the repeated character has been compressed. For instance, aaa would be written as 3a. Solve the problem with and without recursion.
Example

Input: "aaabccdddda"
Output: "3ab2c4da"
let input = "aaabccdddda"

function compress(input){
  input.sort();
  let out = ""
  for (int i=0; i<input.length; i++){
    let count = 1;
    while (i < input.length - 1 && input[i] === input[i + 1]){
      count++;
      i++;
    }
    if ( count === 1){
      out.concat(input[i]);
    } else {
      out.concat(count)
      out.concat(input[i])
    }
  }
  return out;
}


        }
        else
        {
          cout << str[i] << count;
        }
         
    } 
} 

=============================================================================================
Question #4: Checking for Uniqueness

Write an algorithm that determines whether all the elements in a string are unique. You may not convert the string into an array or use array methods to solve this problem. The algorithm should return a boolean.
Example

Input: "hello"

Output: false

Input: "copyright"

Output: true

=============================================================================================
Question #5: Array Sorting

Write an algorithm that sorts an array without using the sort() method. There are many different sorting algorithms — take the time to read about the following:

    Quick sort
    Merge sort
    Heap sort
    Insertion sort
    Bubble sort
    Selection sort

You may implement any of the above algorithms (or your own) to solve the problem — as long as it doesn't use sort().
Example

Input: [9, 2, 7, 12]

Output: [2, 7, 9, 12]