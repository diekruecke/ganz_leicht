<template>
  <div class="own_hpMaster">
    <table class="own_table">
      <thead>
        <tr class="own_header">
          <td colspan="2">
            <div class="own_header_links">
              <div class="own_logo" />
              <div class="own_text_big">
                Monika Schönwald
              </div>
              TouchLife Praktikerin<br />
              Ganzheitliche Massage<br />
            </div>
            <div class="own_header_rechts">
              Raum für Entspannung und Wahrnehmung
            </div>
          </td>
        </tr>
      </thead>
      <tbody style="background-color: white;">
        <tr style="vertical-align: top;">
          <td class="own_navigation">
            <div v-for="nav in navigation" :key="nav.name" class="own_nav">
              <nuxt-link :to="nav.to">{{ nav.name }}</nuxt-link>
            </div>
          </td>
          <td class="own_content">
            <nuxt />
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navigation: [
        { name: 'ganzleicht', to: '/' },
        { name: 'wirkung', to: '/wirkung' },
        { name: 'behandlung', to: '/behandlung' },
        { name: 'produkte', to: '/produkte' },
        { name: 'preise', to: '/preise' },
        { name: 'kontakt', to: 'kontakt' }
      ]
    }
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  background-color: #c0c0c0;
}

*,
*:before,
*:after {
  margin: 0;
}

.own_hpMaster {
  margin: auto;
  width: 950px;
  padding-bottom: 20px;
  padding-top: 20px;
  background-color: #e4eee8;
}

.own_header {
  background-image: url(/home.jpg);
  height: 325px;
  vertical-align: bottom;
  background-color: none;
}

.own_logo {
  background-image: url(/logo.png);
  width: 197px;
  height: 64px;
  margin-bottom: 25px;
}

.own_header_links {
  float: left;
  padding-left: 25px;
  padding-bottom: 30px;
  font-size: 15px;
  color: white;
}

.own_header_rechts {
  float: right;
  padding-right: 25px;
  padding-bottom: 25px;
  transform: translate(0, 125px);
  font-size: 25px;
  color: white;
}

.own_table {
  width: 903px;
  margin: auto;
}

.own_navigation {
  width: 209px;
  box-shadow: 2px 0px 4px 1px rgba(0, 0, 0, 0.2);
  background-color: #f7faf9;
  padding-top: 50px;
  padding-left: 20px;
}

.own_nav {
  padding-bottom: 10px;
}

.own_nav a {
  color: #666666;
  text-decoration: none;
}

.own_nav a:hover,
.own_nav a:active {
  color: #669999;
}

.own_content {
  padding: 50px 100px;
}

.own_title {
  font-size: 25px;
  color: #669999;
}

.own_subtitle {
  font-size: 25px;
  color: #666666;
}

.own_text {
  font-size: 15px;
  color: #959595;
  padding-top: 15px;
}

.own_text_big {
  font-weight: bold;
}
</style>
