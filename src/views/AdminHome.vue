<template>
  <v-app id="app">
    <v-app-bar app light class="pl-7" height="80" id="navbar" flat>
      <a class="navbar-brand" href="/">
        <img src="../assets/Dreamguru.png" width="136" height="28" alt="">
      </a>
      <v-spacer></v-spacer>
      <v-container class="d-none d-sm-block">
        <v-row justify="end" no-gutters >
          <v-col cols="12" md="6">
          </v-col>
          <v-col cols="12" md="3" no-gutters class="text-end">
            <v-avatar>
                <img
                src="../assets/admin.png"
                size="46"
                >
            </v-avatar>
          </v-col>-
          <v-col cols="12" md="2" no-gutters class="text-start">
            <p class="mt-1 mb-0 ml-2"><b>Akmal D.</b></p>
            <p class="xsmall mb-0 ml-2">Admin</p>
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
        <h1 class="text-start hero-2">Pending Guru Applications </h1>
        <v-row no-gutters> 
          <v-col cols="6" sm="2" class="text-start card-list">
        <v-dialog max-width="428">
          <template v-slot:activator="{ on, guru }">
            <v-card max-width="170" class="cards" v-bind="guru" v-on="on">
              <v-avatar color="#E6696A" class="ma-3 cards-avatar">
              <img src="../assets/budi.png" alt="Budi">
              </v-avatar>
            <p class="ml-3 mb-0"><b>Budi Santoso</b></p>
            <p class="small ml-3 mb-0">Budi@gmail.com</p>
            <v-btn class="btn-detail" color="#FFC555" text> 
              Cek Detail 
              <v-icon
                block
                right
                dark
                color="#FFC555"
                >
                mdi-chevron-right
              </v-icon>
            </v-btn>
            </v-card>
          </template>
              <template v-slot:default="guru">
                  <v-card class="bg"> 
                    <v-card-text style="padding-bottom:0px;">
                  <v-container> 
                    <v-row>
                      <div class="form-title">
                        <h3 style="font-weight: 600;">Detail Guru</h3>
                      </div>
                      <v-col cols="6" sm="6" class="text-end pl-0" no-gutters style="padding-right:0px;">
                        <v-avatar color="#E6696A" class="img-fluid ma-3 cards-avatar">
                        <img src="../assets/budi.png" alt="Budi" class="img-fluid">
                        </v-avatar>
                      </v-col>
                      <v-col cols="6" sm="6" class="text-start pl-2 pr-0" style="padding-left:0px;" no-gutters>
                        <p class="mt-3 mb-0"><b>Budi Santoso</b></p>
                        <p class="small mb-0">Budi@gmail.com</p>
                      </v-col>
                    </v-row>
                    <v-row>
                      <h6 class="text-start">Detail Berkas : </h6>
                      <v-col cols="3" sm="3" class="text-start" style="padding-left:8px;" no-gutters>
                      <img src="../assets/berkas.png" class="img-fluid">
                      </v-col>
                      <v-col cols="3" sm="3" class="text-start" style="padding-left:8px;" no-gutters>
                      <img src="../assets/berkas.png" class="img-fluid">
                      </v-col>
                      <v-col cols="3" sm="3" class="text-start" style="padding-left:8px;" no-gutters>
                      <img src="../assets/berkas.png" class="img-fluid">
                      </v-col>
                      <v-col cols="3" sm="3" class="text-start" style="padding-left:8px;" no-gutters>
                      <img src="../assets/berkas.png" class="img-fluid">
                      </v-col>
                    </v-row>
                  </v-container>
                </v-card-text> 
                <v-card-actions class="mt-6 pb-8 px-5">
                  <v-btn
                    color="#FDC356" depressed rounded dark block
                    @click="guru.value = false"
                    
                  >
                    Approve Guru
                  </v-btn>
                </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
          </v-col>
          <v-col cols="6" sm="2" class="text-start card-list">
            <v-card max-width="170" class="cards">
              <v-avatar color="#FFC555" class="ma-3 cards-avatar">
              <img src="../assets/andi.png" alt="Andi">
              </v-avatar>
            <p class="ml-3 mb-0"><b>Andi Wijaya</b></p>
            <p class="small ml-3 mb-0">Andi@gmail.com</p>
            <v-btn class="btn-detail" color="#FFC555" text> 
              Cek Detail 
              <v-icon
                block
                right
                dark
                color="#FFC555"
                >
                mdi-chevron-right
              </v-icon>
            </v-btn>
            </v-card>
          </v-col>
          <v-col cols="6" sm="2" class="text-start card-list">
            <v-card max-width="170" class="cards">
              <v-avatar color="#38BEA5" class="ma-3 cards-avatar">
              <img src="../assets/susi.png" alt="Susi">
              </v-avatar>
            <p class="ml-3 mb-0"><b>Susi Susanti</b></p>
            <p class="small ml-3 mb-0">Susi@gmail.com</p>
            <v-btn class="btn-detail" color="#FFC555" text> 
              Cek Detail 
              <v-icon
                block
                right
                dark
                color="#FFC555"
                >
                mdi-chevron-right
              </v-icon>
            </v-btn>
            </v-card>
          </v-col>
          <v-col cols="6" sm="2" class="text-start card-list">
            <v-card max-width="170" class="cards">
              <v-avatar color="#FFC555" class="ma-3 cards-avatar">
              <img src="../assets/andi.png" alt="Andi">
              </v-avatar>
            <p class="ml-3 mb-0"><b>Andi Wijaya</b></p>
            <p class="small ml-3 mb-0">Andi@gmail.com</p>
            <v-btn class="btn-detail" color="#FFC555" text> 
              Cek Detail 
              <v-icon
                block
                right
                dark
                color="#FFC555"
                >
                mdi-chevron-right
              </v-icon>
            </v-btn>
            </v-card>
          </v-col>
          <v-col cols="6" sm="2" class="text-start card-list">
            <v-card max-width="170" class="cards">
              <v-avatar color="#38BEA5" class="ma-3 cards-avatar">
              <img src="../assets/susi.png" alt="Susi">
              </v-avatar>
            <p class="ml-3 mb-0"><b>Susi Susanti</b></p>
            <p class="small ml-3 mb-0">Susi@gmail.com</p>
            <v-btn class="btn-detail" color="#FFC555" text> 
              Cek Detail 
              <v-icon
                block
                right
                dark
                color="#FFC555"
                >
                mdi-chevron-right
              </v-icon>
            </v-btn>
            </v-card>
          </v-col>
          <v-col cols="6" sm="2" class="text-start card-list">
            <v-card max-width="170" class="cards">
              <v-avatar color="#FFC555" class="ma-3 cards-avatar">
              <img src="../assets/andi.png" alt="Andi">
              </v-avatar>
            <p class="ml-3 mb-0"><b>Andi Wijaya</b></p>
            <p class="small ml-3 mb-0">Andi@gmail.com</p>
            <v-btn class="btn-detail" color="#FFC555" text> 
              Cek Detail 
              <v-icon
                block
                right
                dark
                color="#FFC555"
                >
                mdi-chevron-right
              </v-icon>
            </v-btn>
            </v-card>
          </v-col>
          
          
        </v-row>
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

  data: () => ({
        BidangStudi: ['Matematika', 'Biologi', 'Kimia', 'Fisika'],
        harga:['dibawah 50.000','50.000 - 100.000','100.000 - 300.000','diatas 300.000'],
        rating:['1', '2', '3', '4', '5'],
        availability:['Setiap Hari','2 Hari Sekali','1 Minggu Sekali'],

        dates: ['2021-09-11', '2021-09-12','2021-09-13','2021-09-14','2021-09-15'],
        menu: false,
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
  background-image: url("../assets/bg.png");
  background-repeat: no-repeat;
  background-position: 95% 40%;
  background-color: #F9FAFB;
}
p.xsmall{
  font-size: 10px !important;
}
p.small{
  font-size: 12px !important;
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
.cards{
  border-radius: 20px !important;
  margin-right: 0px !important;
}
.card-list{
  margin-bottom: 14px !important;
}
.cards-avatar{
  width: 144px !important;
  height: 139px !important;
  border-radius: 15px !important;
}
.form-title{
  padding: 40px;
  padding-bottom: 20px;
}
.hero-1-content{
  text-align: start;
  padding: 30px !important;
  padding-top: 100px !important;
  margin-left: 100px;
}
.hero-1{
  margin-top: 128px !important;
  margin-bottom: 44px !important;
}
.hero-2{
  margin-top: 50px !important;
  margin-bottom: 30px !important;
}
.bg{
  background: #F9FAFB !important;
}
.btn-google{

box-shadow: 0px 0px 1px rgba(0, 0, 0, 0.084), 0px 1px 1px rgba(0, 0, 0, 0.168)!important;
border-radius: 2px!important;
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

#navbar{
  background-color: #F9FAFB;
  filter: drop-shadow(0px 4px 40px rgba(0, 0, 0, 0.06));
}
.btn-detail{
  margin-top:36px;
}
</style>
