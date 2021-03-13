<template>
  <div class="container">
    <h1 class="text-center font-l">
      Bin2Dec
    </h1>

    <div class="row justify-center">
      <div class="col-12">

        <input type="text" v-model="binaryInput" class="" placeholder="Binary...">

        <!--        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias aperiam, assumenda beatae consectetur, consequuntur, ducimus ea eum facilis ipsam labore laudantium maxime modi molestiae omnis quaerat quisquam ratione suscipit temporibus?</p>-->
      </div>
      <div class="col-12 ">
        <input type="text" v-model="decimalInput" class="" placeholder="Decimal...">
      </div>
    </div>
<!--    <input type="text">-->

<!--    <div class="header">-->
<!--      Dushanbe-->
<!--    </div>-->

<!--    <div class="row">-->
<!--      <div class="col-3 col-s-3 menu">-->
<!--        <ul>-->
<!--          <li>The Flight</li>-->
<!--          <li>The City</li>-->
<!--          <li>The Island</li>-->
<!--          <li>The Food</li>-->
<!--        </ul>-->
<!--      </div>-->

<!--      <div class="col-6 col-s-9">-->
<!--        <h1>The City</h1>-->
<!--        <p>Chania is the capital of the Chania region on the island of Crete. The city can be divided in two parts, the old town and the modern city.</p>-->
<!--        <img src="./../assets/logo.png" width="250" height="200">-->
<!--      </div>-->

<!--      <div class="col-3 col-s-12">-->
<!--        <div class="aside">-->
<!--          <h2>What?</h2>-->
<!--          <p>Chania is a city on the island of Crete.</p>-->
<!--          <h2>Where?</h2>-->
<!--          <p>Crete is a Greek island in the Mediterranean Sea.</p>-->
<!--          <h2>How?</h2>-->
<!--          <p>You can reach Chania airport from all over Europe.</p>-->
<!--        </div>-->
<!--      </div>-->
<!--    </div>-->

<!--    <div class="footer">-->
<!--      <p>Resize the browser window to see how the content respond to the resizing.</p>-->
<!--    </div>-->
  </div>
</template>

<script>
export default {
  name: "Main",

  data() {
    return {
      binaryInput: "",
      decimalInput: "",
    }
  }
}
</script>

<style scoped>

</style>