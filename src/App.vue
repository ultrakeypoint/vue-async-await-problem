<template>
  <div></div>
</template>

<script>
export default {
  data() {
    return {};
  },

  mounted() {
    const asyncFunc = async () => {
      let a = await this.resolve(2);
      let b = await this.resolve(2);
      let c = await this.resolve(2);

      console.log('After all promise is executed');
    };

    asyncFunc();
    console.log('Hello World');
  },

  methods: {
    async resolve(time) {
      return new Promise((resolve) => {
        setTimeout(() => {
          resolve('resolve');
        }, time * 1000);
      });
    },
  },
};
</script>
