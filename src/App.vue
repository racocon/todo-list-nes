<template>
  <div id="app">
      <link href="https://fonts.googleapis.com/css?family=Press+Start+2P" rel="stylesheet">
      <link href="https://unpkg.com/nes.css/css/nes.css" rel="stylesheet" />
      
      
    <el-row :gutter="20">
      <el-col :span="12" :offset="6">
          <div class="nes-container is-rounded white-bg">

            <section class="message-list center-align">
              <section class="message -right">
                <!-- Balloon -->
                <div class="nes-balloon from-right">
                  <p>Hello! Here's your todo list!</p>
                </div>
                <i class="nes-octocat animate" style="height: 20px"></i>
              </section>
            </section>

          <!-- <div class="center-align">
            <i class="nes-octocat animate"></i>
          </div> -->
          <br>
          <br>
          <br>
          
          <Todo/>
          
          <br>
          <br>

          <div class="center-align">
            <a href="https://github.com/racocon" target="_blank" aria-label="github"><i class="nes-icon github is-medium"></i></a>
          </div>

          <br>

          </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import Todo from './components/Todo'

export default {
  name: 'App',
  components: {
    Todo
  }
}
</script>

<style>
html,
body,
pre,
code,
kbd,
samp {
  font-family: "Press Start 2P";
}

body {
  background: #466368;
  background: linear-gradient(to right bottom, #648880, #293f50);
  height: 100%;
  margin: 0;
  background-repeat: no-repeat;
  background-attachment: fixed;
  padding: 20px;
}

.white-bg {
  background: #fff;
}

#app {
  border-radius: 4px;
  padding: 20px;
  transition: all 0.2s;
}

.padding {
  padding: 1px 7px 2px;
}

.flex {
  display: flex;
}

.space {
  flex-grow: 1;
}

.center-align {
  text-align: center;
}

.el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }

.el-col {
  border-radius: 4px;
}

.nes-balloon {
  width: 300px;
}

</style>
