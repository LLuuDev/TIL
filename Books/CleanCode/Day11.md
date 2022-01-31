# 미션! 더러운 코드를 고쳐라! 2022-01-31

### 더러운 코드를 고치자 🌟
클린 코드 읽으며 무엇이 깨끗한 코드인지, 어떻게 고쳐서 깨끗하게 만들 수 있는지 매일 매일 몸으로 느끼는 중이죠? 직접 깨끗한 코드를 써보며, 실전! 클린코드 해봐요~!

💩 내 더러운 코드좀 봐주세요 💩
제보자 J***님의 코멘트 :
자스챌 할때 크리스마스까지 남은 시간 계산기인데요, 모범답안에서 시,분을 초로 계산하는걸 다르게 했던 것 같은데~! 잘 모르겠어용ㅋㅋ 자스챌 복습하러 가야겠....

```js
const merry = document.querySelector(".js-clock");

function getClock() {
const christmas = new Date("2021, 12, 25");
const date = new Date();
const timeGap = christmas - date;

const xDay = Math.floor(timeGap / (1000 * 60 * 60 * 24));
const xHours = Math.floor(
(timeGap - xDay * 1000 * 60 * 60 * 24) / (1000 * 60 * 60)
);
const xMinutes = Math.floor((timeGap % (60 * 60 * 1000)) / (60 * 1000));
const xSeconds = Math.floor((timeGap % (60 * 1000)) / 1000);

const day = String(xDay).padStart(2, "0");
const hours = String(xHours).padStart(2, "0");
const minutes = String(xMinutes).padStart(2, "0");
const seconds = String(xSeconds).padStart(2, "0");

merry.innerText = `${day}d ${hours}h ${minutes}m ${seconds}s`;
}

getClock();
setInterval(getClock, 1000);
```

청소 완료

```js
const merry = document.querySelector(".js-clock");

function getClock() {
  const christmas = new Date("2021, 12, 25");
  const date = new Date();
  const timeGap = christmas - date;

  const xDay = Math.floor(timeGap / (1000 * 60 * 60 * 24));
  const xHours = Math.floor(
    (timeGap - xDay * 1000 * 60 * 60 * 24) / (1000 * 60 * 60)
  );
  const xMinutes = Math.floor((timeGap % (60 * 60 * 1000)) / (60 * 1000));
  const xSeconds = Math.floor((timeGap % (60 * 1000)) / 1000);

  const day = String(xDay).padStart(2, "0");
  const hours = String(xHours).padStart(2, "0");
  const minutes = String(xMinutes).padStart(2, "0");
  const seconds = String(xSeconds).padStart(2, "0");

  merry.innerText = `${day}d ${hours}h ${minutes}m ${seconds}s`;
}

getClock();
setInterval(getClock, 1000);

```
