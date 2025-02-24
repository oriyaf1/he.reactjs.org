---
id: glossary
title: רשימת מונחי React
layout: docs
category: Reference
permalink: docs/glossary.html

---

## אפליקציית Single-page {#single-page-application}

אפליקציית single-page היא אפליקצייה שטוענת עמוד HTML אחד ואת כל הנכסים (כגון קבצי JavaScript ו-CSS) הדרושים כדי שהאפליקצייה תרוץ. כל אינטראקציה עם הדף או עם הדפים הבאים אינה דורשת נסיעה הלוך ושוב לשרת, כלומר הדף אינו נטען מחדש.

למרות שאתם יכולים לבנות אפליקציית single-page ב-React, זוהי אינה דרישה. React יכולה לשמש גם לשיפור חלקים קטנים של אתרים קיימים עם אינטראקטיביות נוספת. קוד שנכתב ב-React יכול להתקיים בשלום עם markup שרונדר בשרת על ידי משהו כמו PHP, או עם ספריות אחרות בצד הלקוח. למעשה, זה בדיוק האופן בו React נמצאת בשימוש בפייסבוק.

## ES6, ES2015, ES2016, וכו' {#es6-es2015-es2016-etc}

ראשי תיבות אלה מתייחסים לגרסאות העדכניות ביותר של תקן מפרט השפה ECMAScript, אשר שפת JavaScript היא יישום שלה. גרסת ES6 (הידועה גם בשם ES2015) כוללת תוספות רבות לגרסאות הקודמות כגון: פונקציות חץ, מחלקות, תבניות שגיאת דפוס, הצהרות `let` ו-` const`. תוכלו ללמוד עוד על גרסאות ספציפיות [כאן]

ראשי תיבות אלה מתייחסים לגרסאות העדכניות ביותר של תקן מפרט השפה ECMAScript, אשר שפת JavaScript היא יישום שלה. גרסת ES6 (הידועה גם בשם ES2015) כוללת תוספות רבות לגרסאות הקודמות כגון: פונקציות חץ, מחלקות, תבניות שגיאת דפוס, הצהרות `let` ו-` const`. תוכלו ללמוד עוד על גרסאות ספציפיות [כאן](https://en.wikipedia.org/wiki/ECMAScript#Versions).

## מהדרים {#compilers}



מהדר JavaScript לוקח קוד JavaScript, משנה אותו ומחזיר קוד JavaScript בפורמט אחר. מקרה השימוש הנפוץ ביותר הוא לקחת תחביר ES6 ולהפוך אותו לתחביר שדפדפנים ישנים מסוגלים לפרש. [Babel](https://babeljs.io/) הוא המהדר הנפוץ ביותר בשימוש עם React.

## מאגדים {#bundlers}


מאגדים לוקחים קוד JavaScript ו-CSS שנכתב בתור מודולים נפרדים (לעתים קרובות מאות מהם), ומאגדים אותם יחד לתוך כמה קבצים בעלי אופטימיזציה טובה יותר עבור הדפדפנים. כמה מאגדים בשימוש נפוץ באפליקציות React כוללים יישומים כוללים את [Webpack](https://webpack.js.org/) ו-[Browserify](http://browserify.org/).

## מנהלי חבילות {#package-managers}

מנהלי חבילות הם כלים המאפשרים לך לנהל תלויות בפרויקט שלך. [npm](https://www.npmjs.com/) ו-[Yarn](https://yarnpkg.com/) הם שני מנהלי חבילות בשימוש נפוץ באפליקציות React. שניהם לקוחות עבור אותו מרשם חבילות npm.

## CDN {#cdn}

CDN מייצג Content Delivery Network (רשת אספקת תוכן). CDN-ים מספקים מטמון תוכן סטאטי מתוך רשת של שרתים ברחבי העולם. 

## JSX {#jsx}

JSX היא תוספת תחביר עבור JavaScript. היא דומה לשפת תבנית, אבל יש לה את מלוא העוצמה של JavaScript. JSX מתקמפלת לקריאות `React.createElement()` שמחזירות אובייקטי JavaScript פשוטים הנקראים "אלמנטיי React". כדי לקבל מבוא בסיסי ל-JSX [צפו בתיעוד כאן](/docs/introducing-jsx.html) ותוכלו למצוא הדרכה מעמיקה יותר על JSX [כאן](/docs/jsx-in-depth.html).

React DOM משתמשת בקונבנצית מתן שמות של מאפיינים ב-camelCase במקום בשמות של תכונות HTML. לדוגמה, `tabindex` הופך ל-`tabIndex` ב-JSX. המאפיין `class` גם נכתב בשם `className` מכיוון ש-`class` היא מילה שמורה ב-JavaScript:

<<<<<<< HEAD
```js
const name = 'תפוזינה';
ReactDOM.render(
  <h1 className="hello">השם שלי הוא {name}!</h1>,
  document.getElementById('root')
);
```  
=======
```jsx
<h1 className="hello">My name is Clementine!</h1>
```
>>>>>>> 84ad3308338e2bb819f4f24fa8e9dfeeffaa970b

## [אלמנטים](/docs/rendering-elements.html) {#elements}

אלמנטים של React הם אבני הבניין של אפליקציות React. אפשר לבלבל אלמנטים עם קונספט נרחב יותר של "קומפוננטות". אלמנט מתאר את מה שאתם רוצים לראות על המסך. אלמנטים של React אינם ניתנים לשינוי (הם immutable).

```js
const element = <h1>שלום, עולם</h1>;
```

בדרך כלל, אלמנטים אינם נמצאים בשימוש ישיר, אלא מוחזרים מקומפוננטות.

## [קומפוננטות](/docs/components-and-props.html) {#components}

קומפוננטות React הם חלקי קוד קטנים, הניתנים לשימוש חוזר המחזירים אלמנט React שירונדר לדף. הגרסה הפשוטה ביותר של קומפוננטות React היא פונקציית JavaScript פשוטה שמחזירה אלמנט React:

```js
function Welcome(props) {
  return <h1>שלום, {props.name}</h1>;
}
```

קומפוננטות יכולות גם להיות מחלקות ES6:

```js
class Welcome extends React.Component {
  render() {
    return <h1>שלום, {this.props.name}</h1>;
  }
}
```

ניתן לפצל קומפוננטות לחלקים שונים של פונקציונליות ולהשתמש בהן בתוך קומפוננטות אחרות. קומפוננטות יכולות להחזיר קומפוננטות אחרות, מערכים, מחרוזות ומספרים. כלל אצבע טוב הוא שאם חלק ממשק המשתמש שלכם נמצא בשימוש מספר פעמים (כפתור, פאנל, אווטר), או שהוא מורכב מספיק בפני עצמו (אפליקציה, פיד סיפורים, תגובה), הוא מועמד טוב להיות רכיב לשימוש חוזר . שמות רכיבים צריכים תמיד להתחיל עם אות רישית (`<Wrapper/>` **ולא** `<wrapper/>`). ראה [תיעוד זה](/docs/components-and-props.html#rendering-a-component) לקבלת מידע נוסף על רינדור קומפוננטות.

### [`props`](/docs/components-and-props.html) {#props}

`props` הם קלטים לקומפוננטות React. הם נתונים המועברים למטה מקומפוננטת הורה לקומפוננטת ילד.

זכרו ש-`props` הם לקריאה-בלבד. הם לא צריכים להשתנות בשום דרך שהיא:

```js
// טעות!
props.number = 42;
```

אם עליכם לשנות ערך כלשהו בתגובה לקלט משתמש או לתגובת רשת, השתמשו ב-`state` במקום זאת.

### `props.children` {#propschildren}

`props.children` זמין בכל קומפוננטה. הוא מכיל את התוכן בין תגי הפתיחה והסגירה של קומפוננטה. לדוגמה:

```js
<Welcome>שלום עולם!</Welcome>
```

המחרוזת `Hello world!` זמינה ב-`props.children` בקומפוננטת `Welcome`:

```js
function Welcome(props) {
  return <p>{props.children}</p>;
}
```

עבור קומפוננטות המוגדרות כמחלקות, השתמשו ב-`this.props.children`:

```js
class Welcome extends React.Component {
  render() {
    return <p>{this.props.children}</p>;
  }
}
```

### [`state`](/docs/state-and-lifecycle.html#adding-local-state-to-a-class) {#state}

קומפוננטה צריכה `state` כאשר נתונים כלשהם המשויכים אליה משתנים עם הזמן. לדוגמה, קומפוננטת `Checkbox` עשויה להזדקק ל-`isChecked` ב-`state` שלה, וקומפוננטת `NewsFeed` עשויה לרצות לעקוב אחרי `fetchedPosts` ב-`state` שלה.

ההבדל החשוב ביותר בין `state` ל-`props` הוא ש-`props` מועברים מקומפוננטת הורה, אבל `state` מנוהל על ידי הקומפוננטה עצמה. קומפוננטה לא יכולה לשנות את ה-`props` שלה, אבל היא כן יכולה לשנות את ה-`state` שלה.

עבור כל פיסה מסוימת של נתונים משתנים, צריך להיות רק קומפוננטה אחת שתהיה "הבעלים" של אותו מידע ב-`state` שלה. אל תנסו לסנכרן `state` של שני קומפוננטות שונות. במקום זאת, [הרימו אותו למעלה](/docs/lifting-state-up.html) אל האב הקדמון המשותף הקרוב ביותר שלהם, והעבירו אותו למטה בתור `props` לשתי הקומפוננטות.

## [מתודות מעגל חיים](/docs/state-and-lifecycle.html#adding-lifecycle-methods-to-a-class) {#lifecycle-methods}

מתודות מעגל חיים הן פונקציונליות מותאמת אישית המורצת במהלך השלבים השונים של קומפוננטה. ישנן מתודות זמינות כאשר הקומפוננטה נוצרת ונוספת ל-DOM ([mounting](/docs/react-component.html#mounting)), כאשר הקומפוננטה מתעדכנת, וכאשר הקומפוננטה נהיית unmounted או מוסרת מה-DOM.

 ## [קומפוננטות מבוקרות](/docs/forms.html#controlled-components) נגד [בלתי-מבוקרות](/docs/uncontrolled-components.html)

ל-React יש שתי גישות שונות להתמודד עם קלטי טופס.

אלמנט קלט של טופס שערכו נשלט על ידי React נקרא *קומפוננטה מבוקרת*. כאשר משתמש מזין נתונים לקומפוננטה מבוקרת, מופעל מטפל של אירוע שינוי והקוד שלכם מחליט אם הקלט וולידי (על-ידי רינדור מחדש עם הערך המעודכן). אם לא תרנדרו מחדש, אלמנט הטופס יישאר ללא שינוי.

*קומפוננטה בלתי מבוקרת* עובדת כמו שאלמנטים של טופס עובדים מחוץ ל-React. כאשר משתמש מכניס נתונים לתוך שדה טופס (תיבת קלט, תפריט נפתח וכו') המידע המעודכן משתקף ללא צורך ש-React תעשה שום דבר. עם זאת, זה גם אומר שאתם לא יכולים להכריח את השדה שיכיל ערך מסוים.

ברוב המקרים יהיה עליכם להשתמש בקומפוננטות מבוקרות.

## [מפתחות](/docs/lists-and-keys.html) {#keys}

"מפתח" הוא מאפיין מחרוזת מיוחדת שעליכם לכלול בעת יצירת מערכים של אלמנטים. מפתחות עוזרים ל-React לזהות אילו פריטים השתנו, נוספו או הוסרו. המפתחות צריכים להינתן לאלמנטים בתוך מערך על מנת לתת לאלמנטים זהות קבועה.

מפתחות צריכים להיות ייחודיים רק בין אלמנטים אחים באותו מערך. הם לא צריכים להיות ייחודיים על פני האפליקציה כולה או אפילו קומפוננטה אחת.

אל תעביר משהו כמו `Math.random()` למפתחות. חשוב שלמפתחות תהיה "זהות קבועה" על פני רינדורים מחדש כך ש-React תוכל לקבוע מתי פריטים מתווספים, מוסרים, או מאורגנים מחדש. באופן אידיאלי, מפתחות צריכים להתאים למזהים ייחודיים וקבועים שמקורם בנתונים שלכם, כגון `post.id`.

## [Refs](/docs/refs-and-the-dom.html) {#refs}

React תומכת במאפיין מיוחד שניתן לצרף לכל קומפוננטה. התכונה `ref` יכולה להיות אובייקט שנוצר על ידי [פונקציית `React.createRef()`](/docs/react-api.html#reactcreateref) או פונקציית callback, או מחרוזת (ב-API מגירסאות קודמות). כאשר התכונה `ref` היא פונקציית callback, הפונקציה מקבלת את אלמנט ה-DOM הבסיסי או את מופע המחלקה (בהתאם לסוג האלמנט) כארגומנט שלה. זה מאפשר לכם גישה ישירה לאלמנט ה-DOM או מופע הקומפוננטה.

השתמשו ב-refs בואפן חסכני. אם אתם מוצאים את עצמכם משתמשים ב-refs לעתים קרובות כדי "לגרום לדברים לקרות" באפליקציה שלכם, שקלו לבצע היכרות טובה יותר עם [זרימת נתונים מלמעלה-למטה](/docs/lifting-state-up.html).

## [אירועים](/docs/handling-events.html) {#events}

לטיפול באירועים עם אלמנטי React יש כמה הבדלים תחביריים:

* מטפלי אירועים של React נקראים באמצעות camelCase, במקום באותיות קטנות.
* עם JSX אתם מעבירים פונקציה כמטפל האירוע, ולא מחרוזת.

## [התאמה](/docs/reconciliation.html) {#reconciliation}

כאשר ה-props או ה-state של קומפוננטה או משתנים, React מחליטה אם יש צורך בעדכון DOM בפועל על-ידי השוואת האלמנט החדש שהוחזר עם האלמנט הקודם שרונדר. כאשר הם לא זהים, React יעדכן את ה-DOM. תהליך זה נקרא "התאמה".
