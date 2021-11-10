<template>
  <v-app id="app">
    <v-app-bar app light class="pl-xs-0 pl-7" height="80" id="navbar" flat>
      <a class="navbar-brand" href="/">
        <img src="../assets/Dreamguru.png" width="136" height="28" alt="">
      </a>
      <v-spacer></v-spacer>
      <div class="hidden-sm-and-down">
        <v-btn class="mr-5 px-7" color="#FDC356" rounded light outlined>Untuk Guru</v-btn>
        
        <!-- Register button -->
        <v-dialog persistent max-width="600">

        <template v-slot:activator="{ on, register }">
          <v-btn
            class="mr-5 px-7" color="#FDC356" depressed rounded dark outlined
            v-bind="register"
            v-on="on"
          >Daftar</v-btn>
        </template>
        <template v-slot:default="register">
          <v-card class="bg">
            <div class="form-title">
              <img src="../assets/Dreamguru.png" width="184" height="38" alt="">
              <br><br><br>
              <h3 style="font-weight: 600;">Masuk</h3>
            </div>
            
            <v-card-text>
          <v-container class="px-10">
            <v-row no-gutters>
              <v-col cols="12">
                <p class="text-left font-weight-bold">Email</p>
                <v-text-field
                  solo
                  clearable
                  label="john.doe@gmail.com"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <p class="text-left font-weight-bold">Kata Sandi</p>
                <v-text-field
                  v-model="password"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show1 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Masukkan Kata Sandi"
                  hint="At least 8 characters"
                  counter
                  @click:append="show1 = !show1"
                  solo
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <p class="text-left font-weight-bold">Ulangi Kata Sandi</p>
                <v-text-field
                  v-model="password"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show1 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Tulis Ulang Kata Sandi"
                  hint="At least 8 characters"
                  counter
                  @click:append="show1 = !show1"
                  solo
                ></v-text-field>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions class="px-16">
          <v-btn x-large
            color="#FDC356" depressed rounded dark block
            @click="register.value = false"
            href="#/cariguru"
          >
            Daftar
          </v-btn>
        </v-card-actions>
        <v-card-actions class="px-16 pb-6">
          <v-btn x-large class="btn-google"
            color="#FFFFFF" block depressed
            @click="register.value = false"
            href="#/cariguru"
          >
          <div class="left">
                <img width="20px" style="margin-right:20px" alt="Google sign-in" 
                    src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Google_%22G%22_Logo.svg/512px-Google_%22G%22_Logo.svg.png" />
            </div>
            Daftar dengan Google
          </v-btn>
          
        </v-card-actions>
        <p class="pb-16 mb-0">Sudah Punya Akun? 
          <v-btn class="pa-0" color="#FDC356" plain text>Masuk Disini</v-btn> </p>
          </v-card>
        </template>
      </v-dialog>
        <!-- login button -->
        <v-dialog persistent max-width="600">

        <template v-slot:activator="{ on, login }">
          <v-btn
            class="px-7" color="#FDC356" depressed rounded dark
            v-bind="login"
            v-on="on"
          >Masuk</v-btn>
        </template>
        <template v-slot:default="dialog">
          <v-card class="bg">
            <div class="form-title">
              <img src="../assets/Dreamguru.png" width="184" height="38" alt="">
              <br><br><br>
              <h3 style="font-weight: 600;">Masuk</h3>
            </div>
            
            <v-card-text>
          <v-container class="px-10">
            <v-row no-gutters>
              <v-col cols="12">
                <p class="text-left font-weight-bold">Email atau Username</p>
                <v-text-field
                  solo
                  clearable
                  label="john.doe@gmail.com"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <p class="text-left font-weight-bold">Kata Sandi</p>
                <v-text-field
                  v-model="password"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :rules="[rules.required, rules.min]"
                  :type="show1 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Masukkan Kata Sandi"
                  hint="At least 8 characters"
                  counter
                  @click:append="show1 = !show1"
                  solo
                ></v-text-field>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions class="px-16">
          <v-btn x-large
            color="#FDC356" depressed rounded dark block
            @click="dialog.value = false"
            href="#/cariguru"
          >
            Masuk
          </v-btn>
          
        </v-card-actions>
        <v-card-actions class="px-16">
          <v-btn x-large
            color="#FDC356" depressed rounded dark block
            @click="dialog.value = false"
            href="#/admin"
          >
            Masuk Admin
          </v-btn>
          
        </v-card-actions>
        <v-card-actions class="px-16 pb-6">
          <v-btn x-large class="btn-google"
            color="#FFFFFF" block depressed
            @click="dialog.value = false"
            href="#/cariguru"
          >
          <div class="left">
                <img width="20px" style="margin-right:20px" alt="Google sign-in" 
                    src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Google_%22G%22_Logo.svg/512px-Google_%22G%22_Logo.svg.png" />
            </div>
            Masuk dengan Google
          </v-btn>
          
        </v-card-actions>
        <p class="pb-16 mb-0">Belum punya akun? 
          <v-btn class="pa-0" color="#FDC356" plain text>Daftar Sekarang</v-btn> </p>
          </v-card>
        </template>
      </v-dialog>
      </div>
      <!-- Hamburger Menu -->
      <div class="hidden-md-and-up">
      <v-menu bottom left>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                light
                icon
                v-bind="attrs"
                v-on="on"
              >
                <v-app-bar-nav-icon></v-app-bar-nav-icon>
              </v-btn>
            </template>

            <v-list>
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
              >
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
      </div>
    </v-app-bar>

    <v-main>
      <div id="app">
      <main>

        <div class="container-fluid hero-1">
          <div class="row">
            <div class ="col-md-4 hero-1-content">
              <h1>Belajar online jadi lebih asik, <b>Kalo gurunya klop!</b></h1>
              <br>
              <h4>Bersama DreamGuru, kamu bisa nemuin guru yang satu pemikiran dan ga ngebosenin lho, 
                Kok bisa? Makanya yuk <b>cobain daftar sekarang juga!</b> </h4>
              <v-btn class="my-xs-0 px-xs-2 my-5 px-7" color="#FDC356" depressed rounded dark>Masuk</v-btn>
            </div>
          </div>
        </div>

        <div class="container-fluid hero-2">
          <div class="row">
            <div class ="col hero-2-content">
              <h1><b>Pengajar Terbaik Kami</b></h1>
              <br>
            </div>
          </div>
          <div class="flex-row d-flex justify-content-center">
            <div class ="col-md-3 container-hero-2">
              <div class="row container-pengajar ">
                <div class="col-sm-4 container-photo-1">
                    <div id="avatar1"></div>
                </div>
                <div class="col-sm-8 text-start container-text-pengajar ">
                  <p><b>Budi Santoso</b></p>
                  <p class="xsmall">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Amet malesuada sagittis nam feugiat. Ut diam elit et volutpat adipiscing mi egestas. Cras volutpat.</p>
                </div>
              </div>
            </div>
            <div class ="col-md-3 container-hero-2">
              <div class="row container-pengajar">
                <div class="col-sm-4 container-photo-2">
                    <div id="avatar2"></div>
                </div>
                <div class="col-sm-8 text-start container-text-pengajar">
                  <p><b>Susi Susanti</b></p>
                  <p class="xsmall">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Amet malesuada sagittis nam feugiat. Ut diam elit et volutpat adipiscing mi egestas. Cras volutpat.</p>
                </div>
              </div>
            </div>
            <div class ="col-md-3 container-hero-2">
              <div class="row container-pengajar">
                <div class="col-sm-4 container-photo-3">
                    <div id="avatar3"></div>
                </div>
                <div class="col-sm-8 text-start container-text-pengajar">
                  <p><b>Andi Wijaya</b></p>
                  <p class="xsmall">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Amet malesuada sagittis nam feugiat. Ut diam elit et volutpat adipiscing mi egestas. Cras volutpat.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    </v-main>
  </v-app>
  
</template>

<script>
export default {
  name: 'Home',

  components: {
  },

  data: () => ({
        items: [
          { title: 'Masuk' },
          { title: 'Daftar' },
          { title: 'Untuk Guru' },
        ],
        show1: false,
        show2: true,
        show3: false,
        show4: false,
        password: 'Password',
        rules: {
          required: value => !!value || 'Required.',
          min: v => v.length >= 8 || 'Min 8 characters',
          emailMatch: () => (`The email and password you entered don't match`),
        },
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
@media screen and (max-width: 425px) {
  h1{
    font-size: 18px !important;
  }
  h4{
    font-size: 11px !important;
  }
  .hero-1-content{
  text-align: start;
  padding-bottom: 0px !important;
  padding-left: 30px !important;
  padding-right: 160px !important;
  padding-top: 100px !important;
  margin-top: 24px !important;
  margin-left: 12px;
}
.container-fluid.hero-1{
  background-image: url("../assets/Frame 2.png");
  background-repeat: no-repeat;
  background-size: auto;
  background-position: right bottom;
  overflow: hidden;
}
}
</style>