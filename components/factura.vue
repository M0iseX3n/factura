<template>
  <v-dialog v-model="mostrar" width="auto" persistent>
    <v-card max-width="500" title="Productos Comprados">
      <v-card-text>
        <div v-for="(producto, index) in compras" :key="index">
          <v-card outlined class="mb-4 d-flex justify-space-between">
            <div class="d-flex">

              <v-img :src="producto.imagen" height="150px" width="100px"></v-img>
              
              <div class="ml-4">
                <v-card-title>{{ producto.titulo }}</v-card-title>
                <v-card-subtitle>{{ producto.descripcion }}</v-card-subtitle>
                <v-card-text>Precio: {{ producto.precio }}</v-card-text>
              </div>
            </div>
            <v-btn color="red" @click="eliminarProducto(index)">Eliminar</v-btn>
          </v-card>
        </div>
      </v-card-text>
      <v-card-actions>
        <v-btn class="ms-auto" text @click="cerrar">Cerrar</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: {
    show: {
      type: Boolean,
      default: false
    },
    compras: {
      type: Array,
      default: () => [] 
    }
  },
  data() {
    return {
      mostrar: false 
    };
  },
  methods: {
    cerrar() {
      this.$emit('cerrar'); 
    },
    eliminarProducto(index) {
      this.$emit('eliminar', index);
    }
  },
  watch: {
    show(newVal) {
      this.mostrar = newVal;
    }
  }
};
</script>
