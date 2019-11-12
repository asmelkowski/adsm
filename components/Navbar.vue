<template>
<div>
  <v-toolbar max-height="60">
    <v-toolbar-title>Title</v-toolbar-title>

    <v-spacer></v-spacer>

    <template v-if="$vuetify.breakpoint.smAndUp">
      <v-toolbar-items>
        <v-btn text>Link 1</v-btn>
        <v-btn text>Link 2</v-btn>
        <v-btn text>Link 3</v-btn>
      </v-toolbar-items>
    </template>
    <template v-else>
      <svg @click.stop="drawer=!drawer" style="width:40px;height:40px;cursor:pointer" viewBox="0 0 24 24">
        <path fill="#ffffff" d="M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z" />
      </svg>
    </template>
  </v-toolbar>
  <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      right
      mini-variant
    >
      <v-list-item>
          <svg @click.stop="drawer=!drawer" style="width:40px;height:40px;cursor:pointer;" viewBox="0 0 24 24">
    <path fill="#ffffff" d="M13.46,12L19,17.54V19H17.54L12,13.46L6.46,19H5V17.54L10.54,12L5,6.46V5H6.46L12,10.54L17.54,5H19V6.46L13.46,12Z" />
</svg>
      </v-list-item>

      <v-list dense>

        <v-list-item>
          <v-list-item-content>
            <v-list-item-title>Link 1</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title>Link 2</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title>Link 3</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</div>
</template>
<script>
export default {
  name: 'Navbar',
  data() {
    return {
        drawer: false
    }
  }
}
</script>
<style scoped>
</style>