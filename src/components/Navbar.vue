<template>
  <!-- Creación del navbar -->
  <div>      
      <v-app-bar app dark>
          <v-btn @click="drawer = true" class="d-flex d-sm-none" icon elevation="0"> 
              <v-icon>fa-solid fa-bars</v-icon>
          </v-btn>
          <div class="d-flex align-center" :to="'/'">
              <v-img
                alt="logo"
                class="shrink mr-2 image"
                contain
                src="@/assets/icons/logo.png"
                width="150"                
              >                  
              </v-img>
          </div>
          <template>
              <v-tabs v-model="tab" align-with-title class="d-none d-sm-flex">
                  <v-tabs-slider color="white"></v-tabs-slider>
                  <v-tab v-for="item in items" :key="item.id" :to="item.url">
                      {{item.name}}
                  </v-tab>
              </v-tabs>
          </template>
          <v-spacer></v-spacer>
          <v-btn color="green" text :to="'/signin'">
              <span class="mr-2">Sign in</span>
              <v-icon>fa-solid fa-user</v-icon>
          </v-btn>
      </v-app-bar>
      
      <v-navigation-drawer v-model="drawer" absolute temporary bottom>
          <v-list nav dense>
              <v-list-item-group active-class="deep-purple--text text--accent-4">
                  <v-list-item
                    v-for="item in items"
                    :key="item.id"
                    :to="item.url"
                    :class="`${item.btn ? '' : 'd-none'}`"
                  >                      
                    <v-list-item-icon>
                        <v-icon>
                            {{item.icon}}
                        </v-icon>
                    </v-list-item-icon>
                    <v-list-item-title @click="tab = index">
                        {{item.name}}
                    </v-list-item-title>
                  </v-list-item>
              </v-list-item-group>
          </v-list>
      </v-navigation-drawer>
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
                icon: "fas fa-home"
            },
            {
                name: "Meta",
                url: "/meta",
                btn: true,
                icon: "fas fa-code-branch"
            },
            {
                name: "Company",
                url: "/company",
                btn: true,
                icon: "fas fa-building"
            },
            {
                name: "Support",
                url: "/support",
                btn: true,
                icon: "fas fa-cog"
            },
            {
                name: "Contact",
                url: "/contact",
                btn: true,
                icon: "fas fa-phone-alt"
            },
        ]
    })
}
</script>

<style>
.image{
    cursor: pointer;
}
</style>