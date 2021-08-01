<template>
  <div>
      <li>
      <div v-if="!tarea.modificable">{{ tarea.$index + 1 }}: {{ tarea.texto }} <button @click="borrar(tarea)">Eliminar</button></div>
      <!--<input v-if="tarea.modificable" type="text" v-model="tarea.texto" />
      <button @click="modificar(tarea)">M</button> -->
  </li>
  </div>
</template>

<script>
export default {
  name: 'TodoListItem',
  props: {
    tarea: {
      type: Object,
      required: true,
    },
  },
  methods: {
    borrar(tarea) {
      this.$emit('borrar-tarea', tarea)
    },
  },
}
</script>

<style></style>