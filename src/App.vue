<template>
  <div id="app">
    <Header />

    <Navbar />

    <router-view />

    <Footer />
  </div>
</template>

<script>
  import Header from '@/components/layout/Header.vue';
  import Navbar from '@/components/layout/Navbar.vue';
  import Footer from '@/components/layout/Footer.vue';

  export default {
    components: {
      Header,
      Navbar,
      Footer
    }
  };
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Montserrat:400,700|Pacifico');

  * {
    box-sizing: border-box;
  }
  body {
    font-family: 'Montserrat', sans-serif;
    margin: 0;
  }
  /*--------------------------- Estilos base -----------------------------------*/
  img {
    display: block;
    width: 100%;
    max-width: 100%;
  }
  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    margin: 0;
  }
  .container {
    width: 100%;
    margin: auto;
  }
  .container--flex {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
  }
  .column {
    width: 100%;
  }

  /*------------------------------Estilos del banner--------------------------- */

  .banner {
    margin-top: -55px;
    position: relative;
  }
  .banner::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    z-index: 1000;
    top: 0;
  }
  .banner__img {
    width: 100%;
    height: 400px;
    object-fit: cover;
  }
  .banner__content {
    width: 90%;
    color: white;
    text-align: center;
    position: absolute;
    z-index: 1500;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    font-size: 1.5em;
    font-weight: bold;
  }

  /*----------------------------Estilos principales-----------------------------*/

  .group--color .container {
    background: #de423a;
    color: white;
    padding: 10px;
  }
  .main__title {
    margin: 15px 0;
    font-size: 1.8em;
    font-family: 'Pacifico', cursive;
    font-weight: 100;
  }
  .main__txt {
    padding: 15px;
  }
  .column__title {
    font-size: 1.3em;
  }
  .main__about__descirption .column:nth-child(2) {
    padding: 10px;
  }
  .btn {
    display: block;
    text-align: center;
    text-decoration: none;
    width: 100%;
    background: #de423a;
    color: white;
    padding: 10px;
    margin: 10px auto;
  }
  .btn:hover {
    cursor: pointer;
    background: #e96861;
  }
  .group__title {
    font-family: 'Pacifico', cursive;
    text-align: center;
    font-weight: 100;
    font-size: 1.8em;
    margin: 30px;
  }
  .best-models .column {
    margin-bottom: 30px;
    text-align: center;
  }
  .best-models__img {
    margin: auto;
    max-width: 350px;
  }
  .best-models__title {
    font-size: 1.3em;
    padding-top: 10px;
    padding-bottom: 20px;
  }
  .best-models__price {
    font-size: 1.5em;
    color: #de423a;
    font-weight: bold;
  }

  /*----------------------------Estilos responsive------------------------------*/

  @media screen and (min-width: 480px) {
    .logo {
      color: white;
    }
    .main-header__contactInfo {
      text-align: right;
    }

    .main-header__contactInfo__phone {
      background: none;
    }
    .main-header__contactInfo__address {
      color: white;
    }
    .main-nav {
      background: rgba(0, 0, 0, 0.85);
    }
    .banner {
      margin-top: -150px;
      z-index: -1000;
    }
    .banner__img {
      height: 600px;
    }
    .banner__content {
      font-size: 2em;
    }
    .main {
      padding-bottom: 15px;
    }
    .main__about__descirption .column:nth-child(2) {
      padding-left: 20px;
      font-size: 0.9em;
    }
    .main__about__descirption .btn {
      margin: 0;
    }
    .best-models .column {
      border: 5px solid #ddd;
      padding: 5px;
    }
    .best-models__img {
      height: 200px;
      object-fit: cover;
    }
    /*-------- Valores especiales ---------------*/
    .main-footer .container--flex {
      align-items: flex-start;
    }
    .column--50 {
      width: 49%;
    }
    .column--50-25 {
      width: 49%;
    }
    .column--33 {
      width: 32%;
    }
  }

  @media screen and (min-width: 768px) {
    .main__title {
      font-size: 2.2em;
    }
    .main__about__descirption {
      margin-top: 30px;
    }
    .main__about__descirption .column--50:nth-child(2) {
      font-size: 1em;
    }
    .main__about__descirption .column--50:nth-child(2) .column__txt {
      line-height: 30px;
    }
    .column--50-25 {
      width: 24.5%;
    }
    .column__title {
      font-size: 1em;
    }
    .group__title {
      font-size: 2.2em;
    }
  }

  @media screen and (min-width: 1024px) {
    .container {
      width: 1000px;
    }
    .logo {
      font-size: 2em;
      padding: 0;
    }
    .main-header__contactInfo__phone,
    .main-header__contactInfo__address {
      padding-right: 0;
      font-size: 1.15em;
    }
    .main-nav {
      padding: 0;
    }
    .banner__img {
      height: 600px;
    }
    .banner__content {
      font-size: 2.5em;
    }
    .icon-menu {
      display: none;
    }
    .menu {
      position: static;
      display: flex;
      height: auto;
      width: auto;
    }
    .menu__link {
      padding: 20px;
    }
    .group--color .container {
      margin-top: 30px;
      margin-bottom: 30px;
      padding: 20px;
    }
    .main__title {
      font-size: 2.5em;
    }
    .main__about__descirption .column--50:nth-child(2) .column__txt {
      line-height: 45px;
    }
    .best-models__title {
      font-size: 1.4em;
    }
    .best-models__price {
      font-size: 1.8em;
    }
    .main-footer {
      padding-top: 30px;
      padding-bottom: 30px;
    }
  }

  @media screen and (min-width: 1600px) {
    .container {
      width: 1400px;
    }
    .main__about__descirption .column:nth-child(1) img {
      width: 100%;
      height: 350px;
      object-fit: cover;
    }
    .best-models__img {
      height: 300px;
    }
  }

  /*
  #nav {
    padding: 30px;

    a {
      font-weight: bold;
      color: #2c3e50;

      &.router-link-exact-active {
        color: #42b983;
      }
    }
  }*/
</style>
