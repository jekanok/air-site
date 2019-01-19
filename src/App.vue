<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="logo d-flex justify-content-center"> <img src="./assets/logo.svg" alt="Авиа билеты"> </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-3">
          <!-- <corren></corren> -->
        </div>

        <div class="col-md-9">
          <!-- <tikets></tikets> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>

<style>
html,
body,
#app {
  height: 100%;
}

.logo {
  margin: 50px 0px;
}
.menu {
  box-shadow: 0 1px 4px rgba(91, 137, 164, 0.25);
  border-radius: 5px;
  background-color: #ffffff;
  padding: 20px;
}
.content {
  box-shadow: 0 1px 4px rgba(91, 137, 164, 0.25);
  border-radius: 5px;
  background-color: #ffffff;
  margin-bottom: 16px;
  /*    padding: 20px;*/
}

.menu span {
  text-transform: uppercase;
  font-weight: 600;
  padding: 5px 0px;
  color: #4a4a4a;
}
.menu button {
  text-transform: uppercase;
}
.menu .btn-group {
  padding: 5px 0;
}
.menu .btn-secondary:not(:disabled):not(.disabled).active,
.btn-secondary:not(:disabled):not(.disabled):active,
.show > .btn-secondary.dropdown-toggle {
  background-color: #2196f3;
  border: 1px solid #2196f3;
}
.menu .btn-secondary {
  background-color: #ffffff;
  color: #2196f3;
  border: 1px solid #d2d5d6;
  font-weight: 300;
}
.corren {
  margin-bottom: 20px;
}
.list-air {
  margin-top: 6px;
}
.menu .btn-group-vertical > .btn:hover,
.btn-group > .btn:hover {
  background-color: #f2fcff;
  border: 1px solid #64b5f5;
}
.menu .list-group-item {
  border: none;
  font-size: 13px;
  padding: 0.75rem 0rem;
}

.menu .list-group-item:hover {
  background-color: #f1fcff;
}
.form-check {
  padding: 0px 15px;
}
.form-check a {
  color: #4a4a4a;
  text-decoration: none;
}
.menu .list-group-item:hover:after {
  content: "Только";
  padding-right: 10px;
  text-transform: uppercase;
  color: #2196f3;
  letter-spacing: 0.5px;
  float: right;
  display: flex;
  justify-content: flex-end;
}
/* прячем input checkbox */
.form-check input[type="checkbox"] {
  display: none;
}

/* стили для метки */
.form-check label {
  position: relative;
  vertical-align: middle;
}

/* формируем внешний вид чекбокса в псевдоэлементе before */
.form-check label:before {
  content: "";
  color: #000;
  display: inline-block;
  border-radius: 3px;
  -webkit-border-radius: 3px;
  -o-border-radius: 3px;
  -moz-border-radius: 3px;
  position: relative;
  text-align: center;
  text-indent: 0px;
  width: 19px;
  height: 19px;
  background: #fff;
  border: 1px solid #d2d5d6;
  border-image: initial;
  vertical-align: middle;
}

/* вариации внешнего вида в зав-ти от статуса checkbox */
/* checked */
.form-check input:checked + label:before {
  content: "\f00c";
  color: #2196f3;
  border: 1px solid #2196f3;
}
.form-check input[type="checkbox"]:checked + label:after {
  position: relative;
  top: 10px;
  right: 0px;
}
/* disabled */
.form-check input:disabled + label:before {
  background: #eee;
}
.btn-primary {
  padding: 13px 63px;
  background-color: #ff6d00;
  border: none;
  font-size: 16px;
  text-align: center;
  box-shadow: 0 2px 1px rgba(0, 0, 0, 0.1), 0 1px 0 #d64d08;
}
.btn-primary:hover {
  background-color: #d96007;
}
.tiket-buy {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  border-right: 1px solid #eceff1;
  padding: 25px 0;
}
.logo_brand {
  padding: 10px 0px;
}
.tiket_btn {
  padding: 13px 0;
}
.tiket_time span {
  font-size: 32px;
  line-height: 26px;
}
.tiket_transfer {
  font-size: 10px;
  color: #8b9497;
  line-height: 12.1px;
  font-weight: 600;
}
.tiket_from,
.tiket_where {
  font-size: 12px;
  color: #4a4a4a;
  line-height: 18px;
  font-weight: 600;
}
.tiket_date {
  color: #8b9497;
}
.tiket-info {
  margin: 60px 0 0 0;
}
i {
  font-weight: 300;
  font-size: 13px;
}
.air {
  width: 96px;
  height: 1px;
  background-color: #d2d5d6;
}
.air i {
  color: #d2d5d6;
  position: relative;
  right: -99px;
  top: -8px;
  font-size: 16px;
}
</style>
