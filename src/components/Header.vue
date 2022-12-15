<template>
    <header>
      <div class="container">
        <div class="navbar-header">
          <a
            class="logo"
            href="https://drupal-coder.ru/"
            title="Главная"
            rel="home"
          >
            <img
              src="./../assets/logo.png"
              alt="Главная"
              width="156"
              height="31"
            />
          </a>
        </div>
  
        <div class="navbar-collapse-wrapper">
          <ul id="navbar">
            <li><a href="#">Поддержка Drupal</a></li>
            <li><a href="#">Администрирование</a></li>
            <li><a href="#">Продвижение</a></li>
            <li><a href="#">Реклама</a></li>
            <li><a href="#">О нас</a></li>
            <li><a href="#">Проекты</a></li>
            <li><a href="#">Контакты</a></li>
          </ul>
        </div>
      </div>
    </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  display:flex;
  padding: 30px 0px;
  background-color: rgba(0, 0, 0, 0.47);
}
.navbar-header {
  padding: 0px 15px 0px 0px;
  float: left;
}
.logo {
  display: block;
  width: 190px;
  margin: 0px 60px 0px 0px;
}

.navbar-collapse-wrapper {
  display: flex;
  float:left;
  background-color:black;
}

#navbar {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

#navbar li {
  margin-right: 40px;
  margin-bottom: 8px;
  display: inline;
}

#navbar a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
  display: inline-block;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #ffffff;
}
</style>
