<template>
<v-app>
  <div id="app">
    <v-app-bar>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="flex text-xs-center">PC Builder</v-toolbar-title>
      <v-tooltip bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn 
            icon
            v-bind="attrs"
            v-on="on"
            @click="$vuetify.theme.dark = !$vuetify.theme.dark;"
          >
            <v-icon>fa-adjust</v-icon>
          </v-btn>
        </template>
        <span>Change Theme</span>
      </v-tooltip>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
    <v-tabs vertical>
      <v-tab to="/">
        <v-icon left>
          fa-home
        </v-icon>
        Home
      </v-tab>
      <v-tab to="/about">
        <v-icon left>
          fa-question
        </v-icon>
        About
      </v-tab>
      <v-tab>
        <v-icon left>
          mdi-access-point
        </v-icon>
        Option 3
      </v-tab>
    </v-tabs>
    </v-navigation-drawer>
    <v-main>
      <transition>
        <router-view></router-view>
      </transition>
    </v-main>
  </div>
</v-app>
</template>

<script>
export default {
  data: () => ({
        drawer: false,
        group: null,
      }),

      watch: {
      group () {
        this.drawer = false
      },
    },
}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

html {
  overflow-y: auto
}

</style>
