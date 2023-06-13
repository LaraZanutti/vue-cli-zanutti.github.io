<template>
  <div class="container d-flex flex-column">
    <TableComponent
      v-for="(tabla, index) in tablas"
      :key="index"
      :titulo="tabla.titulo"
      :clase="tabla.clase"
      :medidas="tabla.medidas"
    />
  </div>
</template>

<script>
import TableComponent from "./TableComponent";

export default {
  components: {
    TableComponent,
  },
  data() {
    return {
      tablas: [
        {
          titulo: "Hombre",
          clase: "table-danger",
          medidas: [
            {
              medida: "Cintura",
              XS: "76",
              S: "80",
              M: "84",
              L: "88",
              XL: "92",
              XXL: "96",
            },
            {
              medida: "Tiro",
              XS: "28",
              S: "29",
              M: "29",
              L: "30",
              XL: "31",
              XXL: "32",
            },
            {
              medida: "Largo",
              XS: "106",
              S: "106",
              M: "109",
              L: "109",
              XL: "109",
              XXL: "110",
            },
          ],
        },
        {
          titulo: "Mujer",
          clase: "table-success",
          medidas: [
            {
              medida: "Cintura",
              XS: "68",
              S: "72",
              M: "76",
              L: "80",
              XL: "84",
              XXL: "88",
            },
            {
              medida: "Tiro",
              XS: "25",
              S: "26",
              M: "26",
              L: "27",
              XL: "27",
              XXL: "28",
            },
            {
              medida: "Largo",
              XS: "102",
              S: "102",
              M: "102",
              L: "102",
              XL: "103",
              XXL: "104",
            },
          ],
        },
        {
          titulo: "Niño",
          clase: "table-warning",
          medidas: [
            {
              medida: "Cintura",
              XS: "52",
              S: "54",
              M: "56",
              L: "58",
              XL: "62",
              XXL: "64",
            },
            {
              medida: "Tiro",
              XS: "21",
              S: "21",
              M: "22",
              L: "23",
              XL: "23",
              XXL: "23",
            },
            {
              medida: "Largo",
              XS: "38",
              S: "42",
              M: "48",
              L: "57",
              XL: "65",
              XXL: "71",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
</style>