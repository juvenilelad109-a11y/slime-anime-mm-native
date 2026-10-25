SLIME ANIME MM — Native Android starter
========================================
ဒီ Project က Kotlin မဟုတ်ဘဲ Java + Native Android UI + AndroidX Media3 ExoPlayer သုံးထားတဲ့ APK build starter ဖြစ်ပါတယ်။ APK ကို GitHub Actions နဲ့ အခမဲ့ build လုပ်နိုင်အောင် workflow ထည့်ထားပါတယ်။

လက်ရှိပါဝင်သည်
- Native Android UI
- Anime/episode search
- Media3 video player
- Android DownloadManager
- Demo clips ၂ ခု (anime မဟုတ်ပါ; player စမ်းသပ်ရန်သာ)
- GitHub Actions ကနေ debug APK build

အရေးကြီး
- ဒီ starter မှာ Admin login၊ Firebase online catalog၊ owner upload panel မပါသေးပါ။ အဲဒါတွေကို နောက်အဆင့်မှာ Firebase/API နဲ့ ချိတ်ရပါမယ်။
- MainActivity.java ထဲက seedEpisodes() ကို ကိုယ်ပိုင်/ဖြန့်ချိခွင့်ရှိသော direct video URLs ဖြင့် ပြောင်းပါ။
- Telegram post URL သို့မဟုတ် webpage URL ကို direct video URL အစား မသုံးပါနှင့်။
- Download ကို ခွင့်ပြုထားသော Video များအတွက်သာ အသုံးပြုပါ။
- Debug APK သည် စမ်းသပ်ရန်ဖြစ်ပြီး production release အတွက် signing key လိုအပ်နိုင်သည်။

အဆင့် ၁ — GitHub Repository
1. https://github.com/ ဝင်ပြီး New repository ဖန်တီးပါ။
2. Repository name: slime-anime-mm-native
3. ZIP ထဲကဖိုင်များအားလုံးကို repository root ထဲတင်ပါ။ .github folder အပါအဝင်ဖြစ်ရမည်။
4. main branch ထဲ commit လုပ်ပါ။

အဆင့် ၂ — APK Build
1. Repository ထဲက Actions tab ကိုဝင်ပါ။
2. "Build Slime Anime MM APK" workflow ကိုရွေးပါ။
3. Run workflow ကိုနှိပ်ပါ (သို့မဟုတ် main ထဲ push လုပ်ပြီး automatic build ကိုစောင့်ပါ)။
4. Workflow အောင်မြင်ရင် run တစ်ခုကိုဖွင့်ပါ။
5. Artifacts အောက်က Slime-Anime-MM-debug-apk ကို download လုပ်ပါ။
6. ZIP artifact ကို extract လုပ်ပြီး app-debug.apk ကို Android ဖုန်းမှာဖွင့်ပါ။
7. Install unknown apps permission ကို Android Settings မှာ ခွင့်ပြုပြီး Install လုပ်ပါ။

Code ပြင်ရန်
app/src/main/java/mm/slimeanime/app/MainActivity.java
seedEpisodes() method ထဲက Episode title နဲ့ URL များကို ပြင်ပါ။ Commit လုပ်ပြီး workflow ပြန် run ပါ။

Build requirements
- GitHub Actions JDK 17 + Gradle 8.9
- Android Gradle Plugin 8.7.3
- AndroidX Media3 1.5.1
