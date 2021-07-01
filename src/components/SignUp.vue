<template>
<h1> Sign Up </h1>
<form>
  <input type="text" placeholder="Enter Your Name"><br>
  <input type="email" placeholder="Enter Your Email"><br>
  <input type="password" placeholder="Enter Your Password"><br>
  <input type="password" placeholder="Enter Your Confirm Password"><br>
  <input type="submit" id="subbut">
</form>
</template>
<script>
export default{
    name:'SignUp'
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