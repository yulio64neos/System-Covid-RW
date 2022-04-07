<template>
  <!-- Creación del navbar -->
  <div>      
      <v-app-bar app dark>
          <v-btn @click="drawer = true" class="d-flex d-sm-none" icon elevation="0"> 
              <v-icon>fa-solid fa-bars</v-icon>
          </v-btn>
      </v-app-bar>
  </div>
</template>

<script>
export default {
    name: "App",

    data:() => ({
        drawer: false,
        tab: null,
        items: [
            {
                name: "Home",
                url: "/",
                btn: true,
                icon: "fas fa*home"
            },
            {
                name: "Meta",
                url: "/meta",
                btn: true,
                icon: "fas fa*home"
            },
            {
                name: "Company",
                url: "/company",
                btn: true,
                icon: "fas fa*home"
            },
            {
                name: "Support",
                url: "/support",
                btn: true,
                icon: "fas fa*home"
            },
            {
                name: "Contact",
                url: "/contact",
                btn: true,
                icon: "fas fa*home"
            },
        ]
    })
}
</script>

<style>

</style>