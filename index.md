## Project 2

In this project, we learned some advanced JavaScript functions


### Source Code

     const getRandomInteger = function getRandomInteger(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    // Returns a single random lowercase letter
    const getRandomLetter = function getRandomLetter() {
        const alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
        let result = alphabet[getRandomInteger(0,25)];

        return result;
    }

    const getSetRandomString = function getSetRandomString () {
        let result = "";

        for (let i = 0; i < getRandomInteger(5, 26); i++) {
        result += getRandomLetter();
        }

        return result;
    }

    const getRandomString = function getRandomString(minLength, maxLength){
        let result = "";
        for (let i = 0; i < getRandomInteger(minLength, maxLength); i++) {
        result += getRandomLetter();
        }
        return result;
    }

    //Function that inputs a string, splits it into an array, sorts the array, and joins it back into a string. Returns sorted string
    const getSortedString = (string) => {let s = string.split(""); s.sort(); let joined = s.join(''); return joined;}


    console.log(getSortedString("grant"));
    console.log(getRandomString(10,20));


