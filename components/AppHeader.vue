<template>
  <header class="header">
    <div>
      <h1
        class="
          font-mono
          bg-black
          py-10
          px-6
          mb-0.5
          text-lg
          md:text-2xl
          lg:text-4xl
          text-center text-white
          rounded-b-full
        "
      >
        Aprenda Tudo o Que Precisa Para Ter uma Loja de Sucesso
      </h1>
    </div>
    <div
      class="font-mono bg-grey text-center py-5 text-base md:text-lg lg:text-xl"
      v-if="timerCount > 0"
    >
      <h2>
        Em {{ timerCount }} Segundos você receberar uma oportunidade única
      </h2>
    </div>
    <div
      class="font-mono bg-grey text-center py-5 text-base md:text-lg lg:text-xl"
      v-else
    >
      <h2>Desça a página e veja a melhor oportunidade de sua vida</h2>
    </div>
    <VideoPlayer />
    <transition name="slide-fade">
      <div class="div-btn" v-if="timerCount <= 0">
        <BtnCompra />
        <Conteudo />
      </div>
    </transition>
  </header>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {
      timerCount: 15,
    };
  },

  watch: {
    timerCount: {
      handler(value) {
        if (value > 0) {
          setTimeout(() => {
            this.timerCount--;
          }, 1000);
        }
      },
      immediate: true, // This ensures the watcher is triggered upon creation
    },
  },
};
</script>

<style>
.div-btn {
  text-align: center;
  padding-top: 1.5rem;
  background: #0f2027; /* fallback for old browsers */
  background: -webkit-linear-gradient(black, grey);
  background: linear-gradient(black, rgb(87, 87, 87));
}
.slide-fade-enter-active {
  transition: all 1s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>
