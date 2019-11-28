<template>
    <div class="container-fluid">
        <form action="/" method="POST" id="signUp" class="form-section">
            <div v-show="step ===1">
                <h1>User Information</h1>
                <div class="form-row">

                    <div class="form-group col-12-sm">

                        <input type="text" class="form-control" v-model="onboarding.name" id="inputName" placeholder="Name" required>
                    </div>
                    <div class="form-group col-12-sm">

                        <input type="email" class="form-control" v-model="onboarding.email" id="inputEmail" placeholder="Email" required>
                    </div>
                    <div class="form-group col-12-sm">
                        <input type="number" class="form-control" v-model="onboarding.phoneNumber" id="inputPhone" placeholder="Phone Number" required>
                    </div>

                    <div class="form-group col-12-sm">

                        <input type="password" class="form-control" v-model="onboarding.password" id="password" placeholder="Password" required>
                    </div>
                    <button class="btn btn-primary" @click.prevent="next()">Next</button>
                </div>
            </div>
            <div v-show="step ===2">
                <h1>Business Details</h1>
                <div class="form-row">
                    <input type="file" class="form-control" id="logo" placeholder="logo">
                    <div class="form-group col-12-sm">

                        <input type="text" class="form-control" v-model="onboarding.businessName" id="businessName" placeholder="Name" required>
                    </div>
                    <div class="form-group col-12-sm">

                        <input type="text" class="form-control" v-model="onboarding.address" id="address" placeholder="Address" required>
                    </div>
                    <div class="form-group col-12-sm">
                        <input type="text" class="form-control" v-model="onboarding.state" id="inputState" placeholder="State" required>
                    </div>
                    <div class="form-group col-12-sm">
                        <input type="text" class="form-control" v-model="onboarding.country" id="inputCountry" placeholder="Country" required>
                    </div>
                    <div class="form-group col-12-sm">
                        <input type="number" class="form-control" v-model="onboarding.numberOfStaff" id="staffNumber" placeholder="Number of Staff" required>
                    </div>
                    <div class="form-group col-12-sm">
                        <input type="number" class="form-control" v-model="onboarding.monthlyWorkingDays" id="staffNumber" placeholder="Monthly working days" required>
                    </div>
                    <div class="form-group col-12-sm">
                        
                        <select id="workingHours" v-model="onboarding.workWeek" class="form-control">
                            <option selected>Business</option>

                            <option>Monday - Friday (8:00am-5:00pm)</option>
                            <option>Monday - Saturday (8:00am-5:00pm)</option>
                            <option>Monday - Sunday (12:00-9:00pm)</option>
                        </select>
                        
                    </div>
                    <button class="btn btn-primary" @click.prevent="prev()">Prev</button>
                        <button class="btn btn-primary" @click.prevent="next()">Next</button>
                </div>
                </div>
                <div v-show="step ===3">
                    <h1>Subscribe</h1>
                    <div class="form-row">

                        <div class="form-group col-12-sm">

                            <input type="text" class="form-control" id="inputName4" placeholder="Name">
                        </div>

                        <button class="btn btn-primary" @click.prevent="prev()">Prev</button>
                        <input class="btn btn-primary" type="submit" value="SUBMIT">
                    </div>
                </div>
        </form>
        
        
    </div>


</template>

<script>
    export default {
        name: 'Form',
        data() {
            return {
                step: 1,
                onboarding: {
                    name: null,
                    email: null,
                    phoneNumber: null,
                    password: null,
                    businessName: null,
                    address: null,
                    state: null,
                    country: null,
                    numberOfStaff: null,
                    monthlyWorkingDays: null,
                    workWeek: 'Business'

                }
            }
        },
        methods: {
            prev() {
                this.step--;
            },
            next() {
                this.step++;
            },
            submit() {
                alert('Registration Successful')
            }
        }
    }
</script>

<style scoped>
.container-fluid{
    background: url('../assets/form.jpg') center center/cover no-repeat scroll;
height:fit-content;

}
.form-section{
    width:100vw;
    
    margin:0 auto;
    padding: 40px;
}
.form-group.col-12-sm{
    width:100%;
}
input[type="file"]{
    outline:none;
    border:none;
    background:transparent;
}


 @media only screen and (min-width: 320px) {
    h1 {
      font-size: 1.5rem;
    }
    h3 {
      font-size: 1.3rem;
      margin-bottom: 12px;
    }
    
    .btn{
        margin:10px auto;
    }
  }

  @media only screen and (min-width: 768px) {
    h1 {
      font-size: 1.75rem;
      text-align: center;
    }
    h3 {
      font-size: 1.4rem;
      margin-bottom: 12px;
    }
     .form-section{
        width:60vw;
    }
   
  }

  @media only screen and (min-width: 1024px) {
    h1 {
      font-size: 2.0rem;
      text-align: center;
    }
    h3 {
      font-size: 1.3rem;
      margin-bottom: 15px;
    }
      .form-section{
        width:40vw;
    }
    
  }

  @media only screen and (min-width: 1900px) {
    h1 {
      font-size: 2.3rem;
      text-align: center;
    }
    h3 {
      font-size: 2.0rem;
      margin-bottom: 20px;
    }
   
  }
</style>