<template>
  <header id="navbar">
    <div class="container">
      <div class="navbar-header">
        <a
          class="logo-header"
          href="https://drupal-coder.ru/"
          title="Главная"
          rel="home"
        >
          <img
            src="./../assets/logo.png"
            alt="Главная"
            width="180"
            height="31"
          />
        </a>
      </div>

      <div class="navbar-collapse-wrapper">
        <ul id="navbar-content">
          <li><a href="#">Поддержка Drupal</a></li>
          <li>
            <a href="#">Администрирование</a>
            <span class="caret"></span>
            
          </li>
          <li><a href="#">Продвижение</a></li>
          <li><a href="#">Реклама</a></li>
          <li>
            <a href="#">О нас</a>
            <span class="caret"></span>
          </li>
          <li><a href="#">Проекты</a></li>
          <li><a href="#">Контакты</a></li>
        </ul>
      </div>
    </div>
  </header>
  <div class="fullscreen">
    <div class="block-main-header">
      <div class="block-main-background">
        <video>
          <!-- autoplay muted loop -->
          <source src="./../assets/video.mp4" type="video/mp4" />
        </video>
      </div>
      <div class="block-main mb-5">
        <div class="container">
          <div class="row">
            <div class="col-md-6">
              <h1 class="main-title">
                Поддержка <br />
                сайтов на Drupal
              </h1>
              <div class="main-description">
                Сопровождение и поддержка сайтов
                <br />
                на CMS Drupal любых версий и запущенности
              </div>
              <div class="main-contact">
                <a href="#" class="main-contact-btn">Тарифы</a>
              </div>
            </div>
            <div class="col-md-6">
              <div class="row w-99 h-100 align-items-center">
                <div class="col-12 row">
                  <div class="col-4">
                    <div class="support-achievement-wrapper">
                      <div class="support-achievement-title">
                        <div>
                          <h style="font-size: 48px">#1</h>
                          <img
                            src="./../assets/cup.png"
                            alt="Награда"
                            width="60"
                            height="60"
                          />
                        </div>
                      </div>
                      <div class="support-achievement-description">
                        Drupal-разработчик <br />
                        в России по версии <br />
                        Рейтинга Рунета
                      </div>
                    </div>
                  </div>
                  <div class="col-4 mt-4">
                    <div class="support-achievement-wrapper">
                      <div class="support-achievement-title">3+</div>
                      <div class="support-achievement-description">
                        средний опыт <br />
                        специалистов более <br />
                        3 лет
                      </div>
                    </div>
                  </div>
                  <div class="col-4 mt-4">
                    <div class="support-achievement-wrapper">
                      <div class="support-achievement-title">14</div>
                      <div class="support-achievement-description">
                        лет опыта в сфере <br />
                        Drupal
                      </div>
                    </div>
                  </div>
                </div>
                <div class="col-12 row mt-2">
                  <div class="col-4">
                    <div class="support-achievement-wrapper">
                      <div class="support-achievement-title">50+</div>
                      <div class="support-achievement-description">
                        модулей и тем <br />
                        в формате DrupalGive
                      </div>
                    </div>
                  </div>
                  <div class="col-4">
                    <div class="support-achievement-wrapper">
                      <div class="support-achievement-title">90 000+</div>
                      <div class="support-achievement-description">
                        часов поддержки <br />
                        сайтов на Drupal <br />
                      </div>
                    </div>
                  </div>
                  <div class="col-4">
                    <div class="support-achievement-wrapper">
                      <div class="support-achievement-title">300+</div>
                      <div class="support-achievement-description">
                        Проектов <br />
                        на поддержке <br />
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#navbar {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  border-radius: 0;
  border: 0;
  padding-top: 30px;
  padding-bottom: 30px;
  background: transparent;
}

header {
  box-sizing: border-box;
  display: flex;
  padding: 30px 0px;
  background-color: rgba(0, 0, 0, 0.47);
}
.navbar-header {
  padding: 0px 15px 0px 0px;
  float: left;
}
.logo-header {
  display: block;
  width: 180px;
  margin: 7px 60px 7px 0px;
}

.navbar-collapse-wrapper {
  display: flex;
  float: left;
  margin: 10px -15px 0px;
  padding: 0px 15px;
}

#navbar-content {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

#navbar-content .caret {
  color:#fff;
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px solid;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}

#navbar-content li {
  margin-right: 20px;
  margin-bottom: 8px;
  display: inline;
}

#navbar-content a {
  color: #fff;
  text-decoration: none;
  font-weight: bold;
  display: inline-block;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  text-transform: uppercase;
  border-bottom: 3px solid transparent;
  transition: border-color 400ms;
}
#navbar-content a:hover {
  border-bottom: 3px solid #f14d34;
}

.block-main-header {
  position: relative;
  display: flex;
  flex-direction: column;
}
.block-main-background video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 5;
  filter: blur(3px);
  transform: scale(1.04);
}

.block-main {
  position: relative;
  z-index: 15;
  padding-top: 140px;
}

.main-title,
.main-description,
.main-contact-btn {
  font-family: Montserrat;
  color: #fff;
}

.main-title {
  font-size: 52px;
  line-height: 60px;
  font-weight: bold;
  margin-top: 0;
  margin-bottom: 20px;
}

.main-description {
  font-size: 18px;
  line-height: 1.6;
  font-weight: 500;
  color: rgba(255, 255, 255, 0.8);
  margin-bottom: 55px;
}

.main-contact-btn {
  display: inline-block;
  font-weight: 500;
  font-size: 12px;
  text-transform: uppercase;
  line-height: 1;
  color: #fff;
  text-decoration: none;
  padding: 22px 20px;
  width: 220px;
  max-width: 100%;
  text-align: center;
  border: 2px solid #f14d34;
  border-radius: 5px;
  transition: background 500ms;
}
.main-contact-btn:hover {
  background-color: #f14d34;
  transition: 0.5s;
}

.support-achievement-wrapper {
  border-left: 3px solid #f14d34;
  padding: 5px;
  margin: 0;
}
.support-achievement-title {
  font-size: 24px;
  color: #fff;
  font-weight: bold;
  line-height: 1;
  margin-left: 5px;
}

.support-achievement-description {
  font-weight: 500;
  font-size: 12px;
  line-height: 1.25;
  color: rgba(255, 255, 255, 0.7);
  margin-left: 5px;
}
</style>
