<template>
  <AppHeader />
</template>

<script>
export default {
  name: "Header",
  head() {
    name: "Index Page";
    return {
      meta: [
        {
          hid: "VSL",
          name: "VSL João",
          content: "Curso do joão sobre ecommerce",
        },
      ],
    };
  },
};
</script>
