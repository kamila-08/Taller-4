<template>
    <div class="enlaces-interes">
      <h2>Enlaces de interés</h2>
      <ul>
        <li v-for="enlace in enlaces" :key="enlace.url">
          <a :href="enlace.url">{{ enlace.text }}</a>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      enlaces: Array,
    },
  };
  </script>
  
  <style lang="scss" scoped>
  ul {
    list-style: underline; 
    padding:5; 
  }
  
  li {
    margin-bottom: 10px;
  }
  a {
    color: purple;
    text-decoration: underline;
    justify-content: center;
    font-family: Arial, Helvetica, sans-serif;
  }
  </style>
  