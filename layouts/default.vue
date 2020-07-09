<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" absolute temporary app>
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar id="home-app-bar" color="white" app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-spacer />

      <v-text-field
        v-model="search"
        :placeholder="placeholder"
        append-icon="mic"
        class="mx-4"
        flat
        hide-details
        label="Search"
        prepend-inner-icon="search"
        solo-inverted
      ></v-text-field>
    </v-app-bar>
    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- navbar -->
      <!-- Provides the application the proper gutter -->
      <v-container>
        <!-- If using vue-router -->
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    placeholder: "Digite aqui o nome, marca ou princípio ativo do produto...",
    drawer: false,
    group: null
  })
};
</script>

<style>
</style>