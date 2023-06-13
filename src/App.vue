<template>
  <div>
    <HeaderComponent />
    <TableContainer />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent";
import TableContainer from "./components/TableContainer";

export default {
  name: "App",
  components: {
    HeaderComponent,
    TableContainer,
  },
};
</script>
