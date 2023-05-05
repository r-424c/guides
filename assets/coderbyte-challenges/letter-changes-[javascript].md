
Mia:
```js
function StringChallenge(str = '') { 

  str = str.toLocaleLowerCase()
  const letters = Array.from('abcdefghijklmnopqrstuvwxyz')
  const vowels = Array.from('aeiou')

  const result = Array.from(str).map( (character) => {
    const letterFound = letters.findIndex(letter => letter === character)
    if (letterFound >= 0) {
      const letterTarget = (letters.length === letterFound+1 ) ? 0 : letterFound+1
      const charResult = letters[letterTarget]
      const vowelFound = vowels.findIndex(vowel => vowel === charResult)
      if (vowelFound >= 0) {
        return vowels[vowelFound].toUpperCase()
      }
      return charResult;
    }
    return character;
  })

  return result.join(''); 
}
   
// keep this function call here 
console.log(StringChallenge(readline()));
```

alternative: 
```js
function LetterChanges(str) { 

  let shift = str.replace(/[a-z]/gi, function(letter) {
      return (['z','Z'].includes(letter)) ? 'a' : String.fromCharCode(letter.charCodeAt() + 1);
  });
  let answer = shift.replace(/a|e|i|o|u/gi, function(letter) {
      return letter.toUpperCase();
  })
  return answer; 
         
}
```

otras: https://coderbyte.com/solution/Letter%20Changes