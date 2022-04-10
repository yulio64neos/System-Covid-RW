<template>
  <div>
    <v-container fluid>
      <v-col>
        <v-row class="d-flex justify-center">
          <v-col cols="12" md="6" class="">
            <v-row class="align-center justify-center">
              <v-col cols="10" sm="7" md="8">
                <v-skeleton-loader
                  width="100%"
                  :height="`${$vuetify.breakpoint.mobile ? '75' : '130'}`"
                  type="image"
                  :loading="loading"
                  :class="`${$vuetify.breakpoint.mobile ? '' : 'my-8'}`"
                >
                  <v-img src="@/assets/images/coronovirus.jpg"> </v-img>
                </v-skeleton-loader>
              </v-col>
              <v-col cols="10" class="my-3">
                <v-skeleton-loader
                  type="text@5"
                  :loading="loading"
                  width="100%"
                  :class="`${loading ? 'mt-2' : ''}`"
                >
                  <v-badge
                    left
                    icon= "fas fa-info"
                  >
                    <p class="text-justify text-normal font-italic texto">
                      "El Covid-19 proviene de una familia de virus que causan
                      enfermedades (Desde el resfriado común hasta enfermedades
                      respiratorias más graves) donde se da tanto en humanos
                      como en animales." -Gobierno de México (2022)-
                    </p>
                  </v-badge>
                </v-skeleton-loader>
                <v-btn rounded class="text-none gob" color="gobierno" href="https://coronavirus.gob.mx/covid-19/">
                    Visite la página del Gobierno
                </v-btn>
              </v-col>              
            </v-row>
            <v-row>
                <v-col cols="12" class="primary justify-center d-flex" sm="8">

                </v-col>
            </v-row>
          </v-col>
          <v-col cols="10" sm="8" md="6" class="">
            <v-img>
              <v-img
                src="@/assets/images/Protected.png"
                contain
                max-height="500"
              >
              </v-img>
            </v-img>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    loading: false,
  }),
};
</script>

<style scoped>
.texto{    
    font-size: 18px;
}
.gob{
    color: white !important;
}
</style>