<script setup>
import { ref } from 'vue';
import coracao from "./assets/coracao.png";
import cheio from "./assets/cheio.png";

 const estadoCoracao1 = ref(coracao);
 const estadoCoracao2 = ref(coracao);
 const estadoCoracao3 = ref(coracao);

 const trocarCoracao1 = () => { estadoCoracao1.value = estadoCoracao1.value === coracao ? cheio : coracao; };
 const trocarCoracao2 = () => { estadoCoracao2.value = estadoCoracao2.value === coracao ? cheio : coracao; };
 const trocarCoracao3 = () => { estadoCoracao3.value = estadoCoracao3.value === coracao ? cheio : coracao; };

</script>

<template>
  <header>
    <h1>Vue</h1>
    <input type="text" placeholder="Pesquisar no blog">
  </header>
  <main>
    <section>
      <div>
        <h4>17 de ago, 2024</h4>
        <!-- Diretivas do Vue: -->
        <!-- para renderizar um dado da lógica, se for em uma tag usar chaves duplas <p>{{  }}<\p>. Se for dentro de um atributo usar v-bind, atalho : -->
        <img @click="trocarCoracao1" :src= "estadoCoracao1" alt="coração">
      </div>
      <h3>O que é linguagem de programação? Conheça as principais</h3>
      <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
    </section>
    <section>
      <div>
        <h4>17 de ago, 2024</h4>
        <img @click="trocarCoracao2" :src= "estadoCoracao2" alt="coração">
      </div>
      <h3>O que é linguagem de programação? Conheça as principais</h3>
      <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
    </section>
    <section>
      <div>
        <h4>17 de ago, 2024</h4>
        <img @click="trocarCoracao3" :src= "estadoCoracao3" alt="coração">
      </div>
      <h3>O que é linguagem de programação? Conheça as principais</h3>
      <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
    </section>
  </main>
</template>

<style scoped lang="scss">
header{
  background-color: rgba(23, 23, 26, 1);
  height: 20vh;
  text-align: center;
}

h1{
  padding: 23px;
  color: rgba(224, 123, 103, 1);
}

main{
  background-color: rgb(16, 16, 18);
  height: 80vh;
  width: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

input{
  background-color: rgba(32, 32, 36, 1);
  width: 50vw;
  height: 4vh;
  font-family: "Inter", sans-serif;
  font-size: 14px;
  padding: 7px;
  border: solid 1px rgba(37, 37, 41, 1);
  color:rgba(175, 171, 182, 1);

  &:hover{
    border: solid 1px rgba(224, 123, 103, 1);
    color: rgba(224, 123, 103, 1);
  }
}

section{
  width: 50vw;
  height: 20vh;
  background-color: rgba(23, 23, 26, 1);
  border: solid 2px rgba(37, 37, 41, 1);
  border-radius: 4px;
  margin: 15px;

  &:hover{
    border: 2px solid rgba(224, 123, 103, 1);
  }
}

p{
    color: rgba(175, 171, 182, 1);
    font-family: "Inter", sans-serif;
    margin: 6px 12px;
    font-size: 14px;
  }

  h4{
    color: rgba(224, 123, 103, 1);
    font-size: 11px;
    font-family: "Inter", sans-serif;
    font-weight: 200;
    margin: 20px 8px;
  }

div{
  height: 5vh;
  width: 48vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 6px;
}

img{
    height: 15px;
    
    &:hover{
      cursor: pointer;
      transform: scale(1.3); 
    
    }
  }

  h3{
    color: rgba(255, 255, 255, 1);
    font-size: 15px;
    font-family: "Space Grotesk", sans-serif;
    font-weight: 200;
    margin: 7px 12px;
  }
</style>
