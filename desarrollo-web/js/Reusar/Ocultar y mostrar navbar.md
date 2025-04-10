```js
const navbar = document.querySelector(".navbar");
let lastPosition = window.scrollY;

window.addEventListener("scroll", () => {
    let currentPosition = window.scrollY;
    
    if (currentPosition > lastPosition && currentPosition > 200) {
        navbar.classList.add("hide");
    } else {
        navbar.classList.remove("hide");
    }
    lastPosition = currentPosition;
});
```