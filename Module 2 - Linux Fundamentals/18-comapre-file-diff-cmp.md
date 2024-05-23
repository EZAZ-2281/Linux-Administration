# diff cmp

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch superman1
ikibria@DESKTOP-OPJUB1R:~$ echo "abdur rahim" > superman1
ikibria@DESKTOP-OPJUB1R:~$ echo "jakaria ahmed" >> superman1
ikibria@DESKTOP-OPJUB1R:~$ echo "makil ahmed" >> superman1
ikibria@DESKTOP-OPJUB1R:~$ cat superman1
abdur rahim
jakaria ahmed
makil ahmed
```
```
ikibria@DESKTOP-OPJUB1R:~$ touch superman2
ikibria@DESKTOP-OPJUB1R:~$ echo "rahim ahmed" > superman2
ikibria@DESKTOP-OPJUB1R:~$ echo "abdur rahman" >> superman2
ikibria@DESKTOP-OPJUB1R:~$ cat superman2
rahim ahmed
abdur rahman
```
```
ikibria@DESKTOP-OPJUB1R:~$ diff superman1 superman2
1,3c1,2
< abdur rahim
< jakaria ahmed
< makil ahmed
---
> rahim ahmed
> abdur rahman
```
```
ikibria@DESKTOP-OPJUB1R:~$ cmp superman1 superman2
superman1 superman2 differ: byte 1, line 1
ikibria@DESKTOP-OPJUB1R:~$ exit
```
## diff
এখানে diff কমান্ডের আউটপুট কী বোঝাচ্ছে তা বিশ্লেষণ করা হলো:
1,3c1,2: এই লাইনটি বোঝায় যে superman1 ফাইলের ১ থেকে ৩ নম্বর লাইনগুলো superman2 ফাইলের ১ থেকে ২ নম্বর লাইনগুলোর সাথে পরিবর্তিত হয়েছে।
- < চিহ্নের পরে থাকা লাইনগুলো superman1 ফাইলের কন্টেন্টকে বোঝাচ্ছে।
- '>' চিহ্নের পরে থাকা লাইনগুলো superman2 ফাইলের কন্টেন্টকে বোঝাচ্ছে।
- --- চিহ্নটি superman1 এবং superman2 ফাইলের মধ্যে বিভাজক হিসেবে কাজ করছে।

বিস্তারিত ব্যাখ্যা
superman1 ফাইলে প্রথম তিনটি লাইন ছিল:
abdur rahim  
jakaria ahmed  
makil ahmed  
superman2 ফাইলে প্রথম দুটি লাইন ছিল:  
rahim ahmed  
abdur rahman

পার্থক্য:
superman1 ফাইলের abdur rahim পরিবর্তিত হয়ে superman2 ফাইলে rahim ahmed হয়েছে।
superman1 ফাইলের jakaria ahmed এবং makil ahmed পরিবর্তিত হয়ে superman2 ফাইলে abdur rahman হয়েছে।

## cmp
cmp কমান্ডটি ব্যবহার করে দুইটি ফাইলের মধ্যে প্রথম যে অবস্থানে তারা ভিন্ন তা দেখায়। নিচে cmp কমান্ডের আউটপুটটি বিশ্লেষণ করা হলো:

ikibria@DESKTOP-OPJUB1R:~$ cmp superman1 superman2  
superman1 superman2 differ: byte 1, line 1

ব্যাখ্যা:
cmp কমান্ডটি দেখাচ্ছে যে superman1 এবং superman2 ফাইলগুলো ভিন্ন। তাদের পার্থক্য প্রথম বাইটেই।  
- byte 1, line 1: এই অংশটি বোঝাচ্ছে যে ভিন্নতা প্রথম বাইট এবং প্রথম লাইনে আছে।  
অর্থাৎ, superman1 এবং superman2 ফাইলের প্রথম বাইট এবং প্রথম লাইন থেকেই তারা আলাদা।

বিস্তারিত ব্যাখ্যা:  
প্রথম বাইটেই ভিন্নতা থাকায়, cmp কমান্ডটি দেখাচ্ছে যে প্রথম বাইট থেকেই দুইটি ফাইলের কন্টেন্ট আলাদা।
এই ভিন্নতার কারণে, cmp কমান্ডটি আর আগের দিকে যাচ্ছেনা এবং সাথে সাথে পার্থক্যটি জানিয়ে দিচ্ছে।  
উদাহরণ:  
ধরা যাক superman1 ফাইলে প্রথম লাইন ছিল:  
abdur rahim  
এবং superman2 ফাইলে প্রথম লাইন ছিল:  
rahim ahmed  
তাহলে, প্রথম বাইট থেকেই তারা ভিন্ন হবে, কারণ superman1 ফাইলে প্রথম অক্ষর a এবং superman2 ফাইলে প্রথম অক্ষর r।
এইভাবে, cmp কমান্ডটি ব্যবহারের মাধ্যমে আপনি দ্রুত জানতে পারবেন যে দুটি ফাইলের কোন অবস্থান থেকে তারা ভিন্ন।

**[The End]**