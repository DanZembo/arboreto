<template>
  <div>
    <h3>Přidat vlastnost (sloupec)</h3>
    <ul>
      <li v-for="property in availableProperties" :key="property" @click="toggleProperty(property)">
        {{ property }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      availableProperties: [
        "Název taxonu česky", "Název taxonu latinsky", "Průměr kmene", "Obvod kmene", "Výška"
      ],
      selectedProperties: []
    };
  },
  methods: {
    toggleProperty(property) {
      const index = this.selectedProperties.indexOf(property);
      if (index === -1) {
        this.selectedProperties.push(property);
      } else {
        this.selectedProperties.splice(index, 1);
      }
    }
  }
};
</script>
