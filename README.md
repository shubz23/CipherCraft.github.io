# Project Name: CipherCraft

# Description
- CipherCraft is a simple web application that generates secure passwords based on user preferences. 
- Users can specify the length of the password and choose whether it should contain uppercase letters, lowercase letters, numbers, and symbols. 
- The application then generates a random password that meets these criteria and displays it for the user. 
- Additionally, users can copy the generated password to their clipboard with the click of a button.

```javascript
const pwE1 = document.getElementById("pw");
const copyE1 = document.getElementById("copy");
const lenE1 = document.getElementById("len");
const upperE1 = document.getElementById("upper");
const lowerE1 = document.getElementById("lower");
const numberE1 = document.getElementById("number");
const symbolE1 = document.getElementById("symbol");
const generateE1 = document.getElementById("generate");

const upperLetters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
const lowerLetters = "abcdefghijklmnopqrstuvwxyz";
const numbers = "0123456789";
const symbols = "!@#$%^&*()_+=";

function getLowercase() {
  return lowerLetters[Math.floor(Math.random() * lowerLetters.length)];
}

// For rest of the cases we similarly create functions

copyE1.addEventListener("click", () => {
  const textarea = document.createElement("textarea");
  const password = pwE1.innerText;

  if (!password) {
    return;
  }

  textarea.value = password;
  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  textarea.remove();
  alert("Password copied to clipboard");
});
``` 


# Installation
- No installation required. Simply open the index.html file in a web browser.

# Usage
1. Open the index.html file in a web browser.
2. Specify the desired password length.
3. Check the boxes for the types of characters you want in the password (uppercase letters, lowercase letters, numbers, symbols).
4. Click the "Generate Password" button.
5. The generated password will be displayed in the designated area.
6. Click the "Copy" button to copy the password to your clipboard.

# Technologies Used
- HTML
- CSS
- JavaScript
