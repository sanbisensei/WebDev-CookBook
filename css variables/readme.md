  # CSS VARIABLES
  ## dark and light theme
 * here we first declared 2 buttons. one is dark theme and another one is light theme
 then we add the classes.
 ```
  <button id="dark-theme-btn">Dark Theme</button>
    <button id="light-theme-btn">Light Theme</button>
 ```
 * then we did this:
 ```
body{
    background-color: var(--background-color, pink);
}
 
 ```
 * we tipically call custom variables by var(your custom var)
 * here "--" means custom variable.
 * then your old style css stuff.
 * but we *didnt dicalare* any color to our custom variable.
 * so "," means if my custom variables dont have any values then my background color will be pink.
 * now we are going to add some dynamic color with js:
  
```
document.getElementById('dark-theme-btn').addEventListener('click', ()=> {
    document.documentElement.style.setProperty('--background-color', '#333')
})

document.getElementById('light-theme-btn').addEventListener('click', ()=> {
    document.documentElement.style.setProperty('--background-color', 'white')
})
```

* here we used **document.getElementById('dark-theme-btn')** for getting my button
* then we used **addEventListener()** to add a event which is changeing bg with one click of a button
* then we used 'click' goes by a coma and then a arrow function
* in arrow function I first got my css custom variable using **document.documentElement.style.setProperty('--background-color', '#333')**
* here in brackets we first declared my very own custom variable then , the color that we want to store in my variable
* then i repeated this again but with white theme button

## custom var useage

```
:root {
    --div-background-color: red;
    --text-color: black;
    --div-margin: 20px;
    --div-padding: 20px;
}
```
* here we pre declared our custom var
* structure>> --(name of your choise)-(css stuff): (value);
* we use custom var like this:
  


  ```
   .child{
    background-color: var(--div-background-color);
    padding: var(--div-margin);
  }
 
   .one{
    --div-background-color: blue;
    --text-color: white;

  }

  .one-one, .one-two{
    margin: var(--div-margin);
    padding: var(--div-padding);
  }
  ``` 
