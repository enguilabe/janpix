<template>
  <div>
      <div class="container">
          <div class="row">
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[0]}">
                  <h2>Test Online Alternativo</h2>
                  <p class="lead mt-3 mb-5 pb-2">
                      Con este test muy rápido podremos detectar si tienes el virus COVID-19
                  </p>
                  <button type="button" class="btn btn-warning btn-block" v-on:click="test">Empecemos</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[1]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Estás teniendo tos?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[2]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Estás teniendo escalofrios?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[3]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Tienes dolor de garganta?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[4]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Estás teniendo dolor de cuerpo y malestar general?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[5]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Has tenido fiebre [para fines correctos de 37.8 ºC?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[6]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Has perdido el olfato?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[7]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Estás teniendo dificultad respiratoria? [Como si te faltará el aire]
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 2">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[8]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Estás experimentando fátiga?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 2">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[9]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Has viajado en los últimos 14 días?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 3">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[10]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Has viajado o estado en un área afectada por SARS-COV2 (COVID-19)?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 3">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[11]}">
                  <h2>Sintoma</h2>
                  <p class="lead mt-3 mb-5 pb-2 text-warning font-weight-bold">
                      ¿Has estado en contacto directo o cuidado a algún paciente positivo a SARS-COV2 (COVID-19) ?
                  </p>
                  <button type="button" class="btn btn-outline-success btn-block" v-on:click="test()">No</button>
                  <button type="button" class="btn btn-outline-danger btn-block" v-on:click="test(); labs += 3; complete += 1">Si</button>
              </div>
              <div class="col-10 offset-1 mt-4" v-bind:class="{'d-none': display[12]}">
                  <div v-if="labs<3" class="text-center">
                      <img src="@/assets/happy.svg" width="128">
                      <h4 class="title mt-5">
                          Podría ser por estrés toma tus precauciones
                      </h4>
                  </div>
                  <div v-if="labs>=3 && labs<=5" class="text-center">
                      <img src="@/assets/happy.svg" width="128">
                      <h4 class="title mt-5">
                          Hidratate, manten tus medidas de higiene y vuelva en 2 días
                      </h4>
                  </div>
                  <div v-if="labs>=6 && labs<=11" class="text-center">
                      <img src="@/assets/scare.svg" width="128">
                      <h4 class="title mt-5">
                          Acude a consulta médica
                      </h4>
                  </div>
                  <div v-if="labs>=12" class="text-center">
                      <img src="@/assets/sad.svg" width="128">
                      <h4 class="title mt-5">
                          Puedes estar infectado
                      </h4>
                      <br>
                      <h1 class="btn btn-success btn-block" >Llamar al 113</h1>
                  </div>
              </div>
          </div>
      </div>
      <div class="lab" v-bind:class="{'d-none': complete}">
          <img src="@/assets/lab.svg" width="128">
      </div>

  </div>
</template>
<style>
    .lab{
        position:absolute;
        margin-left:-64px;
        left:50%;
        bottom: -8px;
        width: 182px;
    }
</style>
<script>
    export default {
        data() {
            return {
                display: [
                    false,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                    true,
                ],
                count:0,
                labs:0,
                complete:0,
            };
        },
        methods:{
            test: function(){
                this.display.splice(this.display, this.count, true);
                /*
                this.display[0] = true
                this.count += 1;
                this.display[1] = false
                */

            }
        },
        created() {

            /*
            this.$store.dispatch("loanid",{
                id: this.$route.params.id
            }).then(response => {
                this.loans = response.data
                this.isActive = false
                this.$nextTick(function() {
                    $('#example').DataTable();
                });
            }).catch(error => {
                this.error = error.response;
            })*/

        },
        updated(){

        }
    };
</script>
