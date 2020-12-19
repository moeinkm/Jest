<div dir="rtl">

# Jest | جِست
##  معرفی فریم وُرک جِست 
  <p>
جست یک فریم ورک تست است که سریع و راه اندازی آن ساده است. جست به در این تاریخ به طور مداوم توسط فیسبوک توسعه داده می‌شود و برای تست اپلیکیشن های ریأکت توسط بسیاری از کمپانی های بزرگ از جمله فیسبوک استفاده می‌شود.
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
  
نکته: داکیومنت جست از دستور `yarn`استفاده می‌کند البته `npm` هم قابل استفاده است. برای مقایسه این دو دستور به [این لینک](https://yarnpkg.com/en/docs/migrating-from-npm#toc-cli-commands-comparison) مراجعه کنید.

برای شروع، یک تست برای تابعی فرضی که دو عدد را جمع می&nbsp;کند می&nbsp;نویسیم. ابتدا فایل `sum.js` را می‌.سازیم

</div>

```javascript
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```
<div dir="rtl">

سپس یک فایل به اسم `sum.test.js` می‌سازیم که که در واقع همان فایل تست ماست.
</div>

```javascript
const sum = require('./sum');

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```
<div dir="rtl">
  
قسمت زیر را به `package.json` اضافه می‌کنیم:
</div>

```json
{
  "scripts": {
    "test": "jest"
  }
}
```
<div dir="rtl">
  
در آخر دستور `yarn test` یا `npm run test` را اجرا می‍کنیم و جست پیام زیر را برای ما چاپ می‌کند:
</dir>

```bash
PASS  ./sum.test.js
✓ adds 1 + 2 to equal 3 (5ms)
```

<div dir="rtl">
  
**شما با موفقیت اولین تست را با استفاده از جست نوشتید**
</dir>
<div dir="rtl">
  
 این تست با استفاده از`expect` و `toBe`یکسان بودن مقادیر را سنجید. برای یادگیری بیشتر درباره چیز هایی که می‌توان با جست تست کرد [این لینک ](https://jestjs.io/docs/using-matchers)را ببینید.
  
</div>   

<div dir="rtl">
  
## اجرای جست به صورت کامَند لاین

جست را می&#8204;توان مستقیماً از ترمینال اجرا کرد به شرطی که در `PATH` در دسترس باشد. این کار را می&#8204;توان با دستور `yarn global add jest` یا `npm install jest --global` انجام داد.  

در ادامه نحوه اجرای فایل تست به اسم `my-test` با استفاده از تنظیمات `config.json` آمده است:
</div>

```bash
jest my-test --notify --config=config.json
```

<div dir="rtl">

برای اطلاعات بیشتر راجع به اجرای جست به صورت کامَند لاین به [اسناد جست](https://jestjs.io/docs/en/cli) مراجعه کنید
If you'd like to learn more about running `jest` through the command line, take a look at the [Jest CLI Options](https://jestjs.io/docs/en/cli) page.
</div>
