<template>
  <div>
    <h1 class="text-center font-l">
      Bin2Dec
    </h1>

    <div class="row justify-center">
      <div class="col-12 col-s-12">
        <input v-model="binaryInput"
               placeholder="Binary..."
               type="text"
               @change="validateBinaryNumber"
               @input="validateBinaryNumber">
      </div>
      <div class="col-12 col-s-12">
        <input v-model="decimalInput"
               placeholder="Decimal..."
               type="text"
               @change="validateDecimalNumber"
               @input="validateDecimalNumber">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",
  props: {},
  data() {
    return {
      binaryInput: '',
      decimalInput: ''
    }
  },

  watch: {
    binaryInput() {
      setTimeout(() => {
        this.convertToDecimal()
      }, 100)
    },
  },

  methods: {
    validateBinaryNumber() {
      setTimeout(() => {
        this.binaryInput = this.binaryInput.replace(/[^0-1]/g, '')
      }, 1)
    },
    validateDecimalNumber() {
      setTimeout(() => {
        this.decimalInput = this.decimalInput.replace(/[^0-9]/g, '')
      }, 1)
    },
    convertToDecimal() {
      let result = 0;
      let length = this.binaryInput.length;
      let lengthRevertForPow = this.binaryInput.length;
      for (let i = 0; i < length - 1; i++) {
        console.log(Math.pow(2, lengthRevertForPow - 1))
        result += parseInt(this.binaryInput[i], 2) * Math.pow(2, lengthRevertForPow - 1);
        lengthRevertForPow--;
      }

      this.decimalInput = result
    }
  }
}
</script>