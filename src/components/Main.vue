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
               @change="validateNumber(1)"
               @input="validateNumber(1)">
      </div>
      <div class="col-12 col-s-12">
        <input v-model="decimalInput"
               placeholder="Decimal..."
               type="text"
               @change="validateNumber(2)"
               @input="validateNumber(2)">
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
      decimalInput: '',
      type: 1,
    }
  },

  watch: {
    binaryInput() {
      setTimeout(() => {
        this.convert()
      }, 100)
    },
    decimalInput() {
      setTimeout(() => {
        this.convert()
      }, 100)
    },
  },

  methods: {
    validateNumber(type) {
        if (type === 1) {
          setTimeout(() => {
            this.binaryInput = this.binaryInput.replace(/[^0-1]/g, '')
          }, 1);
          this.type = type;
        } else {
          setTimeout(() => {
            this.decimalInput = this.decimalInput.replace(/[^0-9]/g, '')
          }, 1);
          this.type = type;
        }
    },
    convert() {
      if(this.type === 1) {
        this.decimalInput = parseInt(this.binaryInput, 2).toString();
      } else {
        this.binaryInput = parseInt(this.decimalInput).toString(2);
      }


      /**
       * this the second variant of convert to bin2dec
       * this function doesn't work properly
       */
      // let result = 0;
      // let length = this.binaryInput.length;
      // let lengthRevertForPow = this.binaryInput.length;
      // for (let i = 0; i < length - 1; i++) {
      //   console.log(Math.pow(2, lengthRevertForPow - 1))
      //   result += parseInt(this.binaryInput[i], 2) * Math.pow(2, lengthRevertForPow - 1);
      //
      //   if (i === length && parseInt(this.binaryInput[i]) === 1) {
      //     result += 1;
      //   }
      //   lengthRevertForPow--;
      // }
    }
  }
}
</script>