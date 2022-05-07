<template>
  <div class="mt-8">
    <a class="comprar" href="#">
      <span class="top-key"></span>
      <span class="text">QUERO MINHA VAGA</span>
      <span class="bottom-key-1"></span>
      <span class="bottom-key-2"></span>
    </a>
  </div>
</template>

<script>
export default {
  name: "comprar",
};
</script>

<style>
.comprar {
  /* From uiverse.io */
  background-color: transparent;
  border: 2px solid #000;
  border-radius: 0;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-weight: 700;
  letter-spacing: 0.05em;
  margin: 0;
  outline: none;
  overflow: visible;
  padding: 1.25em 2em;
  position: relative;
  text-align: center;
  text-decoration: none;
  text-transform: none;
  transition: all 0.3s ease-in-out;
  user-select: none;
  font-size: 16px;
}

.comprar::before {
  content: " ";
  width: 2.5625rem;
  height: 2px;
  background: teal;
  top: 50%;
  left: 1.5em;
  position: absolute;
  transform: translateY(-50%);
  transform-origin: center;
  transition: background 0.3s linear, width 0.3s linear;
}

.comprar .text {
  font-size: 2.125em;
  line-height: 1.33333em;
  padding-left: 2em;
  display: block;
  text-align: left;
  transition: all 0.3s ease-in-out;
  text-transform: uppercase;
  text-decoration: none;
  color: teal;
}

.comprar .top-key {
  height: 2px;
  width: 2.5625rem;
  top: -2px;
  left: 0.625rem;
  position: absolute;
  background: #e8e8e8;
  transition: width 0.5s ease-out, left 0.3s ease-out;
}

.comprar .bottom-key-1 {
  height: 2px;
  width: 2.5625rem;
  right: 1.875rem;
  bottom: -2px;
  position: absolute;
  background: #e8e8e8;
  transition: width 0.5s ease-out, right 0.3s ease-out;
}

.comprar .bottom-key-2 {
  height: 2px;
  width: 0.625rem;
  right: 0.625rem;
  bottom: -2px;
  position: absolute;
  background: #e8e8e8;
  transition: width 0.5s ease-out, right 0.3s ease-out;
}

.comprar:hover {
  color: white;
  background: black;
}

.comprar:hover::before {
  width: 0.9375rem;
  background: white;
}

.comprar:hover .text {
  color: white;
  padding-left: 1.5em;
}

.comprar:hover .top-key {
  left: -2px;
  width: 0px;
}

.comprar:hover .bottom-key-1,
.comprar:hover .bottom-key-2 {
  right: 0;
  width: 0;
}
</style>