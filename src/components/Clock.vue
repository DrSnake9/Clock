<template>
    <div id='clock'>
    <p class='date' >{{ setDay }} </p>
    <p class='time'>{{setTime}}</p>
    <p class='text'>Montre sympa en Vue.js par Dr Snake</p>
</div>
</template>

<script>
export default {
  data () {
    return {
      el: '#clock',
      d: new Date(),
      week: ['Dimanche', 'Lundi', 'Mardi', 'Mercredi', 'Jeudi', 'Vendredi', 'Samedi'],
      month: ['Janvier', 'Février', 'Mars', 'Avril', 'Mai', 'Juin', 'Juillet', 'Août', 'Septembre', 'Octobre', 'Novembre', 'Décembre']

    }
  },

  computed: {
    setDay () {
      var dateOfDay = (this.week[this.d.getDay()]) + ' ' + this.d.getDate() + ' ' + (this.month[this.d.getMonth()]) + ' ' + (this.d.getFullYear())
      return dateOfDay
    },
    setTime () {
      var time = ('0' + this.d.getHours()).slice(-2) + ':' + ('0' + this.d.getMinutes()).slice(-2) + ':' + ('0' + this.d.getSeconds()).slice(-2)
      return time
    }
  }
}

</script>

<style>
html,body {
    height: 100%;
}
body {
    background: #0f3854;
    background: radial-gradient(ellipse at center,  #1b695f  0%, #000000 80%);
    background-size: 100%;
}
p {
    margin: 0;
    padding: 0;
}
#clock {
    font-family: 'Share Tech Mono', monospace;
    color: #ffffff;
    text-align: center;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    color: #daf6ff;
    text-shadow: 0 0 20px rgba(10, 175, 230, 1),  0 0 20px rgba(10, 175, 230, 0);}
    .time {
        letter-spacing: 0.05em;
        font-size: 80px;
        padding: 5px 0;
    }
    .date {
        letter-spacing: 0.1em;
        font-size: 24px;
    }
    .text {
        letter-spacing: 0.1em;
        font-size: 12px;
        padding: 20px 0 0;
    }

</style>
