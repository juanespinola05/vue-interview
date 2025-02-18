<template>
  <div>
    <h1>Listado de Materiales</h1>
    <table v-for="material in materials" :key="material.price">
      <thead>
        <tr>
          <th>Nombre</th>
          <th>Precio</th>
          <th>Espesor</th>
          <th>Medidas (mm)</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>{{ material.name }}</td>
          <td>{{ material.price }}</td> 
          <td>{{ material.espesor }}</td>
          <td>
            <img width="50" height="50" :src="material.textura" alt="Textura">
          </td>
          <td>{{ material.ancho }}x{{ material.largo }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
export default {
  name: "MaterialList",
  data () {
    return {
      materials: []
    }
  },
  mounted () {
  },
  methods: {
    async loadMaterials() {
      // '/materials.json' es la url de la ruta
    }
  }
}
</script>