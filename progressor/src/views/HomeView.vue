<template>
  <div class="home">
    <HelloWorld msg="Progressor (compo API)" />
  </div>
  <Form />
  
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Form from "@/components/form.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld, Form,
  },
};
</script>
