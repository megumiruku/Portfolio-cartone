<template>
  <div class="header">
      <div class="header-logo">
          <a href="/"><img class="logo" src="../assets/HOME/logo.png" alt="logo"/></a>
      </div>
      <div class="header-nav">
        <nav>
          <ul class="header-nav-list">
            <li class="header-nav-item">
              <a href="/about">About Me</a>
            </li>
            <li class="header-nav-item" >
              <a href="/works">Works</a>
            <li class="header-nav-item">
              <a href="/contact">Contact</a>
            </li>
          </ul>
        </nav>
        <div class="copyright">
          <p>Osaka based Fashion Photographer all images copyright © 2011-2021 Gaetano Cartone | All Rights Reserved</p>
        </div>
        <div class="sns-icons">
          <a href="https://twitter.com/GaetanoCartone" target="_blank"><i class="fab fa-twitter"></i></a>
          <a href="https://www.facebook.com/gaetano.cartone/?ref=hl" target="_blank"><i class="fab fa-facebook"></i></a>
          <a href="https://www.instagram.com/gaetanocartone/" target="_blank"><i class="fab fa-instagram"></i></a>
        </div>
      </div>
    <div id="hamburger" @click="hamburger()" :class="{'active':isClass}">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="menu-content" :class="{'open':isClass}">
      <p class="menu-title">Gaetano Cartone</p>
      <ul class="menu_content_inner">
        <li><a href="/">Home</a></li>
        <li><a href="/about">About Me</a></li>
        <li><a href="/works">Works</a></li>
        <li><a href="/contact">Contact</a></li>
      </ul>
      <div class="copyright">
          <p>Osaka based Fashion Photographer <br>all images copyright © 2011-2021 <br>Gaetano Cartone | All Rights Reserved</p>
      </div>
      <div class="sns-icons">
        <a href="https://twitter.com/GaetanoCartone" target="_blank"><i class="fab fa-twitter"></i></a>
        <a href="https://www.facebook.com/gaetano.cartone/?ref=hl" target="_blank"><i class="fab fa-facebook"></i></a>
        <a href="https://www.instagram.com/gaetanocartone/" target="_blank"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isClass: false,
    };
  },
  methods: {
    hamburger() {
      this.isClass = !this.isClass;
    }
  }
};
</script>

<style scoped>
.header{
  height: 80vh;
  width: 25%;
  position: sticky;
  position: -webkit-sticky;
  top: 50px;
} 
.logo {
  width: 65%; 
}
.logo:hover {
  opacity: 0.7;
}
.header-nav-list {
  padding: 0;
}
.header-nav {
  display: block;
  width:70%;
  margin: 40px 0;
}
.header-nav-item {
  padding:10px 0;
  cursor: pointer;
  list-style: none;
}
.header-nav-item:hover {
  opacity:0.7;
}
.header-nav-item a {
  text-decoration: none;
  color:#333333;
}
.copyright {
  border-top: 0.5px solid #999999;
  padding-top:15px;
  text-align: left;
  font-size: 11px;
  width: 75%;
  line-height: 18px;
   color:#333333;
}
.sns-icons {
  width: 70%;
  display: block;
  margin-top: 30px;
}
.sns-icons a {
  color: black;
  padding-left: 15px;
}
.sns-icons a:hover {
  opacity: 0.7;
}
.menu-content {
  display: none;
}

@media screen and (max-width: 767px) {
  .header {
    width: 80%;
    height: 15vh;
    position: static;
    padding-top: 20px;
  }
  .header-nav{
    display: none;
  }
  .header-logo {
    width: 65%;
    margin-left:10px;
  }
  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 20px;
    right: 20px;
    transition: 0.4s;
  }
  #hamburger span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: #BFBFBF;
    transition: 0.8s;
  }
  #hamburger span:nth-of-type(1) {
    top: 10px;
  }
  #hamburger span:nth-of-type(2) {
    top: 20px;
  }
  #hamburger span:nth-of-type(3) {
    top: 30px;
  }
  
  #hamburger.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }
  #hamburger.active span:nth-of-type(2) {
    opacity: 0;
  }
  #hamburger.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg);
  }
  .menu-content {
    display: block;
    width: calc(100% - 80px);
    height: 100%;
    text-align: center;
    transition: 0.2s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: #fff;
    box-shadow: 80px 0 rgba(77, 76, 76, 0.4);
    z-index: 999;
  }
  .menu-content .menu-title {
    margin: 40px 20px;
    font-size: 1.2rem;
    color: #333333;
    text-align: left;
  }
  .menu_content_inner {
    padding:0;
  }
  .menu-content li a {
    width: 40%;
    margin: 15px;
    padding: 5px;
    border-bottom: 0.5px solid rgba(77, 76, 76, 0.5);
    text-decoration: none;
    display: block;
    color:#333
  }
  .menu-content li {
    width: 100%;
    text-align: left;
    list-style: none;
  }
  .menu-content.open {
    left: 0;
  }
  .copyright {
    margin-left: 20px;
    border-top: none;
  }
}

</style>