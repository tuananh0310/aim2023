<template>
  <div class="hello">
    <h1 style="color: #48CFAD">{{ msg }}</h1>
    <div><h1 style="color:#E9573F; padding:40px;">{{timerOutput}}</h1></div>
    <ul>
      <li>
       <div style="display:flex">
        <h2 style="padding-right:10px">Node JS</h2>
        <button @click.once="handleCountNode" class="button-45"><h1>{{count}}</h1></button>
       </div>
      </li>
      <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">Animation</h2>
         <button @click.once="handleCountAnimation" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
       <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">Docker</h2>
         <button @click.once="handleCountDocker" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
       <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">TypeScript</h2>
         <button @click.once="handleCountTypeScript" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
       <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">Algorithms</h2>
         <button @click.once="handleCountAl" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
       <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">Postgresql</h2>
         <button @click.once="handleCountPost" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
       <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">Nuxt</h2>
         <button @click.once="handleCountNuxt" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
       <li>
        <div style="display:flex">
         <h2 style="padding-right:10px">EngLish</h2>
         <button @click.once="handleCountEnglish" class="button-45"><h1>{{count}}</h1></button>
        </div>
       </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      count: 0,
      countDownToTime : new Date("Dec 30, 2023 00:00:00").getTime(),
      timerOutput:  null
    }
  },
  props: {
    msg: String
  },
  methods: {
    handleCountNode() {
      this.count = 1800;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountAnimation() {
      this.count = 600;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountDocker() {
      this.count = 900;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountTypeScript() {
      this.count = 1200;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountAl() {
      this.count = 1800;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountPost() {
      this.count = 300;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountNuxt() {
      this.count = 600;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    handleCountEnglish() {
      this.count = 3600;
      let intervalId = setInterval(() => {
        this.count--;
        if (this.count <= 0) {
          clearInterval(intervalId);
        }
      }, 1000);
    },
    startTimer() {
      const timeNow = new Date().getTime();
      const timeDifference = this.countDownToTime - timeNow;
      const millisecondsInOneSecond = 1000;
      const millisecondsInOneMinute = millisecondsInOneSecond * 60;
      const millisecondsInOneHour = millisecondsInOneMinute * 60;
      const millisecondsInOneDay = millisecondsInOneHour * 24;
      const differenceInDays = timeDifference / millisecondsInOneDay;
      const remainderDifferenceInHours = (timeDifference % millisecondsInOneDay) / millisecondsInOneHour;
      const remainderDifferenceInMinutes = (timeDifference % millisecondsInOneHour) / millisecondsInOneMinute;
      const remainderDifferenceInSeconds = (timeDifference % millisecondsInOneMinute) / millisecondsInOneSecond;
      const remainingDays = Math.floor(differenceInDays);
      const remainingHours = Math.floor(remainderDifferenceInHours);
      const remainingMinutes = Math.floor(remainderDifferenceInMinutes);
      const remainingSeconds =Math.floor(remainderDifferenceInSeconds);
      this.timerOutput = remainingDays + " Days " + ": " + remainingHours + " Hours " + ": " + remainingMinutes + " Minutes " + ": " + remainingSeconds + " Seconds";
    }
  },
  mounted() {
       setInterval(() => { this.startTimer() }, 1000);
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

/* CSS */
.button-45 {
  align-items: center;
  background-color: #FFE7E7;
  background-position: 0 0;
  border: 1px solid #FEE0E0;
  border-radius: 11px;
  box-sizing: border-box;
  color: #D33A2C;
  cursor: pointer;
  display: flex;
  font-size: 1rem;
  font-weight: 700;
  line-height: 33.4929px;
  list-style: outside url(https://www.smashingmagazine.com/images/bullet.svg) none;
  padding: 2px 12px;
  text-align: left;
  text-decoration: none;
  text-shadow: none;
  text-underline-offset: 1px;
  transition: border .2s ease-in-out,box-shadow .2s ease-in-out;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
  word-break: break-word;
}

.button-45:active,
.button-45:hover,
.button-45:focus {
  outline: 0;
}


.button-45:active {
  background-color: #D33A2C;
  box-shadow: rgba(0, 0, 0, 0.12) 0 1px 3px 0 inset;
  color: #FFFFFF;
}

.button-45:hover {
  background-color: #FFE3E3;
  border-color: #FAA4A4;
}

.button-45:active:hover,
.button-45:focus:hover,
.button-45:focus {
  background-color: #D33A2C;
  box-shadow: rgba(0, 0, 0, 0.12) 0 1px 3px 0 inset;
  color: #FFFFFF;
}
button {
  height: 50px;
}

li {
  padding: 20px;
}

h2 {
  color: #48CFAD,;
}
</style>
