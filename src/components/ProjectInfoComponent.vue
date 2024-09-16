<template>
  <div>
    <h1>Tvorba a správa projektů</h1>
    <div>
      <label>Název projektu:</label>
      <input v-model="projectName" type="text" placeholder="Zadejte název projektu">
    </div>
    <div>
      <label>Autor:</label>
      <input v-model="author" type="text" placeholder="Zadejte autora">
    </div>
    <div>
      <label>Lokace:</label>
      <input v-model="location" type="text" placeholder="Zadejte lokaci">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projectName: '',
      author: '',
      location: ''
    };
  }
};
</script>
