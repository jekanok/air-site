<!--
<template>
  <div>
    <div class="content" v-for="(infos, index) in sortedInfo " :key="index">
      <div class="row">
        <div class="col-md-4">
          <div class="tiket-buy">
            <div class="logo_brand">
              <img src="../assets/logo_brand.svg" alt>
            </div>
            <div class="tiket_btn">
              <button type="button" class="btn btn-primary btn-lg" @click="click">
                Купить
                <br>
                за {{ convertCurrency(infos.price) | money}}
                <i class="fas fa-ruble-sign"></i>
              </button>
            </div>
          </div>
        </div>
        <div class="col-md-8">
          <div class="tiket-info">
            <div class="row">
              <div class="col-md-4">
                <div class="tiket_time">
                  <span>{{infos.departure_time}}</span>
                </div>
              </div>
              <div class="col-md-4">
                <div class="tiket_transfer">
                  <span v-if="infos.stops > 0 && infos.stops < 2">{{infos.stops}} ПЕРЕСАДКА</span>
                  <span
                    v-if="infos.stops > 0 && infos.stops > 1 && infos.stops < 5"
                  >{{infos.stops}} ПЕРЕСАДКИ</span>
                  <span v-if="infos.stops > 0 && infos.stops > 4">{{infos.stops}} ПЕРЕСАДОК</span>
                </div>
              </div>
              <div class="col-md-4">
                <div class="tiket_time">
                  <span>{{infos.arrival_time}}</span>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-md-4">
                <div class="tiket_from">
                  <span>{{infos.origin}}, {{infos.origin_name}}</span>
                </div>
              </div>
              <div class="col-md-4">
                <div class="air">
                  <i class="fas fa-plane"></i>
                </div>
              </div>
              <div class="col-md-4">
                <div class="tiket_where">
                  <span>{{infos.destination_name}}, {{infos.destination}}</span>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-md-4">
                <div class="tiket_date">
                  <span>{{infos.destination_name}}</span>
                </div>
              </div>
              <div class="col-md-4"></div>
              <div class="col-md-4">
                <div class="tiket_date">
                  <span>{{infos.departure_date}}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ticketsData from "../assets/tickets.json";

export default {
  name: "tikets",
  props: ["course", "translate"],
  data() {
    return {
      info: ticketsData.tickets,
      isActive: true,
      translate: "all"
    };
  },
  methods: {
    convertCurrency(money) {
      return money / this.course;
    },
    click() {
      console.log(this.translate);
    }
  },
  filters: {
    money: function(value) {
      return value.toFixed(2);
    }
  },
  computed: {
    sortedInfo() {
      function compare(a, b) {
        if (a.stops < b.stops) return -1;
        if (a.stops > b.stops) return 1;
        return 0;
      }
      return this.info.sort(compare);
    }
  }
};
</script>
-->