<template>
    <div>
        <v-badge color="error" :content="productos.length">
            <v-btn icon @click="detalle()">
                <v-icon>mdi-cart</v-icon>
              </v-btn>
          </v-badge>
       <factura 
        :show="show"
        @cerrar="cerrar"
        :compras="productos"
        @eliminar="eliminarProducto"
       ></factura>
    </div>
</template>
<script>

export default {
    props: {
    productos: {
        type: Array,
        default: []
    },
   },
    data() {
        return {
            show : false          
          }
    },
    methods : {
        detalle(){
            this.show = true
        },

        cerrar(){
            this.show = false;
        },
        eliminarProducto(index) {
      this.productos.splice(index, 1);
    }
    }
    
}
</script>