### Vertical এবং Horizontal Scaling

#### Vertical Scaling

ভার্টিকাল স্কেলিং হল, একটি সার্ভারের রিসোর্স বৃদ্ধি করে স্কেল করা। এখানে রিসোর্স বলতে সার্ভারের Capacity(CPU/RAM/DISK) কে বুঝানো হয়েছে।

ভার্টিকাল স্কেলিং এর উদাহরণ হল MySQL.

<p align="center">
  <img src="./images/vertical-scaling.png" alt="Vertical Scaling">
</p>

#### Horizontal Scaling

হরাইজন্টাল স্কেলিং হল, নতুন সার্ভার যোগ করে স্কেল করা। সার্ভারের Capacity বৃদ্ধি করার পরিবর্তে নতুন সার্ভার যোগ করাই হল হরাইজন্টাল স্কেলিং।

হরাইজন্টাল স্কেলিং এর উদাহরণ হল Cassandra, MongoDB। AWS Lambda হরাইজন্টাল স্কেলিং করে থাকে।

<p align="center">
  <img src="./images/horizontal-scaling.png" alt="Horizontal Scaling">
</p>

Horizontal Scaling ব্যবহার করার সবচেয়ে বড় সুবিধা, <a href="../reliability/README.md" target="_blank">Fault Tolarance</a> and Availability.

Horizontal Scaling এর একটি সম্পূর্ণ উদাহরণ AWS Auto Scale. আপনার যদি একটি EC2 instance server থাকে এবং আপনার সার্ভার প্রচুর Request পেয়ে থাকে তখন AWS Auto Scale নতুন সার্ভার/instance তৈরি করে এবং Horizontal Scale ভিত্তিক কাজ করে।

Real world system এর কথা চিন্তা করলে Horizontal Scaling এরকম হয়,

<p align="center">
  <img src="./images/practical-horizontal-scaling.png" alt="Horizontal Scaling">
</p>

### কখন Scalability নিয়ে চিন্তা করবো?

যখন আপনি কোনো সিস্টেম তৈরী করবেন, তখন প্রথমে আপনার 0(zero) user থাকবে। অর্থাৎ Scalability কোনো issue না।

আপনি 0 user থাকার সময় Scalability(Vertical/Horizontal) নিয়ে কাজ করলে, আপনি এমন একটি problem নিয়ে কাজ করছেন যার কোনো অস্তিত্ব নাই।

Consistent মনিটরিং এর মাধ্যমে আপনি যখন দেখবেন user ট্রাফিক বৃদ্ধি পাচ্ছে তখন Scalability নিয়ে কাজ করা ভালো।
