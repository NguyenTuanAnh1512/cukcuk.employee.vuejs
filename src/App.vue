<template>
  <div id="app">
    <Left-menu />

    <Panel-right />

    <Dialog />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import LeftMenu from './components/LeftMenu';
import PanelRight from './components/PanelRight';
import Dialog from './components/Dialog';

export default {
  name: 'app',
  props: {

  },
  data () {
    return {

    }
  },
  components: {
    LeftMenu,
    PanelRight,
    Dialog,
  },
  methods: {

  },
  computed: {

  },

}
</script>

<style>
body{
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0px;
  font-size: 13px;
}

/* file button.css */
.button {
    height: 40px;
    background-color: #019160;
    border-radius: 4px;
    font-size: 13px;
    color: #ffffff;
    padding-left: 24px;
    padding-right: 24px;
    text-align: center;
    border: none;
    outline: none !important;
    min-width: 100px;
}

.button:hover {
    background-color: #2FBE8E;
}

.button:active {
    background-color: #01B075;
}

.button-with-icon {
    background-repeat: no-repeat;
    background-size: 16px;
    background-position: 16px 11px;
    padding-left: calc(16px + 16px + 8px);
    /*background-image: url(/content/icon/search.png);*/
}

.input_radio ~ label {
    vertical-align: middle;
}

.blue_line {
    width: 80px;
    height: 4px;
    background-color: #2d920b;
    margin-top: 5px;
    margin-bottom: 8px;
}

/* file input.css */
.input {
    border: 1px solid #bbbbbb;
    border-radius: 5px;
    height: 40px;
    /*padding: 0 0 0 40px;*/
    box-sizing: border-box;
    font-size: 12px;
    font-size: 13px;
    margin-top: 4px;
    padding-left: 16px;
}

.input:focus {
    outline: none !important;
    border: 1px solid #019160;
}

.input_fail::-webkit-input-placeholder {
    font-size: 12px;
    color: red !important;
}

.input::-webkit-input-placeholder {
    font-size: 12px;
    color: #bbbbbb;
}

/*Lable for Input*/
.input-label {
    font-size: 13px;
    color: #000000;
}

/*Input with icon inside*/
.input-with-icon {
    border: 1px solid #bbbbbb;
    border-radius: 5px;
    height: 40px;
    box-sizing: border-box;
    font-size: 12px;
    font-size: 13px;
    background-image: url('/content/icon/search.png');
    background-repeat: no-repeat;
    background-size: 16px;
    background-position: 10px 10px;
    padding-left: 30px;
}

.hover_tr:hover {
    background-color: #e3e3e3;
}

.icon_dashboard {
    background-image: url('/content/icon/dashboard.png');
}

.icon_report {
    background-image: url('/content/icon/report.png');
}

.icon_dic-employee {
    background-image: url('/content/icon/dic-employee.png');
}

.icon_setting {
    background-image: url('/content/icon/setting.png');
}

.hiden {
    display: none;
}
* {
    box-sizing: border-box;
}
</style>
