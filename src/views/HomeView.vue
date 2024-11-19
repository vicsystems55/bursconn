<template>
      <!-- Modal -->
      <div data-bs-backdrop='false' class="modal  fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <div class="modal-dialog modal-dialog-centered modal-md">
        <div class="modal-content">
          <div class="modal-header">
            <h1 class="modal-title fs-3 font-weight-bold" id="exampleModalLabel">REGISTRATION FORM</h1>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body ">
            <div  class="">
              <div class="mb-3">
                <label for="surname" class="form-label ">Surname</label>
                <input type="text" class="form-control" id="surname" v-model="surname" required />
              </div>
              <div class="mb-3">
                <label for="firstName" class="form-label">First Name</label>
                <input type="text" class="form-control" id="firstName" v-model="firstname" required />
              </div>
              <div class="mb-3">
                <label for="otherNames" class="form-label">Other Names</label>
                <input type="text" class="form-control" id="otherNames" v-model="othername" />
              </div>
              <div class="mb-3">
                <label for="schoolName" class="form-label">Name of Institution</label>
                <input type="text" class="form-control" id="schoolName" v-model="schoolName" />
              </div>
              <div class="mb-3">
                <label for="state-select">Select State:</label>
                <select id="state-select" class="form-control" v-model="selectedState">
                  <option value="" disabled>Select a state</option>
                  <option v-for="state in states" :key="state" :value="state">
                    {{ state }}
                  </option>
                </select>
               
              </div>
              <div class="mb-3">
                <label for="email" class="form-label">E-mail Address</label>
                <input type="email" class="form-control" id="email" v-model="email" required />
              </div>
              <div class=" mb-3 form-check">
                <input class="form-check-input" type="radio" v-model="gender" :value="'male'" id="flexRadioDefault1">
                <label class="form-check-label" for="flexRadioDefault1">
                  Male
                </label>
              </div>
              <div class="form-check">
                <input class="form-check-input" type="radio" v-model="gender" :value="'female'" id="flexRadioDefault2" >
                <label class="form-check-label" for="flexRadioDefault2">
                  female
                </label>
              </div>

              <div class="text-center py-3">
                <button @click="registerMember()" style="width: 320px;" type="submit"
                  class="btn btn-warning btn-lg btn-block shadow">REGISTER</button>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>

  <div class="home">

    <div class="header-one py-3">

      <div class="d-flex justify-content-around">
        <div class="one">
          <img class="img-fluid animate__animated animate__zoomIn" style="height: 150px;" src="../assets/1.png" alt="">
        </div>


        <div class="one">
          <img class="img-fluid animate__animated animate__zoomIn" style="height: 170px;" src="../assets/3.png" alt="">
        </div>

        <div class="one">
          <img class="img-fluid animate__animated animate__zoomIn" style="height: 170px;" src="../assets/2.png" alt="">
        </div>


      </div>

    </div>
    <div class="header-two py-5  animate__animated animate__fadeIn text-center">
      <div class="container font-header animate__animated animate__fadeInUp">
        <h2>A 4 DAY ANNUAL NATIONAL WORKSHOP ON PUBLIC FINANCE MANAGEMENT
          AND LEADERSHIP STRATEGY FOR RECTORS, PROVOSTS AND BURSARS OF
          POLYTECHNICS AND COLLEGES OF TECHNOLOGY, EDUCATION,
          HEALTH AND AGRICULTURE, IN NIGERIA
        </h2>
        <h2 style="color: yellow" class="py-2">Reducing cost and delivering result</h2>
        <button class="btn btn-warning" data-bs-toggle="modal" data-bs-target="#exampleModal">
          <h3> REGISTER NOW</h3>
        </button>
      </div>
    </div>

    <!-- Button trigger modal -->
    <!-- <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Launch demo modal
</button> -->


    <div class="header-three py-3 text-center">
      <div class="container">
        <h2 style="color: red;" class="animate__animated animate__fadeInUp">HANDS ON PERFORMANCE IMPROVEMENT TRAINING
        </h2>


        <div class="title-section animate__animated animate__fadeInUp animate__delay-1s py-3">
          <h2 style="color: green; font-weight: bolder;" class="py-2 title">
            Theme:</h2>
          <h2>Capacity Building For Quality Delivery</h2>
          <hr>
        </div>



        <div style=" border-radius: 25px;"
          class="contianer title-section animate__animated animate__fadeInUp animate__delay-2s py-5 bg-warning shadow">
          <h2 class="title">Topic:</h2>
          <h2 class="fs-1 font-weight-bold" style="font-weight: bolder;">Public Finance Managment and Leadership
            Strategy</h2>

        </div>


        <div class="title-section animate__animated animate__fadeInUp animate__delay-3s py-3 mt-3">
          <h2 class="title">Target Audience:</h2>
          <h2>Rectors, Provots and Bursars</h2>
          <hr>
        </div>


        <div class="title-section animate__animated animate__fadeInUp animate__delay-4s py-3">
          <h2 class="title">Date</h2>
          <h2>26 - 29 November, 2024</h2>
          <hr>
        </div>


        <div class="title-section animate__animated animate__fadeInUp animate__delay-5s animate__delay-1s py-3">
          <h2 class="title">Venue:</h2>
          <h2>B.O Ukeje Hall, Jibril Aminu House,</h2>
          <h2>National Commission for Colleges of Education (NCCE),<br>
            Plot 829 Cadastral Zone A01, Ralph Shodeinde Street, Gariki FCT-Abuja
          </h2>
          <hr>
        </div>





        <div
          class="container py-3 mt-3 white-background mx-auto animate__animated animate__fadeIn animate__delay-5s animate__delay-2s shadow"
          style="border-radius: 20px;">
          <h2 class="title"> Participation Fee</h2>
          <h2 class="" style="font-weight: bolder;">NGN 150,000/Perticipant</h2>
          <h3 class="py-2">👉 To be paid into the <br> Association of Federal Polytechnic Bursars' <br> Bank Account as
            provided
          </h3>
         <div class="py-2">
          <h3 class="text-success fw-bold ">Account Name</h3>
          <h3 class="">Federal Polytechnic Bursars Corporative Society</h3>
          <br>
          <h3 class="text-success fw-bold ">Account Number</h3>
          <h3 class="">0212829968</h3>
          <br>
          <h3 class="text-success fw-bold ">Bank </h3>
          <h3 class="">Guarantee Trust Bank (GTBank)</h3>
         </div>
          <h3 class="text-danger py-3">Note: All Participants are expected to register online on or before <br>22nd
            November, 2024 to enable the
            association put together all their workshop packages and certificates.</h3>

          <h3 class="py-3">For Registration & Association Accound Details, Visit</h3>
          <p>🌐 www.bursconnationalworkshop.com.ng</p>
          <p>☎ 08036912263, 07036826996</p>
        </div>
      </div>
    </div>

    <div class="footer d-flex justify-content-between">
      <div class="footer-logo">
        <span>Powered By:</span><br>
        de'icon con
      </div>

      <div class="footer-logo2">
        <span>Sponsor-able by:</span><br>
        tetfund logo

      </div>

    </div>


  </div>
</template>


<script>
import axios from 'axios';
export default {
  data() {
    return {
      surname: '',
      firstname: '',
      othername: '',
      email: '',
      gender: '',
      loading: false,
      selectedState: "",
      schoolName:'', // Stores the selected state
      states: [
        "Abia",
        "Adamawa",
        "Akwa Ibom",
        "Anambra",
        "Bauchi",
        "Bayelsa",
        "Benue",
        "Borno",
        "Cross River",
        "Delta",
        "Ebonyi",
        "Edo",
        "Ekiti",
        "Enugu",
        "Gombe",
        "Imo",
        "Jigawa",
        "Kaduna",
        "Kano",
        "Katsina",
        "Kebbi",
        "Kogi",
        "Kwara",
        "Lagos",
        "Nasarawa",
        "Niger",
        "Ogun",
        "Ondo",
        "Osun",
        "Oyo",
        "Plateau",
        "Rivers",
        "Sokoto",
        "Taraba",
        "Yobe",
        "Zamfara",
        "FCT (Federal Capital Territory)"
      ]
    }
  },

  methods: {
    registerMember() {


      axios({
        method: "post",
        url: process.env.VUE_APP_URL + '/api/bursconn/register-member',
        data: {
          email: this.email,
          surname: this.surname,
          firstname: this.firstname,
          othername: this.othername,
          gender: this.gender,
          schoolName: this.schoolName,
          selectedState: this.selectedState
        }
      })
        .then((response) => {

          
          console.log(response),
            this.msg = true
          return this.$router.push('/registration-successful')
        })
        .catch((err) => {
          console.log(err)
        })
    }
  },
}
</script>

<style>
.footer {
  padding: 5px 20px;
  background-color: green;
  color: white;
}

label {
  text-align: left;
}

.title-section animate__animated animate__fadeInUp {
  padding: 0 70px;
}

.white-background {
  background-color: white;
  /* max-width: 900px; */
}

.title {
  color: green;
  font-weight: bolder;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
}

.font-header {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
}

.one img {
  height: 130px;
  object-fit: contain;

}

.home {

  background-image: url('../assets/coatarms.png');
  background-size: 200px;
  box-shadow: inset 0 0 0 1000px rgba(255, 255, 255, 0.623);

}

.header-one {
  min-height: 200px;
}

.header-two {
  min-height: 400px;
  background-size: cover;
  background-position: center center;
  box-shadow: inset 0 0 0 1000px rgba(1, 143, 60, 0.712);

  /* background-color: green; */
  color: white;
  background-image: url('../assets/bg.jpeg');

}

.header-three {

  box-shadow: inset 0 0 0 100vh rgba(191, 226, 201, 0.623);

}
</style>
