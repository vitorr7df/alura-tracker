Skip to content
Search or jump to…
Pull requests
Issues
Codespaces
Marketplace
Explore
 
@vitorr7df 
alura-cursos
/
alura-tracker
Public
forked from rafaelbomfimjr/alura-tracker
Fork your own copy of alura-cursos/alura-tracker
Code
Pull requests
Actions
Projects
Security
Insights
alura-tracker/src/components/Box.vue

Vinicios Neves fim video 3.3
Latest commit ca58e63 on Sep 7, 2021
 History
 0 contributors
19 lines (16 sloc)  266 Bytes

<template>
  <div class="box has-text-weight-bold">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'Box-name'
})
</script>

<style scoped>
.box {
  background: #FAF0CA;
}
</style>
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
alura-tracker/Box.vue at aula-3 · alura-cursos/alura-tracker