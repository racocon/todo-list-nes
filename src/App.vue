<template>
  <div id="app">
      <link href="https://fonts.googleapis.com/css?family=Press+Start+2P" rel="stylesheet">
      <link href="https://unpkg.com/nes.css/css/nes.css" rel="stylesheet" />
      
      
    <el-row :gutter="20">
      <el-col :span="12" :offset="6">
        <el-card>
          <div class="center-align">
            <i class="nes-octocat animate"></i>
          </div>

          <br>
          
          <Todo/>
        </el-card>
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

</style>
