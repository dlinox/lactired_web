<template>
  <pre>
    {{ plantas }}
  </pre>
</template>
<script setup>
const plantas = ref(null);
const init = async () => {
  let res = await fetch("https://infocir-lactired.linox.net.pe/api/plantas");
  let json = await res.json();
  plantas.value = json;
  console.log(json);
};

init();
</script>
