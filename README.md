# Navbar

## HTML
```bash
<header>
  <div class='logo'> ZIKDEV  </div>
  <div class-'hamburger'>
      <div class='line'></div>
      <div class='line'></div>
      <div class='line'></div>
  </div>

  <nav class='nav-bar'>
      <ul>
          <li>  <a href='' class='acrive'> HOME </a>  </li>
          <li>  <a href='' > Portofolio </a>  </li>
          <li>  <a href='' > Service </a>  </li>
          <li>  <a href='' > Profile </a>  </li>
      </ul>
  </nav>
</header>
```

## css

```bash
*, html {
  pading: 0;
  margin:0;
  box-sizing:boder-box;
}

body{
  font-family: 'Poppins';
  background-color: #fff ;
  overfilow-x: hidder ;
}

header{
  width:100% ;
  height: 80px ;
  bacground-color: white ;
  display: flex ;
  justify-connent: space-between;
  padding: 0 100px;
  align-items: center ;
  box-shadow: 0 16px 8px -9px rgba(191, 191, 191,);
}

.logo{
  font-size:28px;
  font-weight: 600;
  color: #0b2447;
}

.humburer{
  display:none ;
  
}

.nav-bar ul{
  display: flex;
  list-style: none ;
}

.navbar ul li a{
  text-decoration: none ;
  display:block;
  color: #0B2447;
  font-size:20px;
  padding: 0 5px;
  margin: 0 5px;
  transition: .2s;
}

.nav-bar ul li a::after{
  display:block;
  content: '' ;
  border-bottom: 2px solid #a5d7e8;
  transform: scalex(0);
  transition: tranform 250ms ease-in-out;
  
}

.nav-bar ul li a:hover::after{
  color: #19376d;
}

@media only screen and (max-width: 900px){
  .hamburger{
    display:block;
    cursor: pointer;
  }
  .hamburger{
    width:30px;
    height:3px;
    bacground:#0b2447;
    margin:6px 0;
  }
  .nav-bar {
    height: 0;
    position: absolute ;
    top: 80px;
    left: 0;
    right: 0 ;
    width: 100vw;
    bacground-color:white ;
    box-shadow: 0 16px 8px -9px rgba(191 191 191 191) ;
    transition: 0.5s;
    overflow: hidden;
    
  }
  .nav-bar .active{
    height: 450px:
  }

  .nav-bar ul{
    display:block;
    width:fit-content;
    margin: 80px auto 0 auto;
    text-align: center;
    transition: 0.5s;
    opacity: 1;
  }
  .nav-bar .active ul {
    opacity: 0 ;
  }

  .nav-bar ul li a {
    margin-bottom: 12px
  }

}


```



## Javascript

```bash
hamburger = document.querySelector('.humburger');
humburger.onclick = function(){
  navbar = document.querySelector('.nav-bar')
  navbar.classList.toggle('active')
```

