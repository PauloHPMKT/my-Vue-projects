<template>
  <div class="card">
    <img v-bind:src="avatar" :alt="description">
    <h1 class="title">{{ nome }}</h1>
    <p>
      Desenvolvedor web Fullstack e criador e administrador de conteúdo para o perfil Dev++
    </p>
    <div class="list-social-icons">
      <ul>
        <li v-for="(social, id) in list_social" v-bind:key="id">
          {{ social }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Card', 
    data() {
      return {
        nome: 'Paulo Sérgio',
        avatar: './public/avatar-pic.png',
        description: 'avatar Paulo',
        list_social: ['Instagram', 'GitHub', 'Linkedin'],
        links_social: [
          'http://www.instagram.com/dev.mais',
          'https://www.github.com/PauloHPMKT',
          'https://www.linkedin.com/in/paulo-sergio-frontend-dev/',
        ]

      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    font-family: 'Roboto', sans-serif;
    color: #fff;
  }

  .list-social-icons {
    margin: 30px 0;
  }
  ul {
    list-style: none;
    display: flex;
    justify-content: center;
  }

  li {
    margin: 10px;
    background-color: #023b47;
    padding: 15px;
    border-radius: 10px;
  }

  a {
    text-decoration: none;
    color: #fff;
  }

  .card {
    background-image: linear-gradient(#351fc56c, #149ebd);
    width: 500px;
    height: 700px;
    border-radius: 20px;
    box-shadow: 0 0 35px rgba(0, 0, 0, 0.411);
    text-align: center;
    padding: 100px 80px;
  }

  img {
    width: 180px;
    border-radius: 100%;
    margin: 20px;
    border: 3px solid rgba(51, 51, 51, 0.288);
  }

  .title {
    letter-spacing: 1px;
    font-weight: 400;
    font-size: 45px;
    margin-bottom: 10px;
  }


</style>-->