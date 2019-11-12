<template>
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
      <v-icon><svg style="width:24px;height:24px" viewBox="0 0 24 24">
        <path fill="#ffffff" d="M3,6H21V8H3V6M3,11H21V13H3V11M3,16H21V18H3V16Z" />
      </svg></v-icon>
    </template>
  </v-toolbar>
</template>
<script>
export default {
  name: 'Navbar'
}
</script>