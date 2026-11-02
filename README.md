# ရွှေမြန်မာ POS & KDS (React + Vite + Tailwind CSS + PWA)

React.js, Tailwind CSS, Vite တို့ဖြင့် အဆင့်မြှင့်တင်ထားသော စားသောက်ဆိုင်သုံး POS စနစ်ဖြစ်ပါသည်။

## ✨ ပါဝင်သော စွမ်းဆောင်ရည်များ (Features)

1. **Modern Mobile-First UI & Bottom Navigation:**
   - ဖုန်းနှင့် တက်ဘလက်များတွင် အသုံးပြုရလွယ်ကူသော အောက်ခြေ Navigation Bar (စားပွဲများ၊ မှတ်တမ်း၊ မီနူး၊ ရောင်းအား၊ ဆက်တင်)
   - မှာယူထားသော စားပွဲအရေအတွက်ကို Badge ဖြင့် အချိန်နှင့်တစ်ပြေးညီ ဖော်ပြပေးခြင်း
2. **Custom PWA Install Banner:**
   - အင်တာနက်မလိုဘဲ Offline အသုံးပြုနိုင်ရန် `beforeinstallprompt` event ကို ဖမ်းယူပြီး လှပသော Install Drawer / Floating Banner ဖြင့် အသုံးပြုသူကို တိုက်တွန်းခြင်း
   - စက်ထဲသို့ တစ်ခါတည်း App အဖြစ် ထည့်သွင်းနိုင်ခြင်း
3. **စားပွဲစီမံခန့်ခွဲမှု (Table Management):**
   - စားပွဲတစ်ခုချင်းစီ၏ အော်ဒါအခြေအနေ (လွတ်/မလွတ်) နှင့် စုစုပေါင်း ကျသင့်ငွေကို တိုက်ရိုက်ကြည့်ရှုနိုင်ခြင်း
4. **Table Order Modal & Cart:**
   - ကဏ္ဍအလိုက် မီနူး filter ပြုလုပ်နိုင်ခြင်း
   - အော်ဒါ အရေအတွက် တိုး/လျှော့ ပြုလုပ်ခြင်း
5. **Dashboard Analytics:**
   - စုစုပေါင်း ရောင်းရငွေ၊ ဘောက်ချာအရေအတွက်၊ အရောင်းရဆုံးကဏ္ဍနှင့် ထိပ်တန်း အရောင်းရဆုံး ၅ မျိုး စာရင်း
6. **Thermal 58mm Printing & Web Bluetooth:**
   - ESC/POS Bluetooth Printer (58mm) နှင့် တိုက်ရိုက်ချိတ်ဆက် ပရင့်ထုတ်နိုင်ခြင်း
   - Browser CSS `@media print` ဖြင့် 58mm thermal စာရွက်ပေါ် သပ်ရပ်စွာ ပရင့်ထုတ်နိုင်ခြင်း
7. **4 Color Themes & Myanmar / English Language:**
   - Light, Dark, Warm, Green Theme များ ရွေးချယ်နိုင်ခြင်း
   - မြန်မာစာ (Padauk Font) နှင့် အင်္ဂလိပ်ဘာသာ အလွယ်တကူ ပြောင်းလဲနိုင်ခြင်း

---

## 🚀 စတင်အသုံးပြုပုံ (Quick Start)

### ၁။ လိုအပ်ချက်များ (Prerequisites)
- [Node.js](https://nodejs.org/) (Version 18 သို့မဟုတ် 20 အထက်)
- NPM သို့မဟုတ် Yarn သို့မဟုတ် PNPM

### ၂။ ပရောဂျက်ကို Run နည်း
```bash
# ၁။ Folder ထဲသို့ ဝင်ပါ
cd pos-vite-app

# ၂။ လိုအပ်သော Packages များကို သွင်းပါ
npm install

# ၃။ Development Server စတင်ပါ
npm run dev
```

Browser တွင် `http://localhost:3000` ဖြင့် ဖွင့်လှစ်အသုံးပြုနိုင်ပါပြီ။

### ၄။ Production Build ပြုလုပ်နည်း
```bash
npm run build
```
`dist/` folder ထွက်လာမည်ဖြစ်ပြီး ၎င်းကို Vercel, Netlify, Cloudflare Pages သို့မဟုတ် မည်သည့် Static Web Server ပေါ်တွင်မဆို တင်နိုင်ပါသည်။

---

## 📱 PWA & Web Bluetooth လိုအပ်ချက်များ
1. **HTTPS Connection:** PWA Service Worker နှင့် Web Bluetooth API တို့သည် `localhost` တွင် အလုပ်လုပ်သော်လည်း အင်တာနက်ပေါ်တင်ပါက မဖြစ်မနေ **HTTPS (SSL)** လိုအပ်ပါသည်။
2. **Bluetooth Printer Support:** Chrome, Edge, Brave စသော Chromium-based Browser များနှင့် Android/Desktop တွင် Web Bluetooth API အပြည့်အဝ အထောက်အပံ့ပေးပါသည်။
