<template>
  <div id="app">
    <header>
      <!-- Navbar -->
      <nav>
        <ul>
          <li class="nav-item">
            <router-link class="nav-link" :to="{name: 'Home'}" exact>
              <img class="logo" src="./assets/build-a-bot-logo.png" />
              Build-a-Bot
            </router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" :to="{name: 'Build'}" exact>
              Build
            </router-link>
          </li>
        </ul>
      </nav>
    </header>
    
    <div class="container">
      <!-- Left sidebar -->
      <aside class="aside">
        <router-view name="sidebar"/>
      </aside>

      <!-- Main page -->
      <main>
          <router-view/>
      </main>
    </div>
  </div>
</template>

<!-- Scripts -->
<script>
export default {
  name: 'app',
};
</script>

<!-- Global Styles -->
<style>
body {
  background: linear-gradient(to bottom, #555, #999);
  background-attachment: fixed;
}
</style>

<!-- Scoped Styles -->
<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
.container {
  display: flex;
  margin: 10px auto 0 auto;
  justify-content: center;
}
main {
  padding: 30px;
  background-color: white;
  width: 964px;
  min-height: 300px;
}
header {
  background-color: #999;
  width: 1184px;
  margin: 0 auto;
}
ul {
  padding: 3px;
  display: flex;
}

/* Navbar */
.nav-item {
  display: inline-block;
  padding: 5px 10px;
  font-size: 22px;
  border-right: 1px solid #bbb;
}
.nav-link {
  text-decoration: none;
  color: inherit;
}
.logo {
  vertical-align: middle;
  height: 30px;
}
.router-link-active {
  color: white;
}

/* Left sidebar aside */
.aside {
  padding: 30px;
  background-color: #aaa;
  width: 100px;
  min-height: 300px;
}
</style>
