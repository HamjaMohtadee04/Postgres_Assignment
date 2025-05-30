"# Postgres_Assignment" 
## Q1: PostgreSQL কী?

DBMS বা ডাটাবেইজ ম্যানেজম্যান্ট সিস্টেম হচ্ছে একেকটা সফটওয়্যার যেগুলো দিয়ে বিভিন্ন ধরনের ডাটাবেইজ তৈরি এবং সেগুলো মেইনটেনেন্স করা হয়। যেগুলো আমরা পিসি তে ইনস্টল করে একেকটা ডাটাবেইজ সার্ভার তৈরি করতে পারি। জনপ্রিয় ডাটাবেইজ যেমন- MySQL, Oracle, PostgreSQL,Microsoft SQL, NoSQL এর মাঝে PostgreSQL অত্যন্ত জনপ্রিয়।  
PostgreSQL হচ্ছে রিলেশনাল ডাটাবেইজ ম্যানেজম্যান্ট সিস্টেম সফটওয়্যার যার দ্বারা আমরা ডাটাবেইজ এর বিভিন্ন ধরনের রিলেশন গুলো স্ট্রাকচারাল কুয়েরি ল্যাংগুয়েজ (SQL) দিয়ে করতে পারি বা ডাটাবেইজ এর সাথে কমিউনিকেট করতে পারি। PostgreSQL কে বলা হয় বর্তমান পৃথিবীর সবচেয়ে এডভান্সড ওপেন সোর্স রিলেশনাল ডাটাবেইজ ম্যানেজম্যান্ট সিস্টেম। 

### কেনো PostgreSQL?

- ওপেন সোর্স - ইন্টারন্যাশনাল কমিউনিটি এর ডেভেলপাররা PostgreSQL কে সাপোর্ট, এর আপডেট, কন্ট্রিবিউট এবং এর যদি কোনো বাগ আসে তা ফিক্সড প্রতিনিয়ত করতেছে। যার জন্য ইউজার দের যে কোনো সাপোর্ট সহজেই পাওয়া যায়। রোভাস্ট এবং এডভান্সড ফিচার প্রতিনিয়ত ডেভেলপাররা বিল্ড করতেছে।
- রিলেশনাল ডাটাবেইজ ম্যানেজম্যান্ট সিস্টেম - PostgreSQL রিলেশনাল ডাটাবেইজ ম্যানেজম্যান্ট সিস্টেম সফটওয়্যার হওয়াতে খুব সহজেই রিলেশনাল মডেল গুলো খুব সহজেই ইমপ্লিমেন্ট করা যায়।
- মর্ডান & এডভান্সড - মর্ডান এবং এডভান্সড ডাটা টাইপস,  ACID কমপাইলেন্স সাপোর্ট করে।
- স্কেলাভিলিটি - PostgreSQL হরিজন্টাল এবং ভার্টিকাল স্কেলাভল।  যার জন্য লার্জ স্কেল এর এপ্লিকেশনের ডাটাবেইজ খুব সহজেই বিল্ড করা যায়।
- ইন্ডেক্সিং - হ্যাস, বি-ট্রি, বিটম্যাপ ইত্যাদি এডভান্সড ইনডেক্সিং ট্যাকনিক সাপোর্ট করে।
- কমিউনিটি সাপোর্ট - PostgreSQL এর রয়েছে অত্যন্ত বড় কমিউনিটি।  যার জন্য খুব সহজেই যে কোনো ধরনের সমস্যার সাপোর্ট দ্রুত পাওয়া যায়

PostgreSQL খুব সহজেই আয়ত্ত করা যায় এবং এর এডভান্সড কুয়েরি ট্যাকনিক এর জন্য বর্তমানে ডেভেলপার দের অন্যতম ফ্যাবারিট রিলেশনাল ডাটাবেইজ ম্যানেজম্যান্ট সিস্টেম হচ্ছে PostgreSQL । 

---

## Q2: PostgreSQL-এ  ডেটাবেইজ স্কিমার উদ্দেশ্য কী?

Schema হলো PostgreSQL-এর একটি লজিকাল স্ট্রাকচার। যেটা একটি ডেটাবেইজের ভিতরে objects (যেমন: tables, views, indexes, functions ইত্যাদি) কে গ্রুপ করে রাখে। Schema ব্যবহারের মূল কারণ হচ্ছে ডেটাবেইসকে সুশৃঙ্খলভাবে সাজানো এবং নাম বা নেমস্পেসের কনফ্লিক্ট এড়ানো। বড় ডেটাবেইজের প্রজেক্টে টেবিল এর সংখ্যা অনেক বেশি হতে পারে। তখন schema ব্যবহার করলে কাজ ভাগ করে রাখা যায় এবং বুঝতে সুবিধা হয় কে কোন অংশের দায়িত্বে।

### Schema এর ব্যবহার -

- একই ডেটাবেইসে একই নামের টেবিল রাখা যায় | যদি টেবিলগুলো আলাদা স্কিমায় থাকে।
- ইউজার পারমিশন আলাদা ভাবে কনফিগার করা যায় স্কিমা অনুযায়ী।
- মডিউল বা ফিচার অনুযায়ী ডেটাবেইস অংশগুলো ভাগ করা যায়।  
  PostgreSQL-এ আমরা schema অনুযায়ী user permission সেট করতে পারি।

**Example** :  
ধরা যাক, একটি ecommerce project তৈরি করা হয়েছে। এক স্কিমায় রয়েছে “admin” টেবিল, আরেক স্কিমায় রয়েছে “user”  টেবিল। উভয় স্কিমায় যদি “login” নামে টেবিল থাকে, তবুও কোনো সমস্যা হবে না, কারণ স্কিমাগুলো আলাদা। আবার যদি ইউজারকে শুধু “admin” স্কিমায় কাজ করতে দেওয়া হয়, তাহলে সে অন্য স্কিমায় কোনো table access করতে পারবে না।

---

## Q3: VARCHAR এবং CHAR ডেটা টাইপের মধ্যে পার্থক্য কী?

**CHAR**:  CHAR হচ্ছে fixed-length ক্যারেক্টার টাইপ। এর মানে, যদি CHAR(10) বলা হয় তাহলে ১০টি CHAR বা স্ট্রিং রাখা যাবে। কিন্তু, CHAR ডাটা টাইপে CHAR(10) বলার পর যদি ৫-ক্যারেক্টার বা ৫ টি স্ট্রিং রাখা হয় তাহলে বাকি CHAR(5) বা ৫ টি স্ট্রিং এর মেমোরির জায়গা “space” দিয়ে এলোকেট হয়ে যায়।

**VARCHAR**: VARCHAR হচ্ছে variable-length ক্যারেক্টার টাইপ। এখানে চাইলে fixed-length ক্যারেক্টার ডাটা টাইপ ব্যবহার করতে পারি। কিন্তু তবুও আচরন করবে variable-length টাইপ এর মতো। যদি VARCHAR(10) বলা হয় তাহলে তা ১০ টি স্ট্রিং এর চাইতে বেশি নিবে না। তবে, যদি ৫টি স্ট্রিং বা ৫-টি ক্যারেক্টার রাখা হয় তাহলে তা বাকি ৫-টি স্ট্রিং এর জায়গা “space” দিয়ে এলোকেট করবে না CHAR ডাটা টাইপ এর মতো। 

যার জন্য VARCHAR ডাটা টাইপ ব্যবহার করার সুবিধা CHAR ডাটা টাইপ ব্যবহার করার চেয়ে বেশি।

**Example:**  
```
CHAR(8) → "HAMJA "  
VARCHAR(8) → "HAMJA"    [VARCHAR ব্যবহার করাটা ভালো কারণ space waste হয় না।]
```
## Q4: PostgreSQL-এ Primary Key এবং Foreign Key কী?
***Primary Key:**
Primary Key হলো এমন একটি কলাম বা কলামের কম্বিনেশন, যা ডাটাবেইজ এর একটি টেবিলের প্রতিটি রেকর্ডকে ইউনিকভাবে চিহ্নিত করে। এটি কোনোভাবেই null বা duplicate হতে পারে না। প্রতিটি টেবিলে একটিমাত্র Primary Key থাকতে পারে এবং এর মাধ্যমে ডেটার ভিন্নতা ও ইউনিকনেস বজায় রাখা হয়। Primary Key ব্যবহার করে একটি ডেটাবেজ এ বুঝতে পারে যায় কোন রেকর্ডটি কাকে ইউনিকলি আইডেনটিফাই করে।

***Foreign Key:**
Foreign Key হলো এমন একটি কলাম যা অন্য একটি টেবিলের Primary Key-এর সাথে সম্পর্ক তৈরি করে। এটি দুটি টেবিলের মধ্যে সংযোগ (relationship) স্থাপন করে এবং ডেটার ইন্টিগ্রিটি বজায় রাখে। অর্থাৎ, Foreign Key টেবিলের কোনো মান যেন অন্য টেবিলের নির্দিষ্ট ভ্যালুর সঙ্গে মিলে, সেটা নিশ্চিত করে। Foreign Key-এর মান অবশ্যই ঐ টেবিলে থাকা Primary Key-এর কোনো একটি ভ্যালুর সাথে ম্যাচ করতে হবে, অথবা NULL হতে পারে এবং একাধিক Foreign Key একই টেবিলে থাকতে পারে।
***Example:**

```
-- departments table
CREATE TABLE departments (
  dept_id SERIAL PRIMARY KEY,       -- Primary Key
  dept_name TEXT NOT NULL
);

-- employees table
CREATE TABLE employees (
  emp_id SERIAL PRIMARY KEY,        -- Primary Key
  name TEXT NOT NULL,
  dept_id INTEGER,                  -- Foreign Key
  FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);
```

## Q5: SELECT স্টেটমেন্টে WHERE ক্লজের কাজ কী?
PostgresSQL এর অন্যতম এবং সবচেয়ে বেশি ব্যবহার করা হয় SELECT স্টেটমেন্ট। বিভিন্ন ধরনের এবং বড় ডাটাবেইজ থেকে এই স্টেটমেন্ট ব্যবহার করে খুব সহজেই ডাটা ফিল্টার করে নির্দিষ্ট ডাটা আনা যায়। আর এই কাজটাই ডেভেলপাররা করে থাকেন WHERE ক্লজ SELECT স্টেটমেন্টে ব্যবহারের দ্বারা। WHERE ক্লজ একটি SQL স্টেটমেন্টে ব্যবহার করা হয় নির্দিষ্ট শর্ত অনুযায়ী ডেটা ফিল্টার করতে। যখন কোনো টেবিল থেকে ডেটা SELECT করতে হয়, তখন WHERE ক্লজ ব্যবহার করে শর্ত দেওয়া যায়। যার মাধ্যমে শুধু সেইসব রেকর্ড দেখানো হয় যেগুলো সেই শর্ত পূরণ করে। এটি খুবই প্রয়োজনীয়, যখন টেবিল বড় হয় এবং সব ডেটা না দেখিয়ে নির্দিষ্ট ডেটা দেখতে হয়। এছাড়াও WHERE ক্লজের মাধ্যমে বিভিন্ন কন্ডিশনাল (AND, OR, LIKE, IN) ইত্যাদি অপারেটর ব্যবহার করে আরও নির্ভুলভাবে ডেটা খোঁজা যায়। এটি অনেক গুরুত্বপূর্ণ, কারণ অনেক সময় ডেটাবেজে হাজার হাজার রেকর্ড থাকতে পারে। তখন পুরো টেবিল দেখতে সময় ও রিসোর্স নষ্ট হয়।

***Example:**
```
SELECT * FROM students
WHERE roll = 5;

SELECT name, marks FROM students
WHERE marks > 50;

SELECT * FROM  students
WHERE course = ‘CSE’  AND marks >80 ;

SELECT * FROM students
WHERE class = '10' OR class = '12';
```