# Pipe

```
ikibria@DESKTOP-OPJUB1R:~$ whoami
ikibria
ikibria@DESKTOP-OPJUB1R:~$ pwd
/home/ikibria
ikibria@DESKTOP-OPJUB1R:~$ cd /etc/
ikibria@DESKTOP-OPJUB1R:/etc$ ls -ltr
total 844
ikibria@DESKTOP-OPJUB1R:/etc$ ls -ltr | more
ikibria@DESKTOP-OPJUB1R:/etc$ ls -ltr | tail -1
```
```
ls -ltr | more কমান্ডটি ls -ltr কমান্ডের আউটপুটকে ধাপে ধাপে দেখাবে, যেখানে আপনি প্রতিটি পৃষ্ঠা শেষে স্পেসবার চাপলে পরবর্তী পৃষ্ঠা দেখতে পাবেন। আর ls -ltr | tail -1 কমান্ডটি ls -ltr কমান্ডের আউটপুটের শেষ এক লাইন দেখাবে।
```