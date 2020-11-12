## Algorithms
Some algorithms solutions made by me, send challenges to msaatkamp@hotmail.com

Waiting for new challenges.


<details>
  <summary># Efficient Vineet</summary>
  This code should receive an array of numbers, that can be sorted in 3 groups, with a maximum result of 3, each.
  For example, calling main([1.5, 1.5, 1.5, 1.5, 1.5]) should result in an array like [3, 3, 1.5]
  
  latest code: 

    function main(array) {
      const takeBags = (input) => {
          const carryBags = []
          input.sort((a, b) => a - b)
          let i = 0;
          while (input.length > 0) {
              carryBags.push(input.pop())

              let j = input.length;
              while (j >= 0) {
                  if (input[j] && (carryBags[i] + input[j] <= 3)) {
                      carryBags[i] = carryBags[i] + input.splice(j, 1)[0]
                  }
                  j--;
              }
              i++;
          }
          if (carryBags > 3) takeBags(carryBags)
          return carryBags;
        }
        console.log(takeBags(array))
    }
  


</details>


