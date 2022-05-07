<template>
  <div class="text-center">
    <h2
      class="
        font-mono font-black
        italic
        underline
        mt-8
        py-10
        px-6
        mb-0.5
        text-lg
        md:text-2xl
        lg:text-4xl
      "
    >
      O Que será ensinado no curso
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
  </div>
</template>

<script>
export default {
  name: "Conteudo",
};
</script>

<style>
.um,
.dois,
.tres,
.quatro {
  border: 2px black solid;
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
</style>
