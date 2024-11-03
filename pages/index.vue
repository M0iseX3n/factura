<template>
    <div>
        <cabezote
         :productos="comprasrealizadas"
        ></cabezote>

        <manager
         :productos="productos"
         @compra="compra">
        </manager>

        <footer class="vivi" > <center> Collector Shoe's
      </center> </footer>

    </div>
    
</template>
<script>
import cabezote from '~/components/cabezote.vue'
export default {
  components: { cabezote },
    data() {
        return {
         
          comprasrealizadas : [],
          productos : [
            {
                imagen : 'https://img.freepik.com/foto-gratis/zapatos-cuero-marron_1203-8175.jpg',
                precio :  290,
                titulo : 'Zapato clasico ',
                descripcion : 'fgf'
            },
             {
                imagen : 'https://http2.mlstatic.com/D_696111-MLA70741601961_072023-C.jpg',
                precio : 3000,
                titulo : 'zapato juvenil',
                descripcion : 'HGHGFHJF',

             } ,
             {
                imagen : 'https://azzurry.com/wp-content/uploads/2023/10/0251_BQ6806-122.jpg',
                precio : 3000,
                titulo : 'Nike Blazer',
                descripcion : 'HGHGFHJF',

             } ,
             {
                imagen : 'https://d2cva83hdk3bwc.cloudfront.net/onitsuka-tiger-mexico-66-yellow-black-1.jpg',
                precio : 3000,
                titulo : 'Onitsika tiger mexico 66',
                descripcion : 'HGHGFHJF',

             } ,
             {
                imagen : 'https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/3bbecbdf584e40398446a8bf0117cf62_9366/Tenis_Samba_OG_Blanco_B75806_01_standard.jpg',
                precio : 3000,
                titulo : 'Adidas Samba',
                descripcion : 'HGHGFHJF',

             } ,
             {
                imagen : 'https://pufferreds.com/cdn/shop/files/A07893C-1.png?v=1714629148',
                precio : 3000,
                titulo : 'Converse one star',
                descripcion : 'HGHGFHJF',

             } ,

          ]
            

                               
           
        }
    },
    methods: {
      compra(data){
         this.comprasrealizadas.push(data)
      }
    },
    
}
</script>

<style>
.vivi {
   padding:30px ;
   background-color: #333;
   color:#000
}
</style>