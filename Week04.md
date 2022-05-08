# Thursday
```javascript
function stringClean(s){
  //replace each number that it's in the range 0-9
  let result= s.replace(/[0-9]/g, "")
  return result
  // Function will return the cleaned string
}

```

```javascript
function getNumberFromString(s) {
  //replace all characters different from 0-9
  let n=s.replace(/[^0-9]+/g, '')
  return Number(n);
}
```

```javascript
function validate(password) {
  // ^ starts 
  //(?=.*\d) has at least 1 numeric char
  //(?=.*[a-z]) has at least 1 lowercase
  //(?=.*[A-Z]) has at least 1 uppercase
  //[0-9a-zA-Z]{6,} should have at least 6 chars from this range
  const regexValidation= /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])[0-9a-zA-Z]{6,}$/
  
  return regexValidation.test(password);
}
```

```javascript
function validateUsr(username) {
  // 0-9 or a-z or _ allowed and length between 4 and 16
  res = /^[0-9a-z_]{4,16}$/
    //regex here/.test(username) 
  return res.test(username)
}
```
