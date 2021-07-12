<template>
<div><h1> Sign Up </h1>
<form autocomplete="off" >
  <input type="text" placeholder="Enter Your Name" required id="name"><br>
  <input type="email" placeholder="Enter Your Email" required disabled id="email"><br>
  <input type="password" placeholder="Enter Your Password" required disabled id="pass"><br>
  <input type="password" placeholder="Enter Your Confirm Password" required disabled id="conpass"><br>
  <input type="submit" id="subbut" disabled v-on:click="fun">
</form>
</div>
</template>
<script>

onkeyup=()=>{
    var name=document.getElementById('name').value;
    if(name.length==" ")
    {
      document.getElementById("email").disabled = true;
    }
    else{
        document.getElementById("email").disabled = false;
        document.getElementById("email").style.borderColor = 'blue';
        var email=document.getElementById('email').value;
        if(email.length==" ")
        {
         document.getElementById("pass").disabled = true;
         document.getElementById("conpass").disabled = true; 
        }
        else{
          document.getElementById("pass").disabled = false; 
          document.getElementById("conpass").disabled = false;
          document.getElementById("pass").style.borderColor = 'blue';
          document.getElementById("conpass").style.borderColor = 'blue'; 
          var pass=document.getElementById('pass').value;
          var conpass=document.getElementById('conpass').value;
          if(pass==conpass)
          {
            document.getElementById("subbut").disabled = false;
            document.getElementById("subbut").style.borderColor = 'blue';
          }
          else{
            document.getElementById("subbut").disabled = true;
            document.getElementById("subbut").style.borderColor = 'black';
          }
        }
    }

}
export default{
    name:'SignUp',
    methods:{
      fun:function()
    {
    alert("hey not disabled");
    }
    }
}
</script>
<style>
input{
    width:300px;
    height:30px;
    padding:10px 0px 10px 5px;
    margin:10px 0px 10px 0px;
    font-weight:bold;
    font-size:15px;
    border:2px solid black;
    color:black;
}
#name
{
    border:2px solid blue;
}
#subbut{
    width:200px;
    height:40px;
}
#subbut:hover
{
    border:2px solid black;
}
</style>