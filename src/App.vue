<template>
  <div id="app" class="w-50 m-auto text-center">
    <h1 class="text-center">TABLA DE USUARIOS</h1>
    <table class="table table-hover">
      <thead>
        <tr class="table-dark">
          <th scope="col">#</th>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido</th>
          <th scope="col">run</th>
          <th scope="col">nacimiento</th>
          <th scope="col">edad</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(persona, index) in personas" :key="index">
          <th scope="row">{{ index + 1 }}</th>
          <td class="table-danger">{{ persona.nombre }}</td>
          <td class="table-primary">{{ persona.apellido }}</td>
          <td class="table-success">{{ persona.run }}</td>
          <td class="table-warning">{{ persona.nacimiento }}</td>
          <td class="table-info">{{ persona.edad }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      personas: [
        {
          nombre: "Jose",
          apellido: "Perez",
          run: "123456-2",
          nacimiento: "12.04-67",
          edad: 52,
        },
        {
          nombre: "María",
          apellido: "Gonzalez",
          run: "123456-2",
          nacimiento: "12-04-67",
          edad: 29,
        },
        {
          nombre: "Manuel",
          apellido: "Dominguez",
          run: "123456-2",
          nacimiento: "12-04-67",
          edad: 60,
        },
      ],
    };
  },
};

</script>
