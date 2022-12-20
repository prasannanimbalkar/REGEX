# User Regex

To use the regular expression for matching a username in JavaScript, you can use the test method of the RegExp object. Here is an example of how you could use it to validate a username:

const usernameRegex = /^[a-zA-Z0-9._-]{3,16}$/;

function isValidUsername(username) {
  return usernameRegex.test(username);
}

console.log(isValidUsername("abc123")); // true
console.log(isValidUsername("my.username")); // true
console.log(isValidUsername("a")); // false (too short)
console.log(isValidUsername("myusernameismuchtoolong")); // false (too long)
console.log(isValidUsername("my username")); // false (contains an invalid character)
The test method returns a boolean value indicating whether the regex matches the given string. In this example, isValidUsername is a function that takes a username as an argument and returns true if the username is valid according to the regex, and false otherwise.

You can also use the match method of the String object to search for a username in a larger body of text. For example:

Copy code
const text = "My username is john.doe and my friend's username is jane.doe.";
const usernameRegex = /^[a-zA-Z0-9._-]{3,16}$/;
const matches = text.match(usernameRegex);
console.log(matches); // ["john.doe", "jane.doe"]
This would output an array containing the two username matches found in the text.



# Password Regex
