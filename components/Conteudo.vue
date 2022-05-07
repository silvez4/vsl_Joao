<template>
  <div
    class="
      text-center
      justify-center
      align-center
      mt-8
      border-t-4 border-yellow-400
    "
  >
    <h2
      class="
        font-mono font-black
        italic
        underline
        text-white
        py-10
        px-6
        mb-0.5
        text-lg
        md:text-2xl
        lg:text-4xl
      "
    >
      O Que você irá aprender
    </h2>
    <div
      class="
        conteudo
        font-mono
        bg-grey
        text-center
        py-5
        mr-5
        ml-5
        mb-5
        text-base
        md:text-lg
        lg:text-xl
      "
    >
      <div class="um">
        <h3 class="md:m-5">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Magni,
          voluptate.
        </h3>
      </div>
      <div class="dois">
        <h3 class="md:m-5">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Magni,
          voluptate.
        </h3>
      </div>
      <div class="tres">
        <h3 class="md:m-5">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Magni,
          voluptate.
        </h3>
      </div>
      <div class="quatro">
        <h3 class="md:m-5">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Magni,
          voluptate.
        </h3>
      </div>
    </div>
    <BtnCompra />
    <Footer />
  </div>
</template>

<script>
import BtnCompra from "./BtnCompra.vue";
export default {
  components: { BtnCompra },
  name: "Conteudo",
};
</script>

<style>
.um,
.tres {
  border-left: 2px black solid;
  border-bottom: 2px black solid;
}
.dois,
.quatro {
  border-right: 2px black solid;
  border-bottom: 2px black solid;
}
.um {
  grid-area: um;
}
.dois {
  grid-area: dois;
}
.tres {
  grid-area: tres;
}
.quatro {
  grid-area: quatro;
}

.conteudo {
  padding: 2rem 0 1rem 0;
  display: grid;
  grid-template-rows: repeat(4, 1fr);
  grid-template-columns: repeat(2, 1fr);
  grid-template-areas:
    "um ."
    ". dois"
    "tres ."
    ". quatro";
}
@media (max-width: 600px) {
  .conteudo {
    grid-template-columns: 1fr;
    grid-template-areas:
      "um"
      "dois"
      "tres"
      "quatro";
  }
  .um,
  .dois,
  .tres,
  .quatro {
    padding: 2rem 0.25rem;
  }
}
</style>
