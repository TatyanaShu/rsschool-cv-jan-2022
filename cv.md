# Tatsiana Shuniborova, Minks.
![Tatsiana Shuniborova](img/IMG_20200912_120604.jpg "Tatsiana Shuniborova")


****************
### **About me** 


My name is Tatsiana  Shuniborova. I am from Minsk, Belarus. I graduated Institute of business of BSU on specialty web-design in september 2021. I learned some languages of programming such as: HTML5, CSS3, JavaScript, php. On the lessons of JavaScript we learned native JavaScript, jQuery and some features of animation. I studied some graphic programs such as: Photoshop, corel, adobe animation and 3ds max. 
When i studied in university i did the project for organization of certification and standartization. I did the project on CMS Joomla and did some features on JS. In project i realised a few pages with information about organization, navigation on this site and form of registration.
I learned English a few years ago, and now I am learning this language  again. I graduated some curses of English as: elementary and pre-intermediate levels. 
I like to study and learn something new. I like to work and see the results of my work.
I have good interpersonal skills and very willing to learn and develop new skills. I am reliable and dependable and often seek new responsibilities within a wide range of employment areas. I don't stop in my development. I am always searching new usefull information and trying to use it.  


**************
### **Contact information:**
Phone: +375-29-863-88-11


E-mail: tashu529@gmail.com


Telegram: Татьяна


Discord: ТатьянаШу#2957


gitHub: [TatyanaShu](https://github.com/TatyanaShu?tab=repositories "github TatyanaShu")


**********************
### **Skills:**


* HTML5.0
* CSS3.0/SCSS
* JavaScript (Basic)
* jQuery
* PHP (Basic)
* CMS (Joomla, Wordpress)
* Graphic programs (Photoshop, Adobe Illustrator, Figma, Corel Draw, Adobe Animate)
* Git (Basic)

### **Language**
+ English (A2)
+ Russian (native)
+ Belarussian (native)

### **Education**
University: Institute of Business of BSU, web-design 2020-2021


Belarussian State Tecnologycal University, engineer of certification and standardization 2006-2013


****************
### **Example code:**

```
_//счетчик  цифр на 2 странице_
const timeCount = 10000,
  step = 20;
function outNum(num, elem) {
  let numb = document.querySelector("#" + elem);
  n = 0;
  let timeView = Math.round(timeCount / (num / step));
  let interval = setInterval(() => {
    n<num? (n += step): clearInterval(interval);
    numb.innerHTML = n;
  }, timeView);
}
_// валидация формы регистрации_
function validate() {
  let errList=document.querySelectorAll ("span");
  let userName=document.getElementById('userName');
  console.log(userName);
  let userPhone=document.getElementById('userTelephone');
let item=document.createElement("span"); 
item.innerHTML ="Поле обязательно для заполнения";
  for (let i= errList.length-1; i>=0; i--) {
        errList[i].remove();
    }
    if (!userName.value){
    userName.classList.add("errorList");
    userName.parentNode.insertBefore(item,userName.nextSibling);
    return false;
    } else{
    userName.classList.remove("errorList");
    item.remove();
  }
  if (!userPhone.value){
    userPhone.classList.add("errorList");
    userPhone.parentNode.insertBefore(item,userPhone.nextSibling);
    return false;
  }
  else{
    userPhone.classList.remove("errorList");
    item.remove();
  }
    
    form=document.entered;
    let login=isFullText(userName);
    let phone=isPhone(userPhone);
    return login&& phone;
}
function isFullText(fieldInp) {
  var letters = /^[A-Za-z]+$|^[А-Яа-я]+$/;

  if (fieldInp.value.match(letters)) {
    fieldInp.className = fieldInp.className.replace("alert", "");
    return true;
  } else {
    fieldInp.className = "alert";
    var item = document.createElement("span");
    item.innerHTML = "Имя должно состоять из букв латиницы или кириллицы";
    fieldInp.parentNode.insertBefore(item, fieldInp.nextSibling);
    return false;
  }
}

function isPhone(userPhone) {
  var pattern = /^(\+\d{3})(\d{2})(\d{3})(\d{2})(\d{2})$/;
  if (userPhone.value.match(pattern)) {
    userPhone.className = userPhone.className.replace("alert", "");
    return true;
  } else {
    userPhone.className = "alert";
    var item = document.createElement("span");
    item.innerHTML = "Телефон должен быть формата +375...";
    userPhone.parentNode.insertBefore(item, userPhone.nextSibling);
    return false;
  }
}
```