# JAVASCRIPT LEARNINGS
Learnings of everyday JS problems, tips-tricks, challenges..

# TABLE OF CONTENTS

// 1. Return true if any of the number contains 0 from the array. [321, 123] = false, [11, 90] = true, [109] = true, [0] = true.
function checkZero(arr) {
  const status = false;
  arr.map(ele => {
    const output = ele.toString().split('').indexOf('0');
    if(output !== -1) {
      status = true
    }
  })
  return status;
}
let input1 = [123,253,2325]
let output1 = checkZero(input1)
console.log(output1);


// 2. Find second occurrence of second letter. Uttam = 2, Panchal = 5, Angular = -1.
function getSecondOccurence(string) {
  const secondChar = string.split('')[1];
  const firstIndex = string.split('').indexOf(secondChar);
  const lastIndexOf = string.split('').lastIndexOf(secondChar);

  if(firstIndex === lastIndexOf) {
    return -1;
  } else {
    return lastIndexOf;
  }
}
let input2 = 'Uttam';
let output2 = getSecondOccurence(input2);
console.log(output2);
