<template>
  <v-app id="app">
    <v-app-bar app light class="pl-7" height="80" id="navbar" flat>
      <a class="navbar-brand" href="/">
        <img src="../assets/Dreamguru.png" width="136" height="28" alt="">
      </a>
      <v-spacer></v-spacer>
      <v-container  class="d-none d-sm-block">
        <v-row justify="end" no-gutters >
          <v-col cols="12" md="6">
          </v-col>
          <v-col cols="12" md="3" no-gutters class="text-end">
            <v-avatar>
                <img
                src="../assets/avatar.png"
                alt="John"
                size="46"
                >
            </v-avatar>
          </v-col>
          <v-col cols="12" md="2" no-gutters class="text-start">
            <p class="mt-1 mb-0 ml-2"><b>Robert P.</b></p>
            <p class="xsmall mb-0 ml-2">Murid</p>
          </v-col>
        </v-row>
      </v-container>
      <v-btn
              class="mr-4"
              fab
              light
              style="height: 48px; width:48px; box-shadow: 0px 4px 40px rgba(0, 0, 0, 0.06);"
              color="white"
            >
              <v-icon light>
                mdi-bell-outline
              </v-icon>
            </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <h1 class="text-start hero-1">Payment Options</h1>
          <v-col cols="12" sm="6">
                <h4 class="text-start"> Debit Instan </h4>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>Direct Debit BNI</b>
                </v-btn>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>OneKlik</b>
                </v-btn>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>Direct Debit Mandiri</b>
                </v-btn>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>OCTO Cash by CIMB Niaga</b>
                </v-btn>
                    
            </v-col>
            <v-col cols="12" sm="6">
                <h4 class="text-start"> Transfer Virtual Account </h4>
                <v-btn class="mb-4" 
                    block color="#FFC555"  outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>BNI Virtual Account</b>
                </v-btn>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>BCA Virtual Account</b>
                </v-btn>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>BRIVA</b>
                </v-btn>
                <v-btn class="mb-4"
                    block color="#FFC555" outlined rounded x-large>
                    <img class="mr-8" src="../assets/bni.png">

                    <b>Mandiri Virtual Account</b>
                </v-btn>
            </v-col>
        </v-row>
        <v-row>
            <hr class="solid">
            <v-col cols="6" sm="6" class="text-start">
                <h4>Total Bayar</h4>
                <h4><b>Rp.1.750.000</b></h4>
            </v-col>
            <v-col cols="6" sm="6" class="text-end">
        <v-dialog max-width="428">
          <template v-slot:activator="{ on,}">
                <v-btn class="" v-bind="size" v-on="on"
                    color="#FFC555" dark depressed>
                    <b>Bayar & Request</b>
                </v-btn>
          </template>
          <template v-slot:default="completion">
                  <v-card class="bg"> 
                    <v-card-text style="padding-bottom:0px;">
                  <v-container> 
                    <v-row>
                      <h4 class="mt-6">Arrangement Completed ! </h4>
                      <v-col cols="12" class="text-center" no-gutters>
                        <v-avatar color="#E6696A" class="ma-3 cards-avatar">
                        <img src="../assets/budi.png" alt="Budi">
                        </v-avatar>
                      </v-col>
                    </v-row>
                      <v-row>
                        <h5> <b>Budi Santoso</b> </h5>
                        <h6> Matematika </h6>
                        
                        <p class="mb-2"><b>Your session will be held on :</b></p>
                        <p class="mb-4"> 3 - 7 February 2021 at <b>3:00 - 6:00 PM</b> via Zoom</p>
                        
                        <p><b>Zoom Link</b></p>
                        <img class="btn-zoom mb-4" src="../assets/zoom.png" alt="Go To Zoom Meeting">
                        
                        <p class="mb-0"><b>Note :</b></p>
                        <p>Once it's scheduled it can't be canceled.</p>
                      </v-row>
                  </v-container>
                </v-card-text> 
                <v-card-actions class="pb-8 px-5">
                  <v-btn
                    color="#FDC356" depressed rounded dark block
                    @click="completion.value = false"
                    href="#/cariguru"
                    
                  >
                    Add to Google Calendar
                  </v-btn>
                </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
            </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
  
</template>

<script>
export default {
  name: 'App',

  components: {
  },
  computed: {
    size () {
      const size = {xs:'large',sm:'large',md:"x-large",lg:'x-large',xl:'x-large'}[this.$vuetify.breakpoint.name];
      return size ? { [size]: true } : {}
    }
  },
  data: () => ({
        
        components: {
            
        }
      }),
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

#app {
  font-family: "Montserrat";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #F9FAFB;
}
hr.solid {
  border-top: 3px solid #000000;
}
p.xsmall{
  font-size: 10px !important;
}
p{
  font-size: 14px !important;
}
h1{
  font-size: 48px !important;
}
h2{
  font-size: 36px !important;
}
h3{
  font-size: 28px !important;
}
h4{
  font-size: 22px !important;
}
h5{
  font-size: 18px !important;
}
h6{
  font-size: 16px !important;
}
.form-title{
  padding: 40px;
  padding-bottom: 20px;
}
.hero-1{
  margin-top: 80px !important;
  margin-bottom: 44px !important;
}
.hero-1-content{
  text-align: start;
  padding: 30px !important;
  padding-top: 100px !important;
  margin-left: 100px;
}
.btn-hero-1{
  margin-left: 0px !important;
  margin-top: 20px;
}
.bg{
  background: #F9FAFB !important;
}
.btn-google{

box-shadow: 0px 0px 1px rgba(0, 0, 0, 0.084), 0px 1px 1px rgba(0, 0, 0, 0.168)!important;
border-radius: 2px!important;
}
.container-fluid.hero-1{
  background-image: url("../assets/Frame 1.png");
  background-repeat: no-repeat;
  background-size: initial;
  background-position: right bottom;
  overflow: hidden;
}
.container-fluid.hero-2{
  margin-top: 50px;
}
.btn.btn-outline-primary{
  border-radius: 18px;
  border: 2px solid #FFC555;
  color:#FFC555;
  padding-left:30px;
  padding-right:30px;
  margin-left: 10px;
  margin-right: 10px;
}
.btn.btn-outline-primary:hover{
  background:#FFC555;
  border: 2px solid #FFC555;
}
.btn.btn-primary:hover{
  background:#E3A733;
  border: 2px solid #E3A733;
}
.btn.btn-primary{
  border-radius: 18px;
  border: 2px solid #FFC555;
  background:#FFC555;
  padding-left:30px;
  padding-right:30px;
  margin-left: 10px;
  margin-right: 30px;
}
.container-hero-2{
  margin : 15px;
  margin-top: 50px !important;
  margin-bottom: 50px !important;
}
.container-pengajar{
  height: 146px;

  background: #FFFFFF;
  box-shadow: 0px 4px 40px rgba(0, 0, 0, 0.06);
  border-radius: 20px;
}
.container-photo-1{
  height: 146px;
  background: #E6696A;
  border-radius: 20px 0px 0px 20px;
  object-fit: cover;
  overflow:hidden;
  padding:0px !important;
}
.container-photo-2{
  height: 146px;
  background: #38BEA5;
  border-radius: 20px 0px 0px 20px;
  object-fit: cover;
  overflow:hidden;
  padding:0px !important;
}
.container-photo-3{
  height: 146px;
  background: #FFC555;
  border-radius: 20px 0px 0px 20px;
  object-fit: cover;
  overflow:hidden;
  padding:0px !important;
}
.container-text-pengajar{
  padding: 15px !important;
}
#avatar1 {
    background-image: url('../assets/budi.png');
    width: 100%;
    height: 100%;
    border-radius: 20px 0px 0px 20px;
    background-size: auto;
    background-repeat: no-repeat;
    background-position: bottom center;
}
#avatar2 {
    background-image: url('../assets/susi.png');
    width: 100%;
    height: 100%;
    border-radius: 20px 0px 0px 20px;
    background-size: auto;
    background-repeat: no-repeat;
    background-position: bottom center;
}
#avatar3 {
    background-image: url('../assets/andi.png');
    width: 100%;
    height: 100%;
    border-radius: 20px 0px 0px 20px;
    background-size: auto;
    background-repeat: no-repeat;
    background-position: bottom center;
}

#navbar{
  background-color: #F9FAFB;
  filter: drop-shadow(0px 4px 40px rgba(0, 0, 0, 0.06));
}
.btn-zoom {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
.cards-avatar{
  width: 144px !important;
  height: 139px !important;
  border-radius: 15px !important;
}
@media screen and (max-width: 600px) {
  h4{
    font-size: 18px !important;
  }
  .hero-1{
  margin-top: 40px !important;
  margin-bottom: 44px !important;
}
}
</style>