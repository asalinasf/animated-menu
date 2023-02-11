# Animated Menu

This project is about an animated menu is made with HTML, CSS and Sass

# Screen Project

## Computer
![project screen](img/screen.png)

# Install

```sh
git clone https://github.com/asalinasf/animated-menu/
cd animated-menu
open in your browse
```

# HTML
```html
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./css/styles.css">
    <title>Animated Menu</title>
</head>

<body>
    <ul>
        <li style="--i:#a955ff; --j:#ea51ff;">
            <span class="icon">
                <ion-icon name="home-outline"></ion-icon>
            </span>
            <span class="title">Home</span>
        </li>
        <li style="--i:#56ccf2; --j:#2f80ed;">
            <span class="icon">
                <ion-icon name="chatbubble-outline"></ion-icon>
            </span>
            <span class="title">Messages</span>
        </li>
        <li style="--i:#ff9966; --j:#ff5e62;">
            <span class="icon">
                <ion-icon name="heart-outline"></ion-icon>
            </span>
            <span class="title">Favorite</span>
        </li>
        <li style="--i:#80ff72; --j:#7ee8fa;">
            <span class="icon">
                <ion-icon name="videocam-outline"></ion-icon>
            </span>
            <span class="title">Videos</span>
        </li>
        <li style="--i:#ffa9c6; --j:#f434e2;">
            <span class="icon">
                <ion-icon name="camera-outline"></ion-icon>
            </span>
            <span class="title">Photos</span>
        </li>
    </ul>
    <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
</body>

</html>
```

# CSS
```css
* {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  box-sizing: border-box;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
body ul {
  position: relative;
  display: flex;
  gap: 25px;
}
body ul li {
  position: relative;
  list-style: none;
  width: 60px;
  height: 60px;
  background-color: #fff;
  border-radius: 60px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.1);
  transition: 0.5s;
}
body ul li:hover {
  width: 180px;
  box-shadow: 0px 10px 25px rgba(0, 0, 0, 0);
}
body ul li:hover::before {
  opacity: 1;
}
body ul li:hover::after {
  opacity: 0.5;
}
body ul li:hover ion-icon {
  transform: scale(0);
  color: #fff;
  transition-delay: 0.25s;
}
body ul li:hover .title {
  transform: scale(1);
  transition-delay: 0.5s;
}
body ul li::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: 60px;
  background: linear-gradient(45deg, var(--i), var(--j));
  opacity: 0;
  transition: 0.5;
}
body ul li::after {
  content: "";
  position: absolute;
  top: 10px;
  width: 100%;
  height: 100%;
  border-radius: 60px;
  background: linear-gradient(45deg, var(--i), var(--j));
  z-index: -1;
  filter: blur(15px);
  transition: 0.5;
  opacity: 0;
}
body ul li ion-icon {
  color: #777;
  font-size: 1.5em;
  transition: 0.5s;
  transition-delay: 0.25;
}
body ul li span {
  position: absolute;
}
body ul li .title {
  color: #fff;
  font-size: 1.1em;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  transform: scale(0);
  transition: 0.5s;
  transition-delay: 0s;
}
```
# Visit my project with this url

https://menuaaronsalinas.netlify.app/
