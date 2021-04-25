<template>
  <div class="table">
    <table calss="center">
      <thead>
        <tr>
          <th v-for="(col, ix) in columns" :key="ix">{{ col.text }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(row, ix) in programData" :key="ix">
          <td v-for="(item, ix) in row" :key="ix">
            {{ item }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>

  <div>
    <ul>
      <li v-for="(row, ix) in programData" :key="ix">
        {{ row.name }}
      </li>
    </ul>
  </div>
</template>


<script>
import data from "./../data/sample_new.json";

export default {
  name: "DataTable",
  data() {
    return {
      columns: [
        { text: "LOB", format: "str" },
        { text: "Entity", format: "str" },
        { text: "TIN", format: "str" },
        { text: "Name", format: "str" },
        { text: "Epsiode Class", format: "str" },
        { text: "Episode Category", format: "str" },
        { text: "Bundle", format: "str" },
        { text: "Episode Count", format: "int" },
        { text: "Total Allowed", name: "total_allowed", format: "money" },
        { text: "AAE", format: "money" },
        { text: "PAS", format: "money" },
        { text: "LRCS", format: "money" },
        { text: "SOC", format: "money" },
        { text: "FC", format: "money" },
        { text: "Total Opportunity", format: "money" },
        { text: "Savings Rate", format: "percent" },
      ],
      programData: data,
    };
  },
  methods: {},
  computed: {},
};
</script>


<style scoped>
table,
td {
  border: 1px solid #333;
  margin-left: 50px;
  margin-right: 50px;
}

thead,
tfoot {
  background-color: rgb(82, 82, 82);
  color: #fff;
}
</style>