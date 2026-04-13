<!-- LANGUAGE TOGGLE -->
<div align="center">

<a href="#arabic-section">
  <img src="https://img.shields.io/badge/🇦🇪_العربية-اقرأ_بالعربي-green?style=for-the-badge" alt="Arabic"/>
</a>
&nbsp;&nbsp;
<a href="#english-section">
  <img src="https://img.shields.io/badge/🇬🇧_English-Read_in_English-blue?style=for-the-badge" alt="English"/>
</a>

</div>

---

<!-- SHIELDS -->
<div align="center">

[![YouTube Tutorial](https://img.shields.io/badge/📺_YouTube-Watch_Tutorial-FF0000?style=for-the-badge&logo=youtube)](https://youtu.be/gFt1yf1-ukU?si=ZFLewzqIddB9sO4T)
[![n8n Workflow](https://img.shields.io/badge/n8n-Download_Workflow-EA4B71?style=for-the-badge&logo=n8n)](https://n8n.io)
[![Meta WhatsApp API](https://img.shields.io/badge/Meta-WhatsApp_Business_API-25D366?style=for-the-badge&logo=whatsapp)](https://developers.facebook.com/docs/whatsapp)
[![Groq AI](https://img.shields.io/badge/Groq-LLaMA_3.3_70B-F55036?style=for-the-badge)](https://console.groq.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Free](https://img.shields.io/badge/Cost-100%25_Free-brightgreen?style=for-the-badge)](https://github.com/YousefAutomates/whatsapp-api-free-n8n-automation)

</div>

---

<!-- ENGLISH SECTION -->
<a id="english-section"></a>

<div align="center">

# 🤖 Free WhatsApp API from Meta + n8n AI Automation
### Complete Guide — From Zero to a Working WhatsApp Chatbot | 2026

> **Get a free official WhatsApp Business API test number from Meta and build a full AI chatbot using n8n — step by step, completely free.**

</div>

---

## 📺 Tutorial Video

<div align="center">

[![Watch the Full Tutorial](https://img.shields.io/badge/▶_Watch_Full_Tutorial_on_YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/gFt1yf1-ukU?si=ZFLewzqIddB9sO4T)

**إزاي تاخد WhatsApp API مجاني من Meta وتجرب عليه الأتمتة | شرح كامل 2026**

</div>

---

## 🎯 What This Project Is About

This project shows you how to:

- ✅ Get a **free official WhatsApp Business API** test number from Meta
- ✅ Set up **Meta for Developers** and configure Webhooks correctly
- ✅ Build a **complete AI chatbot** using n8n + Groq (LLaMA 3.3 70B)
- ✅ Generate a **permanent Access Token** that never expires
- ✅ Handle **message filtering** to avoid responding to status updates
- ✅ Maintain **conversation memory** per customer phone number

> **Note:** This uses a **Test Number**, not a Production number.
> A test number works with up to 5 verified phone numbers — perfect for testing your automation before going live.

---

## ⚡ Tech Stack — All Free

| Tool | Purpose | Cost |
|------|---------|------|
| **Meta WhatsApp Business API** | Send & receive WhatsApp messages | 🆓 Free (test number) |
| **n8n** | Workflow automation platform | 🆓 Free (self-hosted or cloud trial) |
| **Groq API** | AI inference engine | 🆓 Free tier |
| **LLaMA 3.3 70B** | Large language model | 🆓 Free via Groq |

---

## 📁 Repository Structure

```
whatsapp-api-free-n8n-automation/
│
├── 📂 workflows/
│   ├── 🤖 main-whatsapp-ai-agent.json        ← Main AI chatbot workflow
│   └── 🔗 meta-webhook-verifier.json         ← Webhook verification workflow
│
├── 📂 docs/                                   ← Documentation (coming soon)
├── 📂 assets/                                 ← Screenshots & diagrams
│
├── 📄 .gitignore                              ← Protects sensitive credentials
├── 📄 LICENSE                                 ← MIT License
├── 📄 CONTRIBUTING.md                         ← Contribution guidelines
├── 📄 SECURITY.md                             ← Security best practices
└── 📄 README.md                               ← You are here
```

---

## 📥 Download Workflows

| Workflow | Description | Download |
|----------|-------------|---------|
| **Main AI Agent** | Full WhatsApp chatbot with AI | [⬇️ Download](https://raw.githubusercontent.com/YousefAutomates/whatsapp-api-free-n8n-automation/main/workflows/main-whatsapp-ai-agent.json) |
| **Webhook Verifier** | Meta webhook verification | [⬇️ Download](https://raw.githubusercontent.com/YousefAutomates/whatsapp-api-free-n8n-automation/main/workflows/meta-webhook-verifier.json) |

> **How to import into n8n:**
> n8n → Workflows → Import from File → Select the `.json` file

---

## 🗺️ How It Works

```
Customer sends WhatsApp message
           │
           ▼
    WhatsApp Trigger (n8n)
           │
           ▼
    IF Node — Is it a text message?
     │                    │
    YES                   NO
     │                    │
     ▼                  STOP
  AI Agent             (ignore delivery
  (Groq LLaMA)          receipts, etc.)
     │
     ▼
  Send WhatsApp Reply
```

### Why the IF Filter?
When Meta sends a WhatsApp message to your webhook, it actually sends **3 separate events**:
1. The actual message
2. A "delivered" status update
3. A "read" status update

Without the filter, your AI would respond **3 times** to every message!

---

## 🚀 Setup Guide

### Step 1 — Meta Developer Account

1. Go to [developers.facebook.com](https://developers.facebook.com)
2. Create account → **My Apps** → **Create App**
3. Choose: **Business** type
4. Add **WhatsApp** product to your app
5. Select or create a **Business Portfolio**

### Step 2 — Get Free Test Number

1. Go to: **App → WhatsApp → Getting Started**
2. Meta gives you a **free US test number** (starts with +1 555...)
3. Add your personal number to the allowlist (up to 5 numbers)
4. Verify with the code sent to your WhatsApp
5. Copy your **Phone Number ID**

### Step 3 — Configure Webhook (Meta Verification)

> ⚠️ **Do this BEFORE activating the main workflow!**

1. Import `meta-webhook-verifier.json` into n8n
2. **Activate** the workflow (turn it ON)
3. Copy the **Production Webhook URL** from the Webhook node
4. Go to: **Meta App → WhatsApp → Configuration → Webhook**
5. Paste the URL as **Callback URL**
6. Set any text as **Verify Token** (remember it!)
7. Click **Verify and Save** ✅

### Step 4 — Generate Permanent Access Token

> The temporary token expires every 24 hours — use a permanent one!

1. Go to [business.facebook.com](https://business.facebook.com)
2. **Settings → Users → System Users → Add**
3. Name it anything, set role to **Admin**
4. **Assign Assets** → Add your WhatsApp account → Full Control
5. **Generate Token** → Select your App → Set expiry to **Never**
6. ✅ Copy and save this token securely!

### Step 5 — n8n Credentials Setup

Add these credentials in n8n:

**WhatsApp Trigger API:**
- Client ID → App ID (from Meta App Settings → Basic)
- Client Secret → App Secret (from Meta App Settings → Basic)

**WhatsApp API (Send):**
- Access Token → Your permanent System User Token
- Business Account ID → Your WABA ID (from Meta Dashboard)

**Groq API:**
- API Key → From [console.groq.com](https://console.groq.com) (free)

### Step 6 — Import & Configure Main Workflow

1. Import `main-whatsapp-ai-agent.json` into n8n
2. Update **Phone Number ID** in the "Send WhatsApp Reply" node
3. Customize the **System Prompt** in the AI Agent node
4. **Activate** the workflow
5. Send a test message from your registered number ✅

---

## ⚠️ Test Number vs Production — Key Differences

| Feature | Test Number | Production Number |
|---------|-------------|------------------|
| Cost | 🆓 Free | 💳 Paid per message |
| Recipient limit | 5 numbers only | Unlimited |
| Number type | Meta's US number | Your own number |
| Verification badge | ❌ No | ✅ Green tick possible |
| Business verification | ❌ Not required | ✅ Required |
| Templates required | ❌ No | ✅ Yes (to start conversation) |
| Best for | Testing automation | Real business use |

---

## 🔒 Important Security Notes

- ❌ **Never commit** Access Tokens to GitHub
- ❌ **Never commit** App Secrets
- ✅ Store all secrets in **n8n Credentials** (encrypted)
- ✅ Use **System User Tokens** (never expire) for production
- ✅ Read [SECURITY.md](SECURITY.md) before deploying

---

## 🐛 Common Issues & Solutions

<details>
<summary><b>❌ Error 131030 — Recipient not in allowlist</b></summary>

**Cause:** In test mode, you can only send to numbers you've verified.

**Fix:**
1. Go to Meta Dashboard → WhatsApp → Getting Started
2. Add the recipient number in the "To" field
3. Send verification code and confirm
</details>

<details>
<summary><b>❌ Error 190 — Invalid OAuth access token</b></summary>

**Cause:** Using an expired temporary token.

**Fix:** Generate a permanent System User Token (see Step 4 above).
</details>

<details>
<summary><b>❌ Webhook verification failed</b></summary>

**Cause:** Verify Token mismatch or webhook not active.

**Fix:**
1. Make sure the `meta-webhook-verifier` workflow is **Active**
2. Check the Verify Token matches exactly (no extra spaces)
3. Confirm the webhook URL is the **Production URL**, not Test URL
</details>

<details>
<summary><b>❌ AI responds multiple times to one message</b></summary>

**Cause:** Missing the IF filter node.

**Fix:** Make sure the IF node is connected and checks for `messages[0].text.body` existence.
</details>

---

## 🌐 Professional Automation Services

<div align="center">

**Looking for custom automation solutions for your business?**

I provide professional automation services including WhatsApp bots, AI agents, CRM integrations, and full workflow automation.

[![Visit Portfolio](https://img.shields.io/badge/🌐_Visit_Portfolio-yousefautomates.pages.dev-blue?style=for-the-badge)](https://yousefautomates.pages.dev/)

**م. يوسف الشربيني | Eng. Yousef Elsherbiny**
Automation Services | n8n | AI Agents | WhatsApp Bots

</div>

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — free to use, modify, and distribute.

---

<!-- ARABIC SECTION -->
<a id="arabic-section"></a>

---

<div align="center">

# 🤖 WhatsApp API مجاني من Meta + أتمتة بالذكاء الاصطناعي عبر n8n
### شرح كامل — من الصفر لبوت واتساب شغّال بالكامل | 2025/2026

> **احصل على رقم اختبار مجاني رسمي من Meta وابنِ بوت واتساب بالذكاء الاصطناعي باستخدام n8n — خطوة بخطوة، مجاناً تماماً.**

</div>

---

## 📺 الفيديو التعليمي

<div align="center">

[![شاهد الشرح الكامل على يوتيوب](https://img.shields.io/badge/▶_شاهد_الشرح_الكامل_على_يوتيوب-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/gFt1yf1-ukU?si=ZFLewzqIddB9sO4T)

**إزاي تاخد WhatsApp API مجاني من Meta وتجرب عليه الأتمتة | شرح كامل 2026**

</div>

---

## 🎯 هدف المشروع

هدف الفيديو والمشروع ده إنك تعرف:

- ✅ إزاي تحصل على **WhatsApp Business API مجاني ورسمي** من Meta كـ Test Number
- ✅ إزاي تعمل إعداد **Meta for Developers** وتضبط الـ Webhook صح
- ✅ إزاي تبني **بوت ذكاء اصطناعي كامل** باستخدام n8n و Groq (LLaMA 3.3 70B)
- ✅ إزاي تولد **Access Token دائم** ما ينتهيش
- ✅ إزاي تعمل **فلتر للرسائل** عشان البوت ما يردش على تحديثات الحالة
- ✅ إزاي تحافظ على **ذاكرة المحادثة** لكل عميل بشكل منفصل

> **ملاحظة مهمة:** ده بيستخدم **Test Number** مش Production.
> الـ Test Number بيشتغل مع 5 أرقام بحد أقصى — كافي تماماً لاختبار أتمتتك قبل ما تطلق للعملاء الحقيقيين.

---

## ⚡ الأدوات المستخدمة — كلها مجانية

| الأداة | الاستخدام | التكلفة |
|--------|-----------|---------|
| **Meta WhatsApp Business API** | إرسال واستقبال رسائل الواتساب | 🆓 مجاني (Test Number) |
| **n8n** | منصة الأتمتة | 🆓 مجاني (Self-hosted أو Cloud Trial) |
| **Groq API** | محرك الذكاء الاصطناعي | 🆓 مجاني |
| **LLaMA 3.3 70B** | نموذج اللغة الكبير | 🆓 مجاني عبر Groq |

---

## 📁 هيكل الملفات

```
whatsapp-api-free-n8n-automation/
│
├── 📂 workflows/
│   ├── 🤖 main-whatsapp-ai-agent.json        ← الوركفلو الرئيسي (البوت الذكي)
│   └── 🔗 meta-webhook-verifier.json         ← وركفلو التحقق من الـ Webhook
│
├── 📂 docs/                                   ← التوثيق (قريباً)
├── 📂 assets/                                 ← الصور والمخططات
│
├── 📄 .gitignore                              ← حماية الـ Credentials
├── 📄 LICENSE                                 ← رخصة MIT
├── 📄 CONTRIBUTING.md                         ← دليل المساهمة
├── 📄 SECURITY.md                             ← سياسة الأمان
└── 📄 README.md                               ← أنت هنا
```

---

## 📥 تحميل الوركفلو

| الوركفلو | الوصف | التحميل |
|----------|-------|---------|
| **البوت الرئيسي** | بوت الواتساب الذكي الكامل | [⬇️ تحميل](https://raw.githubusercontent.com/YousefAutomates/whatsapp-api-free-n8n-automation/main/workflows/main-whatsapp-ai-agent.json) |
| **Webhook Verifier** | التحقق من webhook الميتا | [⬇️ تحميل](https://raw.githubusercontent.com/YousefAutomates/whatsapp-api-free-n8n-automation/main/workflows/meta-webhook-verifier.json) |

> **طريقة الاستيراد في n8n:**
> n8n → Workflows → Import from File → اختار ملف الـ `.json`

---

## 🗺️ كيف يعمل النظام

```
العميل يبعت رسالة واتساب
           │
           ▼
    WhatsApp Trigger (n8n)
           │
           ▼
    IF Node — هل هي رسالة نصية؟
     │                    │
    نعم                   لا
     │                    │
     ▼                  وقف
  AI Agent             (تجاهل إشعارات
  (Groq LLaMA)          التسليم والقراءة)
     │
     ▼
  إرسال الرد على الواتساب
```

### ليه محتاجين الـ IF Filter؟
لما Meta بتبعت رسالة واتساب للـ Webhook بتاعك، بتبعت في الواقع **3 Events منفصلة**:
1. الرسالة الفعلية
2. تحديث "تم التسليم"
3. تحديث "تمت القراءة"

من غير الفلتر، البوت هيرد **3 مرات** على كل رسالة!

---

## 🚀 خطوات الإعداد

### الخطوة 1 — حساب Meta Developer

1. روح على [developers.facebook.com](https://developers.facebook.com)
2. أنشئ حساب → **My Apps** → **Create App**
3. اختار نوع: **Business**
4. أضف منتج **WhatsApp** للـ App بتاعك
5. اختار أو أنشئ **Business Portfolio**

### الخطوة 2 — الحصول على Test Number مجاني

1. روح على: **App → WhatsApp → Getting Started**
2. Meta هتديك **رقم أمريكي تجريبي مجاني** (بيبدأ بـ +1 555...)
3. أضف رقمك الشخصي للـ Allowlist (حد أقصى 5 أرقام)
4. تحقق بالكود اللي هييجيلك على الواتساب
5. انسخ الـ **Phone Number ID** بتاعك

### الخطوة 3 — إعداد الـ Webhook (التحقق من Meta)

> ⚠️ **اعمل ده قبل تفعيل الوركفلو الرئيسي!**

1. استورد `meta-webhook-verifier.json` في n8n
2. **فعّل** الوركفلو (شغّله)
3. انسخ **Production Webhook URL** من الـ Webhook Node
4. روح على: **Meta App → WhatsApp → Configuration → Webhook**
5. الصق الـ URL في خانة **Callback URL**
6. اكتب أي نص كـ **Verify Token** (احتفظ بيه!)
7. اضغط **Verify and Save** ✅

### الخطوة 4 — توليد Access Token دائم

> الـ Token المؤقت بينتهي كل 24 ساعة — استخدم واحد دائم!

1. روح على [business.facebook.com](https://business.facebook.com)
2. **Settings → Users → System Users → Add**
3. سميه أي اسم، اجعل الدور **Admin**
4. **Assign Assets** → أضف حساب الواتساب بتاعك → Full Control
5. **Generate Token** → اختار الـ App بتاعك → اضبط الانتهاء على **Never**
6. ✅ انسخ الـ Token واحفظه في مكان آمن!

### الخطوة 5 — إعداد الـ Credentials في n8n

أضف الـ Credentials دي في n8n:

**WhatsApp Trigger API:**
- Client ID → App ID (من Meta App Settings → Basic)
- Client Secret → App Secret (من Meta App Settings → Basic)

**WhatsApp API (الإرسال):**
- Access Token → الـ System User Token الدائم
- Business Account ID → الـ WABA ID (من Meta Dashboard)

**Groq API:**
- API Key → من [console.groq.com](https://console.groq.com) (مجاني)

### الخطوة 6 — استيراد وضبط الوركفلو الرئيسي

1. استورد `main-whatsapp-ai-agent.json` في n8n
2. حدّث **Phone Number ID** في نود "Send WhatsApp Reply"
3. عدّل الـ **System Prompt** في نود الـ AI Agent حسب مشروعك
4. **فعّل** الوركفلو
5. ابعت رسالة تجريبية من رقمك المسجل ✅

---

## ⚠️ الفرق بين Test Number و Production

| الميزة | Test Number | Production Number |
|--------|-------------|------------------|
| التكلفة | 🆓 مجاني | 💳 مدفوع لكل رسالة |
| حد الأرقام | 5 أرقام فقط | غير محدود |
| نوع الرقم | رقم Meta الأمريكي | رقمك الخاص |
| شارة التحقق الخضراء | ❌ لا | ✅ ممكن |
| توثيق الأعمال | ❌ غير مطلوب | ✅ مطلوب |
| Templates للبدء | ❌ مش لازم | ✅ مطلوب |
| مناسب لـ | اختبار الأتمتة | الاستخدام التجاري الحقيقي |

---

## 🔒 ملاحظات أمان مهمة

- ❌ **لا ترفع** Access Tokens على GitHub أبداً
- ❌ **لا ترفع** App Secrets
- ✅ خزّن كل الأسرار في **n8n Credentials** (مشفّرة)
- ✅ استخدم **System User Tokens** (لا تنتهي) في الإنتاج
- ✅ اقرأ [SECURITY.md](SECURITY.md) قبل النشر

---

## 🐛 مشاكل شائعة وحلولها

<details>
<summary><b>❌ Error 131030 — الرقم مش في الـ Allowlist</b></summary>

**السبب:** في وضع الاختبار، ينفع تبعت بس للأرقام اللي سجّلتها.

**الحل:**
1. روح Meta Dashboard → WhatsApp → Getting Started
2. أضف الرقم في خانة "To"
3. ابعت كود التحقق وأكّده
</details>

<details>
<summary><b>❌ Error 190 — Access Token غير صالح</b></summary>

**السبب:** استخدام Token مؤقت منتهي الصلاحية.

**الحل:** ولّد System User Token دائم (اتبع الخطوة 4 فوق).
</details>

<details>
<summary><b>❌ فشل التحقق من الـ Webhook</b></summary>

**السبب:** Verify Token غير متطابق أو الوركفلو مش شغّال.

**الحل:**
1. تأكد إن وركفلو `meta-webhook-verifier` **Active**
2. تحقق من تطابق الـ Verify Token حرفاً بحرف (بدون مسافات)
3. تأكد إن الـ URL هو **Production URL** مش Test URL
</details>

<details>
<summary><b>❌ البوت بيرد أكثر من مرة على كل رسالة</b></summary>

**السبب:** الـ IF Filter مش موجود أو مش متوصّل صح.

**الحل:** تأكد إن الـ IF Node موجود ومتوصل وبيتحقق من وجود `messages[0].text.body`.
</details>

---

## 🌐 خدمات الأتمتة الاحترافية

<div align="center">

**هل تحتاج إلى حلول أتمتة مخصصة لنشاطك التجاري؟**

أقدم خدمات أتمتة احترافية تشمل بوتات الواتساب والـ AI Agents وتكامل الأنظمة وأتمتة العمليات التجارية الكاملة.

[![زيارة الموقع](https://img.shields.io/badge/🌐_زيارة_الموقع-yousefautomates.pages.dev-blue?style=for-the-badge)](https://yousefautomates.pages.dev/)

**م. يوسف الشربيني | Eng. Yousef Elsherbiny**
خدمات الأتمتة | n8n | AI Agents | WhatsApp Bots

</div>

---

<div align="center">

**⭐ أعجبك المشروع؟ لا تنسى تعمل Star للـ Repository!**

[![GitHub stars](https://img.shields.io/github/stars/YousefAutomates/whatsapp-api-free-n8n-automation?style=social)](https://github.com/YousefAutomates/whatsapp-api-free-n8n-automation/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/YousefAutomates/whatsapp-api-free-n8n-automation?style=social)](https://github.com/YousefAutomates/whatsapp-api-free-n8n-automation/network/members)

*جميع الحقوق محفوظة © 2025 — م. يوسف الشربيني*
*[yousefautomates.pages.dev](https://yousefautomates.pages.dev/)*

</div>
