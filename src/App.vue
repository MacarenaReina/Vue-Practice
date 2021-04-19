<template>
  <v-app id="inspire">
    <v-system-bar app>
      <v-spacer></v-spacer>
      <v-icon>mdi-square</v-icon>
      <v-icon>mdi-circle</v-icon>
      <v-icon>mdi-triangle</v-icon>
    </v-system-bar>

    <v-app-bar app class="deep-purple lighten-2">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Welcome to my Vue practices!</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <!--  -->
    </v-navigation-drawer>

    <v-main class="grey lighten-2">
      <v-container>
        <v-row>
          <template v-for="n in 3">
            <v-col
              v-for="j in 4"
              :key="`${n}${j}`"
              cols="4"
              md="3"
            >
              <v-sheet height="150"></v-sheet>
              <v-btn block tile class="deep-purple lighten-3">
                Block Button
              </v-btn>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({ drawer: null }),
  }
</script>
