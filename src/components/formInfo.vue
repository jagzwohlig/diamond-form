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
              <b-form @submit="onSubmit" v-if="show" class="text-left">
                <!-- Company Name -->
                <label class="text-left">All fields are compolsory.</label>

                <b-form-group
                  id="input-group-1"
                  label="Company Name:"
                  label-for="input-1"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-1"
                        placeholder="Your Company Name"
                        v-model="$v.userDetails.companyName.$model"
                        :state="validateState('companyName')"
                        aria-describedby="input-userDetails-companyName"
                      ></b-form-input>
                      <b-form-invalid-feedback
                        id="input-userDetails-companyName"
                      >
                        Name of hotel is required.
                      </b-form-invalid-feedback>
                    </b-col>
                    <b-col md="2">
                      <div>
                        <div>
                          <b-icon
                            icon="check2"
                            class="h2 text-success"
                          ></b-icon>
                        </div>
                        <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- director -->
                <b-form-group
                  id="input-group-2"
                  label="Director:"
                  label-for="input-2"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-2"
                        v-model="userDetails.director"
                        placeholder="Full Name Of Director"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <!-- <b-icon icon="check2" class="h2 text-success"></b-icon> -->
                        </div>
                        <div>
                          <b-icon icon="x" class="h2 text-danger"></b-icon>
                        </div>
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>

                <!-- first name -->
                <b-form-group
                  id="input-group-3"
                  label="First Name:"
                  label-for="input-3"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-3"
                        v-model="userDetails.firstName"
                        required
                        placeholder="First Name"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <b-icon
                            icon="check2"
                            class="h2 text-success"
                          ></b-icon>
                        </div>
                        <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- last name -->
                <b-form-group
                  id="input-group-4"
                  label="Last Name:"
                  label-for="input-4"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-4"
                        v-model="userDetails.lastName"
                        required
                        placeholder="Last Name"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <b-icon
                            icon="check2"
                            class="h2 text-success"
                          ></b-icon>
                        </div>
                        <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- email -->
                <b-form-group
                  id="input-group-5"
                  label="Email address:"
                  label-for="input-5"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-5"
                        v-model="userDetails.email"
                        placeholder="Email Address"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <b-icon
                            icon="check2"
                            class="h2 text-success"
                          ></b-icon>
                        </div>
                        <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- phone No -->
                <b-form-group
                  id="input-group-6"
                  label="Phone No:"
                  label-for="input-6"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-6"
                        v-model="userDetails.phone"
                        required
                        placeholder="Enter Phone No"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <b-icon
                            icon="check2"
                            class="h2 text-success"
                          ></b-icon>
                        </div>
                        <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- address -->
                <b-form-group
                  id="input-group-7"
                  label="Address:"
                  label-for="input-7"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-7"
                        v-model="userDetails.address"
                        required
                        placeholder="Enter Address"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <b-icon
                            icon="check2"
                            class="h2 text-success"
                          ></b-icon>
                        </div>
                        <!-- <div><b-icon icon="x" class="h2 text-danger"></b-icon></div> -->
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- back NAme -->
                <b-form-group
                  id="input-group-8"
                  label="Bank Name:"
                  label-for="input-8"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-8"
                        v-model="userDetails.bankName"
                        required
                        placeholder="Enter Bank Name"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <!-- <b-icon icon="check2" class="h2 text-success"></b-icon> -->
                        </div>
                        <div>
                          <b-icon icon="x" class="h2 text-danger"></b-icon>
                        </div>
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <!-- account No -->
                <b-form-group
                  id="input-group-8"
                  label="Account No:"
                  label-for="input-8"
                >
                  <b-row>
                    <b-col md="10">
                      <b-form-input
                        id="input-8"
                        v-model="userDetails.accountNumber"
                        placeholder="Enter Account Number"
                      ></b-form-input>
                    </b-col>
                    <b-col md="2">
                      <div class="mx-auto">
                        <div>
                          <!-- <b-icon icon="check2" class="h2 text-success"></b-icon> -->
                        </div>
                        <div>
                          <b-icon icon="x" class="h2 text-danger"></b-icon>
                        </div>
                      </div>
                    </b-col>
                  </b-row>
                </b-form-group>
                <div class="text-center verified-btn">
                  <b-button type="submit" variant="primary" class="px-5"
                    >Verify</b-button
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
import { validationMixin } from "vuelidate";
import { required } from "vuelidate/lib/validators";
export default {
  mixins: [validationMixin],
  data() {
    return {
      userDetails: {
        companyName: null,
        director: null,
        firstName: null,
        lastName: null,
        email: null,
        phone: null,
        address: null,
        bankName: null,
        accountNumber: null
      },
      show: true
    };
  },
  validations: {
    userDetails: {
      companyName: {
        required
      },
      director: {
        required
      },
      firstName: {
        required
      },
      lastName: {
        required
      },
      email: {
        required
      },
      phone: {
        required
      },
      address: {
        required
      },
      bankName: {
        required
      },
      accountNumber: {
        required
      }
    }
  },
  methods: {
    validateState(name) {
      const { $dirty, $error } = this.$v.userDetails[name];

      return $dirty ? !$error : null;
    },
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.userDetails));
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
