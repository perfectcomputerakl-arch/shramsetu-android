# ShramSetu Android APK Project

यह Android app आपके लाइव ShramSetu GitHub Pages वेबसाइट को ऐप के अंदर खोलता है।

Website URL:
https://perfectcomputerakl-arch.github.io/shramsetu/

## सबसे आसान तरीका: GitHub से APK बनवाएँ

1. इस ZIP को extract करें।
2. GitHub पर नया public या private repository बनाएँ, उदाहरण: `shramsetu-android`.
3. ZIP के अंदर की सभी फाइलें और `.github` फ़ोल्डर सहित repository के root में upload करें। ZIP फाइल को अकेले upload न करें।
4. ऊपर **Actions** टैब खोलें।
5. यदि GitHub workflow की अनुमति पूछे, तो उसे enable करें।
6. `Build ShramSetu APK` workflow खोलें और **Run workflow** दबाएँ। अगर push पर workflow अपने-आप चल चुका है, तो उसे पूरा होने दें।
7. हरा checkmark आने के बाद workflow run खोलें। नीचे **Artifacts** में `ShramSetu-debug-APK` डाउनलोड करें।
8. ZIP artifact को extract करें। उसमें `app-debug.apk` होगा।
9. APK अपने Android फोन में भेजें और install करें। फोन पूछे तो केवल अपने डाउनलोड किए APK के लिए install permission दें।

## Android Studio से बनाना

Android Studio में इस project folder को Open करें, Gradle sync पूरा होने दें, फिर **Build > Build Bundle(s) / APK(s) > Build APK(s)** चुनें।

## जरूरी बातें

- यह online WebView wrapper है; इंटरनेट के बिना वेबसाइट नहीं खुलेगी।
- वेबसाइट के मौजूदा front-end features ही ऐप में दिखेंगे। वास्तविक login, database, सुरक्षित user accounts और server-side job applications अलग से बनानी होंगी।
- यह debug APK है, जिसे परीक्षण के लिए बनाया जाता है। Play Store पर publish करने के लिए release signing और store requirements पूरी करनी होंगी।
- App website को `https://perfectcomputerakl-arch.github.io/shramsetu/` से लोड करता है। अगर GitHub Pages का URL बदले, तो `MainActivity.java` में `SITE_URL` अपडेट करें।
