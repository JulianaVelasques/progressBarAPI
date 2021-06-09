<h2 align="center">
  🚀 Progress Bar
</h2>

<p align="center">
  
  <a href="https://github.com/Silve1ra/coffee-shop/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/JulianaVelasques/progressBarAPI">
  </a>

  <a href="https://github.com/Silve1ra/coffee-shop/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/JulianaVelasques/progressBarAPI">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-brightgreen">
</p>

This project is a progress Bar for a Clown's web app. It allow people to give a "Hahaha!" every time they have to do the Clown's performance evaluation.


## API Reference

### Getting Started
- Base URL: At present this app can only be run at https://jsfiddle.net/JulianaVelasques/aymsfk1e/199/. 

### Endpoints 
#### Function /getProgress
- General:
    - Returns the style of the progressBar and the ```aria-valuenow``` attribute that defines the current value for the progressbar .
    
```
function getProgress() {
  return document.getElementById("progressBar").getAttribute("aria-valuenow");
}
```

#### Function /setProgress
- General:
    - This function determine that the value of progressbar will be the the value of the ```aria-valuenow``` and this ``value`` will change the value of ``width`` that will be displayed on the screen. In short, with this function we can show the progress to the final-user by using the ``innerHTLM`` property to modify the content of the HTML element.
    

```
function setProgress(value) {
  document.getElementById("progressBar").setAttribute("aria-valuenow", value);  
  document.getElementById("progressBar").setAttribute("style", "width: " + value + "%;");
  document.getElementById("progressBar").innerHTML = (value + "%");
}
```

#### Function /increment
- General:
    - Whit this function we can specify the rules for the progressbar. It will be activated each time the final-user click on the button. So, each time the button is clicked will increase the ``getProgress`` on the screen by 1 and then set it on the screen, it will happens when the progress < than 100.
    - When the clown get 100 "Hahaha!" the user will see a message showing that they found the best clown.

```
function increment() {
	var i = getProgress();
	if(i < 100){
		i++;
		setProgress(i);	
	}else{
		alert("You found the best clown.");
	}
}
```




## Authors
Yours truly, <a href="https://github.com/JulianaVelasques"><b>Juliana Velasques</b> 
