<template>
  <div>
    <h2>Editace projektu</h2>
    <table>
      <thead>
        <tr>
          <th v-for="property in properties" :key="property">{{ property }}</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td v-for="property in properties" :key="property">
            <input v-model="newRow[property]" type="text">
          </td>
        </tr>
        <tr v-for="(row, rowIndex) in rows" :key="rowIndex">
          <td v-for="property in properties" :key="property">{{ row[property] }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      properties: ["Název taxonu česky", "Výška", "Průměr kmene"],
      rows: [],
      newRow: {}
    };
  },
  methods: {
    addRow() {
      this.rows.push({ ...this.newRow });
      this.newRow = {};
    }
  }
};
</script>
