<template>
  <div>
       <div class="container">

        <!-- Outer Row -->
        <div class="row justify-content-center">

            <div class="col-xl-10 col-lg-12 col-md-9">

                <div class="card o-hidden border-0 shadow-lg my-5">
                    <div class="card-body p-0">
                        <!-- Nested Row within Card Body -->
                        <div class="row">
                            <div class="col-lg-6 d-none d-lg-block bg-login-image"></div>
                            <div class="col-lg-6">
                                <div class="p-5">
                                    <div class="text-center">
                                        <h1 class="h4 text-gray-900 mb-4">Forgot Password</h1>
                                    </div>
                                    <form class="user">
                                        <div class="form-group">
                                            <label for="">Existing Email Address</label>
                                            <input type="email" class="form-control form-control-user"
                                                id="exampleInputEmail" aria-describedby="emailHelp"
                                                placeholder="Existing Email Address..." v-model="form.email">
                                        </div>
                                       
                                        
                                        <button type="submit" class="btn btn-primary btn-user btn-block">
                                            Forget Password
                                        </button>
                                        <hr>
                                       
                                    </form>
                                    <hr>
                                    
                                    <div class="text-center">
                                        <router-link class="small" to="/">Back To Login</router-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>

        </div>

    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default{
    created(){
        if(User.loggedIn()){
            this.$router.push({name:'home'})
        }

    },
    data(){
        return {
            form:{
                email:null
            },
            errors:{

            }
        }    
    },
   
}

</script>

<style>
</style>