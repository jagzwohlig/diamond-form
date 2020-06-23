<template>
  <div>
    <div class="form-content">
      <div class="text-white main-title py-5">VerifAId</div>
    </div>
    <div class="backgorund-content">
      <div class="verified-form">
        <b-container>
          <b-card class="p-4">
            <div>
              <b-form
                @submit="onSubmit"
                @reset="onReset"
                v-if="show"
                class="text-left"
              >
                <!-- Company Name -->
                <b-form-group
                  id="input-group-1"
                  label="Company Name:"
                  label-for="input-1"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-1"
                      v-model="form.comapny"
                      type="comapny"
                      required
                      placeholder="Enter Comapny"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <b-icon icon="check2" class="h2 text-success"></b-icon>
                      </div>
                      <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                    </div>
                  </div>
                </b-form-group>
                <!-- director -->
                <b-form-group
                  id="input-group-2"
                  label="Director:"
                  label-for="input-2"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-2"
                      v-model="form.director"
                      type="director"
                      required
                      placeholder="Enter director"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <!-- <b-icon icon="check2" class="h2 text-success"></b-icon> -->
                      </div>
                      <div>
                        <b-icon icon="x" class="h2 text-danger"></b-icon>
                      </div>
                    </div>
                  </div>
                </b-form-group>

                <!-- first name -->
                <b-form-group
                  id="input-group-3"
                  label="First Name:"
                  label-for="input-3"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-3"
                      v-model="form.name"
                      required
                      placeholder="Enter Name"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <b-icon icon="check2" class="h2 text-success"></b-icon>
                      </div>
                      <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                    </div>
                  </div>
                </b-form-group>
                <!-- last name -->
                <b-form-group
                  id="input-group-4"
                  label="Last Name:"
                  label-for="input-4"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-4"
                      v-model="form.lastname"
                      required
                      placeholder="Enter Last Name"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <b-icon icon="check2" class="h2 text-success"></b-icon>
                      </div>
                      <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                    </div>
                  </div>
                </b-form-group>
                <!-- email -->
                <b-form-group
                  id="input-group-5"
                  label="Email address:"
                  label-for="input-5"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-5"
                      v-model="form.email"
                      type="email"
                      required
                      placeholder="Enter email"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <b-icon icon="check2" class="h2 text-success"></b-icon>
                      </div>
                      <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                    </div>
                  </div>
                </b-form-group>
                <!-- phone No -->
                <b-form-group
                  id="input-group-6"
                  label="Phone No:"
                  label-for="input-6"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-6"
                      v-model="form.phoneNo"
                      required
                      placeholder="Enter Phone No"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <b-icon icon="check2" class="h2 text-success"></b-icon>
                      </div>
                      <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                    </div>
                  </div>
                </b-form-group>
                <!-- address -->
                <b-form-group
                  id="input-group-7"
                  label="Address:"
                  label-for="input-7"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-7"
                      v-model="form.address"
                      required
                      placeholder="Enter Address"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <b-icon icon="check2" class="h2 text-success"></b-icon>
                      </div>
                      <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                    </div>
                  </div>
                </b-form-group>
                <!-- back NAme -->
                <b-form-group
                  id="input-group-8"
                  label="Bank Name:"
                  label-for="input-8"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-8"
                      v-model="form.bankname"
                      required
                      placeholder="Enter Bank Name"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <!-- <b-icon icon="check2" class="h2 text-success"></b-icon> -->
                      </div>
                      <div>
                        <b-icon icon="x" class="h2 text-danger"></b-icon>
                      </div>
                    </div>
                  </div>
                </b-form-group>
                <!-- account No -->
                <b-form-group
                  id="input-group-8"
                  label="Account No:"
                  label-for="input-8"
                >
                  <div class="d-flex">
                    <b-form-input
                      id="input-8"
                      v-model="form.accountNo"
                      required
                      placeholder="Enter Account No"
                    ></b-form-input>
                    <div class="mx-auto">
                      <div>
                        <!-- <b-icon icon="check2" class="h2 text-success"></b-icon> -->
                      </div>
                      <div>
                        <b-icon icon="x" class="h2 text-danger"></b-icon>
                      </div>
                    </div>
                  </div>
                </b-form-group>
                <div class="text-center verified-btn">
                  <b-button type="submit" variant="primary" class="px-5"
                    >Verified</b-button
                  >
                  <!-- <b-button type="reset" variant="danger">Reset</b-button> -->
                </div>
              </b-form>
            </div>
          </b-card>
        </b-container>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        comapny: "",
        director: "",
        name: "",
        lastname: "",
        email: "",
        phoneNo: "",
        address: "",
        bankname: "",
        accountNo: ""
      },
      show: true
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.food = null;
      this.form.checked = [];
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    }
  }
};
</script>
<style lang="scss">
.form-content {
  position: relative;
  background: linear-gradient(to right, #184065, #126778, #06bd9e 100%);
  min-height: 500px;
  .main-title {
    font-size: 60px;
  }
}

.backgorund-content {
  background-color: #f7f7fa;
  height: calc(100vh - 500px);
  .form-group {
  }
  .d-block {
    font-size: 1.5rem;
  }
  .form-control {
    // height: calc(1.5em + 1.01rem + 2px);
    width: 95%;
    font-size: 1.2rem;
  }
}
.verified-form {
  transform: translate(0%, -30%);
  .container {
    max-width: 1440px;
  }
  .verified-btn {
    .btn-primary {
      background: #06bd9e;
      border-color: #06bd9e;
      font-size: 20px;
    }
    .btn-primary:active {
      background: #06bd9e;
      border-color: #06bd9e;
    }
    .btn-primary:focus {
      background: #06bd9e;
      border-color: #06bd9e;
    }
    .btn-primary:hover {
      background: #06bd9e;
      border-color: #06bd9e;
    }
  }
}
</style>
