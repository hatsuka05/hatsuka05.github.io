---
title: Weekend reading 1
date: 2022-05-21 22:41:19
tags:
---
### Austin-Texas startup that bloomed in 2021

1. WP Engine
Size: 251-500 - $: 290.7m - Founder: 3
Wordpress CMS
2. Disco
Size: 251-500 - $: 233.6m - Founder: 3
SaaS: AI solutions for lawyers, automate and simplify complex and error-prone tasks that distract from practicing law
3. SparkCognition
Size: 101-250 - $: 163.3$ - Founder: 1
SaaS: AI solutions that enable organization to optimize processes, predict future outcome, 
4. ClearData
Size: 101-250 - $: 80.4m - Founder: 4
SaaS: giải pháp bảo mật dữ liệu thông ty y tế cho các cở sở y tế
5. Billd
Size: 51-100 - $: 90m - Founder: 2
#Fintech #Xây dựng: cho phép các nhà thầu trả sau trong vòng 120 ngày để nhận được vật liệu xây dựng
6. InKind
Size: 11-50 - $: 6.5m - Founder: 3
Sử dụng food credit thu mua nguyên liệu và cung cấp cho các nhà hàng
Food Credit: Khoản vay do các bank cung cấp cho các công ty thực phẩm để thu mua thực phẩm từ farmer
7. Ontic
Size: 51-100 - $: 16.7m - Founder: 3
Bảo mật doanh nghiệp, phòng chống bạo lực và các vấn đề an ninh doanh nghiệp
8. Place Technology
Size: 11-50 - $: 5.7m - Founder: 2
SaaS: Cung cấp các phần mềm tài chính hỗ trợ doanh nghiệp ra quyết định kinh doanh
9. OJO Labs
Size: 251-500 - $: 134m - Founder: 2
AI solutions tư vấn mua nhà, tìm kiếm bđs ...
10. Workrise
Size: 501-1000 - $: 752.5 - Founder: 3
Cung cấp + đào tạo lao động cho các ngành liên quán đến năng lượng (năng lượng mặt trời, dầu khí)
11. Outdoorsy
Size: 101-250 - $: 195.1m - Founder: 4
Cho thuê RV ở 1 số khu vực có view đẹp
RV: xe bán tải có tích hợp khôg gian giải trí bên trong
12. CesiumAstro
Size 11-50 - $: 28.2m - Founder: 1
Out-of-the-box communications systems for satellites and other space-faring vehicles
13. FloorFound
Size: 1-10 - $: 4.7m - Founder: 1
Cung cấp giải pháp xử lý đổi trả hàng, bán hàng tồn kho
14. Ibble
Size: 11-50 - $: 0 - Founder: 3
Video contents like tiktok
15. Interplaylearning
Size: 51-100 - $: 12.5m - Founder: 1
Sử dụng thực tế ảo + in 3D để đào tạo nghề
16. Literati
Size: 101-250 - $: 52m - Founder: 2
subscription-based platform where users can get books on a regular basis
17. Spruce
Size: 11-50 - $: 14.6 - Founder: 2
offer whole-house cleans, tidy-ups or single room requests
18. Wheel
Size: 101-250 - $: 65.6 - Founder: 3
Chăm sóc sức khoẻ online bằng nền tảng kết nối bác sỹ với người cần tư vấn sức khoẻ
19. Stoplight
Size: 51-100 - $: 20.4$ - Founder: 1
Cung cấp giải pháp phát triển, quản lý, trực quan hoá API cho doanh nghiệp
20. Raundris
Size: 1-10 - $: 1.5m - Founder: 2
B2B giặt là, realtime tracking
21. Check
Size: 1-10 - $: 0.1m - Founder: 1
Gửi tin nhắn, video trong trường hợp khẩn cấp

### The smarter you are, the more you doubt yourself
Don’t delegate. So what to delegate: Time-consuming task, repetitive things that steal your joy, task with hight learning curve (the more we spend your seconds learning how to do something, the less time we have to actually do it)

Đưa ra nhiều giả định. => thật sự nguy hiểm khi 1 người nghĩ rằng họ thật sự biết về điều mà họ không thực sự biết

Think instead of doing. Everyone has a plan until they get a punched in the mouth

Fear imperfection. But perfection doesn't exist.

### 5 realtime nodejs lib ruling in 2022
1. Socket.io 
2. Express
3. Koa.js: next generation web framework design by team bihind express. more expressive, smaller, more robust foundation
4. Meteor.js: allows for rapid prototyping and produces cross-platform code 
5. Nest.js

### code like there is no if-else
-> https://medium.com/@shirkavand/code-like-there-is-no-if-statement-36ca170c2b92
-> TODO: using c++ to implement linked list, create func to remove 1 entry

### Deno.js
Về cơ bản nó là viết lại engine javascript của nodejs.
(+) Native typescript
(-) Có ít sự lựa chọn hơn trong các package
(?) Các quyền truy cập tệp, mạng, ... cần được khai báo rõ ràng *[Refs](https://deno.land/manual/getting_started/permissions)

### I work as a technical directory at Pixar
What does that mean?
Strong passion for both arts and sciences and knew i would have to continue with both.
Learned from folks across the studio, attended Production Technology meetings, sat in on a scratch recording session, walked through war rooms filled with concept art from in-progress films, attended movie screenings, and stayed late scrolling through the latest work published from the day.
... Phần đằng sau đọc chán quá nên thôi không ghi nữa :D

### ES2022 (ES13) | Most wanted features 
#### Declare a field inside a Class without having a constructor
```js
class Post {
  title = 'posttitle';
}
```

#### Private field and method
```js
class Post {
  title = 'default_title';
  #password = 'default_password';

  // if have no set, we cant set update value of password in contructor block
  set #password(pass) {
    this.#password = pass;
  }

  contructor() {
	this.#password = 'update_password';
  }

  getPasswordNotPrivateFunc = () => {
    return this.#password;
  }

  #getPasswordPrivateFunc = () => {
    return this.#password;
  }
}

const testPost = new Post();

console.log(testPost.title); // default_title
console.log(testPost.#password); // can't be access private field
console.log(testPost.getPasswordNotPrivateFunc()); // ok
console.log(testPost.#getPasswordPrivateFunc()); // can't be access private method
```

#### at() func
```js
const list = [1, 2, 3];

// instead of 
console.log(list[list.length - 2) // output: 2

// now we can do that
console.log(list.at(-2)) // output: 2
```


### Tools you must try for startup
Marketing: Mailchimp, Google Analytics
Sales: hubspot
Data and Analytics: Google data studio, maptive
Finance: Gusto, Expensify
Communication: Slack, Trello

### Monica Sai Kambala: preparation and interview experience - Google Software Engineer
I went awry trying to practice from every coding platform, every Youtube playlist, every coding interview book and after a few weeks, I didn’t know what I practised.
Narrowed down my resources to Leetcode and Narasimha Karumanchi’s “Data Structures and Algorithmic Thinking with Python”.
Xem các thảo luận ở  mục "Discuss" in Leetcode để có thêm các ý tưởng.
Quản lý thời gian: Phỏng vấn kéo dài 45 phút => thời gian để tiếp cận vấn đề và viết mã là trong 20-25 phút
Think out loud. Important question: Do they want you to work with them in a team? Người phỏng vấn quan sát cách bạn giải quyết vấn đề, nên không cần quá tập trung vào việc bạn giải quyết vấn đề đó đúng hay sai. Ngay cả khi bạn đưa ra giải pháp trong 10 phút, nếu bạn không trình bày được suy nghĩ của mình thì cuộc phỏng vấn cũng sẽ không mấy tốt đẹp.

### Đọc sách Technicals một cách hiệu quả
Cần hiểu được những điều sau:
- Hiểu các thuật ngữ
- Biết khi nào nên dừng lại. Đôi lúc không phải vùi đầu vào lý thuyết quá lâu là hiệu quả, hãy bắt tay thực hiện sớm nhất
- Ghi chú
Các bước:
- Đọc phần lời nói đầu
=> Mục đích để hiểu cuốn sách này nói về điều gì, ai nên đọc, cấu trúc sách, cách để đọc
- Scanning:
=> Đi qua nhanh các tiêu đề lớn, các hình ảnh
- Đọc lướt:
=> Đọc câu đầu tiên và cuối cùng mỗi đoạn
=> Đọc chú thích
=> Đọc các đoạn mã
=> Mục đích là để cố gắng ghi nhớ những gì có vẻ sẽ quan trọng 
- Complete reading
=> Đọc hết một chương, mapping đến những phần đã ghi chú trong quá trình đọc lướt

### Blockchain layers L0, L1, L2, L3
![Blockchain layers](blockchain_layers.png)
#### L0
Nơi cài đặt phần cứng, connections, internet để cho phép layer 1 ví dụ như Bitcoin hoạt động. Một dApp có thể tự động chạy trên nhiều khối miễn là các khối xử dụng cùng layer 0
#### L1
Xử lý và hoàn thiện các transactions
Các thuật toán đồng thuật ví dụ như (PoW, PoS) được cài đặt ở đây
3 tiêu chí quan trọng: Phần quyền, bảo mật và khả năng mở rộng
#### L2
Là các tích hợp của bên thứ 3 được sử dụng để tăng khả năng mở rộng và giao dịch
#### L3
Application with UI. Nơi người dùng thực tế tương tác.

### Salaries of JavaScript Developers in Top 8 Companies
#### Google 
Software Engineer: $156,806
Developer Relations Engineer: $154,545
Application Engineer: $199,805
#### eBay
Full-Stack Developer: $175,521
Software Engineer: $124,398
Front-End Software Engineer: $124,398
#### Facebook
Front-end Engineer: $172,114
Software Engineer: $187,046
Full-Stack Production Engineer: $166,290
#### Groupon
Software Engineering Manager: $180,106
Software Development Engineer: $139,671
Mobile Staff Engineer: $165,170
#### LinkedIn
Senior Software Engineer: $185,034
Staff Software Engineer: $222,075
Technical Services Manager: $126,069
#### Microsoft
Software Engineer: $136,877
Service Engineer: $140,386
Azure App Services Support Engineer: $74,904
#### Netflix
Senior UI Engineer: $276,987
Senior Front End Engineer: $138,643
Full-Stack Senior Software Engineer: $409,202
#### Paypal
Software Developer: $121,652
Full-Stack Software Engineer: $115,810
Full Stack Web Engineer: $132,773
#### Uber
Software Engineer: $159,263
Senior Software Engineer: $184,065
Front End Engineer: $159,263
[Ref1](https://careerkarma.com/blog/who-uses-javascript/)
[Ref2](https://insights.stackoverflow.com/survey/2021#top-paying-technologies-programming-scripting-and-markup-languages)

### Let Me Show You How to Get a Data Science Job Without Any Work Experience

### LAION release 5 billion Image-text - largest freely dataset - LAION5B
2.32 billion images with English text
2.26 billion with text from other languages
1.27 billion whose text language could not be determined unambiguously




