#[6 kyu] Triple trouble
```
function tripledouble(num1, num2) {
  //code me
  
  const reg = /(\w)\1+/ig
  let filter_string_nums1 = num1.toString().match(reg)||[]
  let filter_string_nums2 = num2.toString().match(reg)||[]
  let istripledouble = 0
  filter_string_nums1.map(item1 => {
      filter_string_nums2.map(item2 => {
        if((item1.search(item2) != -1 ||item2.search(item1) != -1)&&(item1.length>2||item2.length>2)){
          console.log('item1',item1,'item2',item2)
          istripledouble = 1
        }
      })
  })
  return istripledouble
}
```

#[6 kyu] Write Number in Expanded Form
```
function expandedForm(num) {
  // Your code here
  let final_str = num.toString()
  return final_str.split('').map((item,index) => {
    if(item>0){
      let pow = Math.pow(10,final_str.length-index-1)
      return item*pow
    }
  }).filter(i => i).join(' + ')
}
```

# [6 kyu] CamelCase Method

```
String.prototype.camelCase=function(){
  //your code here
  return this.replace(/\b\w+\b/g,(string) => string.substring(0,1).toUpperCase()+string.substring(1)).replace(/\s+/g,"")
}
```

# [6 kyu] Reversed Words

```
function reverseWords(str){
  str = str.split(" ").reverse().join(" ")
  return str; // reverse those words
}
```

# [6 kyu] Replace With Alphabet Position

```
function alphabetPosition(text) {
  var array = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"];
  var result = [];
  for(i in text){
    var c = text[i];
    var index = array.indexOf(c.toLowerCase()) + 1;
    if (index != 0) result.push(index.toString());
    
  }
  return result.join(' ');
}
```

## [5 kyu] Where my anagrams at?
```
function anagrams(word, words) {
  return words.filter(item => word.split("").sort().join("") === item.split("").sort().join(""))
}
```
## [6 kyu] Find the missing term in an Arithmetic Progression
```

```


