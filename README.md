# ten-line-slides

Ten lines of Javascript is enough to make a very basic slide library.

Well, ten lines of Javascript and four CSS rules.

Final product

* [start here](1.html)
* [final product](slides.html)


```html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>slides</title>
<style>
body { 
  margin: 0; 
  padding: 0;
}
section {  
  width: 100vw; 
  height: 100vh; 
  display: none;
}
h1 {
  margin: 0;
}
section:first-child { 
  display: block; 
}
#one   { background-color: hsla(115, 27%, 56%, 1);}
#two   { background-color: hsla(42, 83%, 70%, 1);}
#three { background-color: hsla(17, 89%, 72%, 1);}
#four  { background-color: hsla(158, 20%, 43%, 1);}
#five  { background-color: hsla(338, 37%, 54%, 1);}
</style>
</head>

<body>

<main>
  <section id=one  ><h1>first slide </h1></section>
  <section id=two  ><h1>second slide</h1></section>
  <section id=three><h1>third slide </h1></section>
  <section id=four ><h1>fourth slide</h1></section>
  <section id=five ><h1>fifth slide </h1></section>
</main>


<script class=slides>
let main = document.querySelector('main')
document.addEventListener('keyup', keyupEvent => {
  if(keyupEvent.key == 'ArrowRight'){
    main.appendChild(main.firstElementChild)
  }
  if(keyupEvent.key == 'ArrowLeft'){
    main.insertAdjacentElement('afterbegin', main.lastElementChild)
  }
})
</script>

</body>
</html>
```
