
# JS DrumKit

This project is the first JS-30 challenge where I learned about ```DOM, event listner```, ```audio``` and ```transition end``` thing.


## Demo

[Click Here](https://skyz03.github.io/JS---DrumKit/)

## Features

- Playing of Audio.
- Add Class & Remove Class after transition end.
- Use of Event Listners to play an audio & add/remove class.

## Lessons Learned

As this is one of the first JS challenge, here I first understood the loop of ```adding eventlisters.```

```DOM SELECTION => EVENT lISTENER => ADD/REMOVE CLASS```.

```EVENT lISTENER => DOM SELECTION => ADD/REMOVE CLASS```.


```
function playSound(e) {  //this e is event
window.addEventListener("keydown", playSound);

  const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);  //to get the audio of that keycode.
  const key = document.querySelector(`.key[data-key="${e.keyCode}"]`);     //to get the div associated with the keycode.

  if (!audio) return;
  audio.currentTime = 0;
  audio.play();

  key.classList.add("playing");
}

```

Here, e = event & addEventListener is added followed by DOM and then add class at the end.

## Optimizations

The everytime changing background rather than static one.

## Screenshots

[image](https://user-images.githubusercontent.com/42742924/150360629-1c2df672-e027-4e67-ae07-531734634f23.png)

## Tech Stack

**Client:** HTML, CSS/SCSS & JS

## Documentation

[Difference between onClick & addEventListner](https://stackoverflow.com/questions/6348494/addeventlistener-vs-onclick)

[Difference2 between onClick & addEventListner](https://www.google.com/search?client=firefox-b-d&q=onclick+event+listener+vs+.addeventlistner)

# Notes 

The function playSound is selecting the audio and the div element related the specific keys and playing the sound with addition of border class.

The another remove transition is used to wait for the transform transaction to end it's animation where after class is removed after animation.

Finally it is calling both the function at the end and it is working
