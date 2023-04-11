<script setup>
const items = [
  ['20金融1', 104.17],
  ['20多媒体设计', 100.00],
  ['20工业设计', 94.44],
  ['20金融2', 82.61],
  ['20电商', 70.71],
  ['20智能制造2', 45.45],
  ['20智能制造1', 0.00],
  ['20第二学位', 0.00],
  ['21金融1', 100.00],
  ['21智能制造1', 97.37],
  ['21工业设计', 94.12],
  ['21计技2班', 95.16],
  ['21计技1班', 75],
  ['21金融2', 86.96],
  ['21智能制造2', 80.56],
  ['22金融2', 151.17],
  ['22金融1', 136.66],
  ['22多媒体设计', 111.50],
  ['22电商2班', 113.33],
  ['22电商1班', 161.11],
  ['22工业设计', 102.08],
  ['22智能制造2', 134.92],
  ['22第二学位', 188.95],
].sort((a, b) => b[1] - a[1]);

let sum = 0;
items.forEach(i => sum+= i[1]);
const percent = (sum / items.length).toFixed(2);
</script>

<template>
  <div class="bg">
    
    <img width="512" src="/head.png" />
    <!-- <img width="512" src="/head1.png" />
    <div class="rate-box">
      粤台产业科技学院参学率
      <div>
          {{percent}}%
      </div>
    </div>
    <img width="512" src="/head2.png" /> -->
    <div>
      <div v-for="(item, index) in items" class="list-item">
        <img v-if="index==0" src="/金牌.png" />
        <img v-if="index==1" src="/银牌.png" />
        <img v-if="index==2" src="/铜牌.png" />
        <span v-if="index>2">{{ index + 1 }}</span>
        <span>{{ item[0] }}</span>
        <span>{{ item[1] }}%</span>
      </div>
      <p style="text-align: end;">*数据截止至2023年4月11日</p>
      <p>粤台产业科技学院团委学生会|宣</p>
    </div>
  </div>
</template>

<style scoped>
.bg {
  width: 512px;
  background-color: #dbd2fb;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}

span {
  color: black;
}

/* .list-item img {
  height: auto;
} */

p {
  color: black;
  font-size: 24px;
}

.rate-box {
  height: 64px;
  width:340px;
  margin-right: 16px;
  background-color: #f6d46d;
  display: flex;
  color:black;
  font-size: 20px;
  font-weight: bold;
  justify-items: center;
  align-items: center;
  padding-left: 16px;
  align-self: flex-end;
}

.rate-box div {
  background-color: #d9d3f8;
  flex: 1;
  height: 56px;
  margin: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.list-item {
  width: 350px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  font-size: 24px;
  border-radius: 12px;
  padding-left: 24px;
  padding-right: 24px;
}
.list-item span:first-child {
  width: 16px;
}

.list-item :nth-child(2) {
  flex: 1;
  display: flex;
  justify-content: left;
  padding-left: 16px;
  /* color:aqua; */
}
.list-item:first-child {
  background-color: #fbe49a;
}

.list-item:nth-child(2) {
  background-color: #d7f3fd;

}

.list-item:nth-child(3) {
  background-color: #eed3fc;
}

.list-item:first-child,
.list-item:nth-child(2),
.list-item:nth-child(3) {
  font-size: 32px;
  box-shadow: rgba(0, 0, 0, 0.5) 0 0 8px;
  margin-bottom: 16px;
}

.list-item:nth-child(even) {
  background-color: #d7f3fe;
}
</style>
