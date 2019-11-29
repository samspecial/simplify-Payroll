/* eslint-disable */
<template>
  <div class="container-fluid">
    <div class="bg-info size">
      <div class="container">
        <div class="row">
          <nav class="col navbar navbar-expand-lg navbar-dark mr-auto">
            <a class="navbar-brand" href="/">Simplify Payroll</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div id="navbarContent" class="collapse navbar-collapse">
              <ul class="navbar-nav mr-auto">
                <li class="nav-item active">
                  <a href="/" class="nav-link">Home</a>
                </li>
                <li class="nav-item">
                  <a href="#about" class="nav-link">About</a>
                </li>
                <li class="nav-item">
                  <a href="#signUp" class="nav-link">Sign Up</a>
                </li>
              </ul>
            </div>
          </nav>
        </div>
      </div>
    </div>

    <div class="row hero">
      <div class="col-12 col-md-12 col-lg-12">
        <div class="jumbotron-fluid content">
          <div class="row">
            <div class="col-12-sm col-md-6">

            </div>
            <div class="col-12-sm col-6-md">
              <h1 class="display-4">{{head}}</h1>
              <h3>{{subHead}}</h3>
              <a class="btn btn-info" href="#about" role="button">
                {{btn}}
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Feature/>
    <Form/>
  </div>
</template>

<script>
  import Feature from './Feature'
  import Form from './Form'
  export default {
    name: 'LandingPage',
    components: {
      Feature,
      Form,
    },
    data() {
      return {
        head: 'Simplify Payroll',
        subHead: 'With Software and service designed for your system',
        btn: 'Learn More',


      }
    }
  }
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }


  div.jumbotron-fluid.content {
    margin: 0 auto;
    width: 80vw;
    height: 70vh;
    display: flex;
    flex-flow: column wrap;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: url('../assets/hero.png') right bottom/contain no-repeat scroll;
  }

  .size {
    padding: 10px 20px;
  }

  h1 {
    font-size: 1.5rem;
    font-weight: 700;
    line-height: 16px;
    margin-bottom: 40px;
  }

  h3 {
    font-size: 1.3rem;
    margin-bottom: 25px;
    font-weight: 500;
  }

  .btn-primary {
    padding: 10px 20px;
    margin-top: 15px;
  }

  @media only screen and (min-width: 320px) {
    h1 {
      font-size: 1.5rem;
    }
    h3 {
      font-size: 1.3rem;
      margin-bottom: 12px;
    }
    .display-4 {
      font-size: 1.8rem;
    }
    .btn-primary {
      margin-top: 50px;
      padding: 5px 10px;
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
    .display-4 {
      font-size: 2.3rem;
    }
    div.jumbotron-fluid.content {
      background: url('../assets/hero.png') right bottom/contain no-repeat scroll;
      width: 80vw;
      height: 90vh;
      padding: 10px;
    }
  }

  @media only screen and (min-width: 1024px) {
    h1 {
      font-size: 2.0rem;
      text-align: center;
      line-height: 32px;
    }
    h3 {
      font-size: 1.3rem;
      margin-bottom: 15px;
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

  a {
    color: #42b983;
  }
</style>