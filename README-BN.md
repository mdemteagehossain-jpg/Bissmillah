# Bismillah Craft & Studio — Android APK

## নীল Capacitor আইকনের বদলে BCS লোগো বসাতে

1. ZIP ফাইলটি extract করুন।
2. GitHub repository-র মূল (root) ফোল্ডারে থাকা ফাইলগুলোর সঙ্গে এই ZIP-এর ফাইলগুলো আপলোড/replace করুন। বিশেষ করে `.github/workflows/build-apk.yml` অবশ্যই replace করবেন এবং `assets`-এর সব PNG ফাইল আপলোড করবেন।
3. GitHub-এ **Actions → Build Android APK → Run workflow** চাপুন, অথবা `main` branch-এ commit করুন।
4. Run-এর মধ্যে **Generate Android app icons from BCS logo** ধাপটি সবুজ হয়েছে কি না দেখুন। এরপর **Build debug APK** ও **Upload APK artifact** সফল হলে artifact থেকে APK নামান।
5. পুরোনো অ্যাপ সরিয়ে নতুন APK install করে দেখুন। একই অ্যাপের ডেটা দরকার হলে uninstall করার আগে backup নিন।

এই প্যাকেটে `icon-only.png`, `icon-foreground.png`, `icon-background.png` এবং বড় `splash.png` আছে; এগুলো থেকে workflow-তে Android launcher icon generate হবে।


## নতুন আপডেট
- “প্লে স্টোর অ্যাপ নাম ও লোগো” সেটিংস অপশন সরানো হয়েছে।
- লগইন স্ক্রিন থেকে ডিফল্ট পাসওয়ার্ডের লেখা সরানো হয়েছে।
- অ্যাডমিন মেনুতে পাসওয়ার্ড পরিবর্তনের অপশন যোগ হয়েছে।
- শপের নাম আলাদা `shop_title_name` হিসেবে localStorage এবং IndexedDB-তে সেভ হয়, তাই অ্যাপ বন্ধ করে আবার খুললেও নাম থাকার কথা।

প্রথমবার পাসওয়ার্ড আগের মতো `1234`; নিরাপত্তার জন্য লগইন করে সেটি বদলে নিন। পাসওয়ার্ডটি এই ডিভাইসের অ্যাপের local storage/IndexedDB-তে রাখা হয়; এটি সার্ভার-ভিত্তিক নিরাপত্তা নয়।

## নতুন UI আপডেট
- অ্যাপ খোলার সময় BCS লোগোর fade/zoom ও float অ্যানিমেশন এবং Handmade • Custom Design • With Love ট্যাগলাইন।
- হোমপেজের কভার/ব্যানার আগের চেয়ে বড়।
- ভিউয়ার ও অ্যাডমিন প্রোডাক্ট ছবির জন্য ১:১ স্কয়ার অনুপাত।
- প্রোডাক্ট ছবিতে ট্যাপ করলে বড় ছবি দেখার ভিউয়ার; ছবিতে আবার ট্যাপ করলে জুম, বাইরে ট্যাপ বা ×/Escape দিয়ে বন্ধ।
