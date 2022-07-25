<template>
  <div>
    <input @change="onChange" v-model="valorCopy" />
  </div>
</template>

<script>
export default {
  props: {
    valor: {
      type: String,
      default: '1000'
    }
  },
  mounted() {
    this.valorCopy = this.padraoMoedaBrasil.format(this.valorCopy);
  },
  data() {
    return {
      valorCopy: this.valor,
      padraoMoedaBrasil: new Intl.NumberFormat("pt-BR", {
        style: "currency",
        currency: "BRL",
        minimumFractionDigits: 2
      })
    };
  },
  methods: {
    onChange({ target }) {
      this.valorCopy = this.padraoMoedaBrasil.format(target.value);
    }
  }
};
</script>

<style scoped>
</style>