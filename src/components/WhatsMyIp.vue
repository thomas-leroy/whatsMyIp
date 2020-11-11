<template>
  <div class="container">
    <div class="myIp">
      <p>{{ ip }}</p>
    </div>

    <div class="otherStuff">
      <p>
        Viewport size: <br />
        {{ browser.width }}px x {{ browser.height }}px <br />
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WhatsMyIp',
  data () {
    return {
      ip: null,
      browser: {
        width: window.innerWidth || document.body.clientWidth,
        height: window.innerHeight || document.body.clientHeight,
      },
    }
  },
  created() {
    // Get user api
    fetch(process.env.VUE_APP_API_BASE_URL)
      .then(response => response.json())
      .then(data => (this.ip = data.ip));

    // Update browser size
    window.addEventListener('resize', this.watchResize);
  },
  methods: {
    watchResize() {
      this.browser.width = window.innerWidth || document.body.clientWidth;
      this.browser.height = window.innerHeight || document.body.clientHeight;
    },
  }
}
</script>

<style scoped>
  .container{
    display: flex;
    height: 100%;
  }

  .myIp, .otherStuff{
    display: flex;
    flex: 1;
    width: 50%;
    height: 100%;
    color: white;
    vertical-align: middle;
    background-color: darkslategrey;
  }

  p{
    font-size: 7vw;
    font-weight: 700;
    margin: auto; /* Important */
    text-align: center;
  }

  .otherStuff{
    background-color: white;
  }

  .otherStuff p{
    color: black;
    font-size: 15px;
  }
</style>
