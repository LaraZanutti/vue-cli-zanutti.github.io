<template>
  <div>
    <div :class="titulo">
      {{ titulo }}
    </div>
    <table class="table table-striped table-hover border text-center mb-5">
      <thead>
        <tr>
          <th v-for="(header, indexH) of headers" :key="indexH">
            {{ header }}
          </th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(medida, indexM) of medidas" :key="indexM" :class="clase">
          <td class="fw-semibold">{{ medida.medida }}</td>
          <td>{{ medida.XS }}</td>
          <td>{{ medida.S }}</td>
          <td>{{ medida.M }}</td>
          <td>{{ medida.L }}</td>
          <td>{{ medida.XL }}</td>
          <td>{{ medida.XXL }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
    props:{
        titulo:String,
        clase:String,
        medidas:Array

    },
  data() {
    return {
      headers: ["Talle", "XS", "S", "M", "L", "XL", "XXL"],
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@100;200;300;400;500&display=swap');

.Hombre {
    background-color: rgb(182, 16, 16);
    font-size: 30px;
    padding-left: 10px;
    color: #fff;
    text-transform: uppercase;
    font-weight: 700;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.Mujer {
    background-color: rgb(100, 150, 94);
    font-size: 30px;
    padding-left: 10px;
    color: #fff;
    text-transform: uppercase;
    font-weight: 700;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.Niño {
    background-color: #f6db81;
    font-size: 30px;
    padding-left: 10px;
    color: #FFF;
    text-transform: uppercase;
    font-weight: 700;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.titulo{
    font-family: 'Great Vibes', cursive;
    font-size: 75px;
    font-weight: 550;
    transition: all .5s ease-in-out;
}

.titulo:hover{
    transform: scale(1.25);
    color: rgb(182, 16, 16);
}

</style>