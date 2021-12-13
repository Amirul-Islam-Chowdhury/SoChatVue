<template>
<div>
    <form @submit.prevent="handleSubmit">

       <h1> SoChat</h1>
   

       <label>Name :</label>
        <input type="name" v-model="name" required>

        <label>Email :</label>
        <input type="email" v-model="email" required>

        <label>Password :</label>  
        <input type="password" v-model="password" required>            
        <div v-if="passwordError" class="error">{{ passwordError }} </div>

        
   

        <div>
            <input type="checkbox" v-model="terms" required>
            <label>Please accept terms and conditions</label>
        </div>

        
       
        <div class="button">
            <button class="submit" type="submit">Sign up here</button>
        </div>

        <div class="button2">
            <button class="login" type="login">Login </button>
        </div>

        
    </form>

</div>

</template>


<script>
export default{

    data() {
        return {
            email: '',
            password: '',
            role: 'designer',
            education: [],
            terms: false,
            passwordError: ''
        }
    },
   
}
</script>


<style scoped> 

h1{
    font-family: 'Courier New', Courier, monospace;
    text-align: center;
    font-size: 50px;
}

form {
    max-width: 600px;
    margin: 40px auto;
    background: rgb(184, 213, 233);
    text-align: left;
    padding: 20px;
    border-radius: 10px;
}

label {
    color: rgb(0, 0, 0);
    display:inline-block;
    margin: 50px 0 15px;
    text-transform: uppercase;
}

input, select {
    display: block;
    padding: 10px 4px;
    width: 100%;
    box-sizing: bordre-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: rgb(0, 0, 0);
}

input[type="checkbox"] {
    display: inline-block;
    width:16px;
    margin: 0 10px 0;
    position: relative;
    top: 2px;
}

.pill {
    display: inline-block;
    margin: 20px 10px 0 0 ;
    padding: 6px 12px;
    border-radius: 20px;
    font-size: 12px;
    cursor: pointer;
    background: rgb(0, 0, 0);
}

button.login{
     background: rgb(10, 24, 230);
    border: 0;
    padding: 10px 25px;
    color: white;
    border-radius: 20px;
    margin: auto;
    display: block;
    margin-bottom: 1rem;
    
}

button {
    background: rgb(7, 24, 7);
    border: 0;
    padding: 10px 20px;
    color: white;
    border-radius: 20px;
     margin: auto;
    display: block;
    margin-bottom: 1rem;
}

.submit {
    text-align: center;
}


.error {
    color: #ff0000;
    margin-top: 10px;
    font-size: 0.8em;
    font-weight: bold;
}
</style>


