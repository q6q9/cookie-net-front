<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HomeView",
});
</script>
<template>
  <div>
    <h2>
      Hi <span class="text-danger">{{ $auth.user("name") }}</span
      >!
    </h2>
    <h3>
      {{
        $auth.check()
          ? "What are u gonna do?"
          : "For using our cookies actions u needed log in"
      }}
    </h3>
    User:
    <div>
      <h4>{{ $auth.user("email") }}</h4>
      <h4>{{ $auth.user("name") }}</h4>
    </div>
  </div>
</template>
