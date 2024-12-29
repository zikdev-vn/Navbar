# Navbar

## HTML
```bash
<header>
  <div class='logo'> ZIKDEV </div>
  <div class='hamburger'>
      <div class='line'></div>
      <div class='line'></div>
      <div class='line'></div>
  </div>

  <nav class='nav-bar'>
      <ul>
          <li> <a href='' class='active'> HOME </a> </li>
          <li> <a href=''> Portfolio </a> </li>
          <li> <a href=''> Service </a> </li>
          <li> <a href=''> Profile </a> </li>
      </ul>
  </nav>
</header>
```

## css

```bash
*, html {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins';
  background-color: #fff;
  overflow-x: hidden;
}

header {
  width: 100%;
  height: 80px;
  background-color: white;
  display: flex;
  justify-content: space-between;
  padding: 0 100px;
  align-items: center;
  box-shadow: 0 16px 8px -9px rgba(191, 191, 191, 1);
}

.logo {
  font-size: 28px;
  font-weight: 600;
  color: #0b2447;
}

.hamburger {
  display: none;
}

.nav-bar ul {
  display: flex;
  list-style: none;
}

.nav-bar ul li a {
  text-decoration: none;
  display: block;
  color: #0B2447;
  font-size: 20px;
  padding: 0 5px;
  margin: 0 5px;
  transition: .2s;
}

.nav-bar ul li a::after {
  display: block;
  content: '';
  border-bottom: 2px solid #a5d7e8;
  transform: scaleX(0);
  transition: transform 250ms ease-in-out;
}

.nav-bar ul li a:hover::after {
  transform: scaleX(1);
  color: #19376d;
}

@media only screen and (max-width: 900px) {
  .hamburger {
    display: block;
    cursor: pointer;
  }
  .line {
    width: 30px;
    height: 3px;
    background: #0b2447;
    margin: 6px 0;
  }
  .nav-bar {
    height: 0;
    position: absolute;
    top: 80px;
    left: 0;
    right: 0;
    width: 100vw;
    background-color: white;
    box-shadow: 0 16px 8px -9px rgba(191, 191, 191, 1);
    transition: 0.5s;
    overflow: hidden;
  }
  .nav-bar.active {
    height: 450px;
  }
  .nav-bar ul {
    display: block;
    width: fit-content;
    margin: 80px auto 0 auto;
    text-align: center;
    transition: 0.5s;
    opacity: 1;
  }
  .nav-bar ul li a {
    margin-bottom: 12px;
  }
}
```



## Javascript

```bash
const hamburger = document.querySelector('.hamburger');
hamburger.onclick = function() {
  const navbar = document.querySelector('.nav-bar');
  navbar.classList.toggle('active');
};
```

# Background animation


## html

```bash
<div class='div'></div> 
```

## css

```bash
.div{
  background-size: 100% 100% ;
  box-shadow: 20px 20px 10px gray ;
  animation: slider 10s linear infinte;
}

.@keyframes sider{
  0%{background-image:url();},
  30%{background-image:url();},
  60%{background-image:url();},
  100%{background-image:url();}
}
```
