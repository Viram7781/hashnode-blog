## Random Background color Generator with Javascript #project1

In this article, you will learn how to build a simple Random Background Generator by using simple Javascript basics.

So let's dive in :

Prerequisites:

1. Of course a code editor
2. Basic knowledge of Html, CSS & Javascript 


### 1. HTML Setting

Create a div with a class of main and add a button with a class btn and add onclick event with a function changeBg()

```
<div class="main">
     <button class="btn" onclick="changeBg()">Change Bg</button>
</div>
```

### 2. CSS Setting
Since this is a Javascript tutorial I am not focusing more on styling.

I just center the button in main div by using flex box. Don't worry if you don't know what is flex box

```
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.main{
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### 3. Javascript Setting
Let the fun part begin :

```
function changeBg() {
  let bg = Math.random();
   
  let bgStr = bg.toString(16);
   
  let randomBg = '#' + bgStr.substr(2,6);
   
  let main = document.querySelector('.main');
   
  main.style.backgroundColor = randomBg;
}

```

Time to break down the codes and see what exactly happened :


A. First we need to create a function.

```
function changeBg(){
 
}
```

B. Create a variable to store the value of Math.random( )

Math.random() returns a random number between 0 (inclusive), and 1 (exclusive)

Math.random() always returns a number lower than 1 
```
function changeBg() {
  let bg = Math.random();
}
```
C. Convert the value of math random to a string by using the toString(16) method and store it in a variable

The toString() method converts a number to a string.

16 - The number will show as an hexadecimal value

toString(16) returns:
15 = f,
14 = e,
13 = d,
12 = c,
11 = b,
10 = a,
9 = 9,
8 = 8,
7 = 7,
6 = 6,
5 = 5,
4 = 4,
3 = 3,
2 = 2,
1 = 1,
0 = 0

```
function changeBg() {
  let bg = Math.random();
   
  let bgStr = bg.toString(16);
 
}
```

D. We need only 6 characters to change our background colour because hex code takes only 3 characters or 6 characters.

So that we need to slice 6 characters from the above variable (bg) to do that we use the .substr() method

string.substr(start, length)

The substr() method extracts parts of a string, beginning at the character at a specified position, and returns a specified number of characters.

To extract characters from the end of the string, use a negative start number.


```
function changeBg() {
  let bg = Math.random();
   
  let bgStr = bg.toString(16);
   
  let randomBg = '#' + bgStr.substr(2,6);
 
}
```

E. Then we need to select the container by using query selector and store it in a variable


```
function changeBg() {
  let bg = Math.random();
   
  let bgStr = bg.toString(16);
   
  let randomBg = '#' + bgStr.substr(2,6);
   
  let main = document.querySelector('.main');
 
}
```

F. After selecting the container use we need to set the background colour to the value stored in the variable i.e randomBg bg by using the style background colour method


```
function changeBg() {
  let bg = Math.random();
   
  let bgStr = bg.toString(16);
   
  let randomBg = '#' + bgStr.substr(2,6);
   
  let main = document.querySelector('.main');
   
  main.style.backgroundColor = randomBg;
}
```

I modified the code that I described in this article and added few mode elements such as displaying the hex code of the background color and added a copy button to make copying the hex code easy and use in our projects. I also added few styling to the button.

Random Background Color Generator project [live demo](https://codepen.io/Ram7781/full/vYmmqOE) hosted on codepen do check it out

I advise all of you to practice by coding yourself. Play with javascript functions and create projects and comment down below the link to it.

I love to check them out

I hope you found my article helpful. [Buy Me a Coffee](https://www.buymeacoffee.com/Ram7781) if you would like to support me.

Thanks for reading😉

Have a nice day😊