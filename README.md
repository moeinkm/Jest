<div dir="rtl">

# Jest | جِست
##  معرفی فریم وُرک جِست 
  <p>
جست یک فریم ورک تست است که سریع و راه اندازی آن ساده است. جست به در این تاریخ به طور مداوم توسط فیسبوک توسعه داده می شود و برای تست اپلیکیشن های ریأکت توسط بسیاری از کمپانی های بزرگ از جمله فیسبوک استفاده می شود.
  </p>

</div>


<div dir="rtl">

نسب جست با [`yarn`](https://yarnpkg.com/en/package/jest):

</div>

```bash
yarn add --dev jest
```

<div dir="rtl">
  
یا [`npm`](https://www.npmjs.com/package/jest):
</div>

```bash
npm install --save-dev jest
```
<div dir="rtl">
  
نکته: داکیومنت جست از دستور `yarn` استفاده می&nbsp;کند البته `npm` هم قابل استفاده است. برای مقایسه این دو دستور به [این لینک](https://yarnpkg.com/en/docs/migrating-from-npm#toc-cli-commands-comparison) مراجعه کنید.

برای شروع، یک تست برای تابعی فرضی که دو عدد را جمع می&nbsp;کند می&nbsp;نویسیم. ابتدا فایل `sum.js` را می&nbsp;.سازیم

</div>

```javascript
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```
<div dir="rtl">
  سپس یک فایل به اسم `sum.test.js` می&nbsp;سازیم که که در واقع همان فایل تست ماست.
