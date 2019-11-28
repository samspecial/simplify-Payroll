<template>
    <div class="container-fluid">
        <div class="container-fluid mt-4">
      <div class="row features" id="about">
        <div class="col-12">
          <h1 class="about-tagline">{{tagline}}</h1>
        </div>
        <div class="row row-card">
          <div v-for="user in users" :user="user" :key="user.id" class="col-12 col-md-6 col-lg-4">
            <div class="card">
              <div class="card-body">
                <h3 class="card-title">
                  {{user.first}}
                </h3>
                <p class="card-text">
                  {{user.second}}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div></div>
    </div>
</template>

<script>
    export default {
        name: 'Feature',
        data() {
            return {
                users: [{
          id: 1,
          first: "Automated Taxes",
          second: "All local, state and federal payroll taxes are calculated, filed and paid automatically"
        }, {
          id: 2,
          first: "Payroll on Autorun",
          second: "You can set payroll to run automatically each pay period. Nice!"
        }, {
          id: 3,
          first: "Flexible payment Schedule",
          second: "Pay your team weekly, bi-weekly, twice a month, or monthly"
        },
        {
          id: 4,
          first: "Unlimited Payrolls",
          second: "Run payrolls as many times as you need"
        }, {
          id: 5,
          first: "Accounting Integrations",
          second: "Gusto integrates with QuickBooks, Xero, and FreshBooks"
        }, {
          id: 6,
          first: "Payroll Report",
          second: 'Generate and download report for payroll history, bank transactions and contractor payments, paid time off, tax payments and more.'
        },
        {
          id: 7,
          first: 'Direct Deposit',
          second: "Your employees\' paycheck goes directly into their bank accounts"
        }, {
          id: 8,
          first: "No payroll setup fees",
          second: "Our easy-to-use software and helpful support team are here to help you get started."
        }, {
          id: 9,
          first: "Mobile",
          second: "Access your account and run payroll anytime on your smartphone or tablet"
        }
        ]
            }
        }
    }
</script>


<style scoped>

  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .size {
    padding: 10px 20px;
  }

    .card {
    height: 200px;
    margin: 10px;
    padding: 10px;
    background-color: orange;
  }

  .features {
    background: url('../assets/feature.jpg') center center/cover no-repeat scroll;
    padding: 10px;
     color:black;
  }

  .about-tagline {
    margin: 30px;
    font-weight:900;
   
  }

  @media only screen and (min-width: 320px) {
    h1 {
      font-size: 1.5rem;
    }
    h3 {
      font-size: 1.3rem;
      margin-bottom: 12px;
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
    .row-card {
      width: 75vw;
      height: fit-content;
      margin: 0 auto;
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
    .features {
      padding: 40px;
    }
    .card {
      margin: 15px;
    }
    .row-card {
      width: 65vw;
      height: fit-content;
      margin: 0 auto;
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
    .card {
      margin: 15px;
    }
  }

  a {
    color: #42b983;
  }

</style>