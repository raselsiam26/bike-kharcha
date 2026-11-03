# Firebase সেটআপ (একবারের কাজ)

1. console.firebase.google.com → **Add project** (Analytics লাগবে না)।
2. **Build → Authentication → Get started** → Sign-in method-এ **Email/Password** চালু করো। চাইলে **Google**-ও চালু করো।
3. **Build → Firestore Database → Create database** (production mode, কাছের লোকেশন)।
4. Firestore-এর **Rules** ট্যাবে `firestore.rules` ফাইলের লেখাটা পেস্ট করে **Publish** করো। এতে প্রত্যেকে শুধু নিজের ডেটা দেখতে পাবে।
5. **Project settings → Your apps → Web (`</>`)** → অ্যাপ রেজিস্টার করো, যে `firebaseConfig` দেখাবে সেটা `firebase-config.js`-এ বসাও।
6. **Authentication → Settings → Authorized domains**-এ তোমার Vercel ডোমেইন (যেমন `bike-kharcha.vercel.app`) যোগ করো। `localhost` আগে থেকেই থাকে।
7. GitHub-এ কমিট করলে Vercel নিজে আপডেট করবে।

APK প্রজেক্টেও (`www/firebase-config.js`) একই কনফিগ বসাও। APK-তে Google লগইন বাটন লুকানো থাকে, ইমেইল/পাসওয়ার্ড চলবে।

*Firebase web apiKey গোপন কোনো চাবি নয়, ডেটার নিরাপত্তা আসে Firestore Rules থেকে।*
