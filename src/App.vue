<template>
  <div id="app">
    <!--projects start-->
    <Projects />
    <!--projects end-->
    <!--donate start-->
    <Donate />
    <!--donate end-->
  </div>
</template>

<script>
import Projects from '@/components/Projects.vue';
import Donate from '@/components/Donate.vue';

export default {
  name: 'App',
  components: { Projects, Donate },
  }
</script>
