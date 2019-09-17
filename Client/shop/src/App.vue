<template>
 <v-card
    class="mx-auto overflow-hidden"

  >
    <v-system-bar color="#673AB7"></v-system-bar>
    <v-app-bar
      color="#673AB7"
      dark
      prominent
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Store</v-toolbar-title>
      <div class="flex-grow-1"></div>

      <v-btn style="margin-left: 1000px;" icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      bottom
      temporary
    >
      <v-list
        nav
        dense
      >
      
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Home  <i class="fas fa-home"></i></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Catalog</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>About Us</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Contact Us</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-card-text>
      The navigation drawer will appear from the bottom on smaller size screens.
      <v-icon dark>home</v-icon>
    </v-card-text>
  </v-card>
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

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
