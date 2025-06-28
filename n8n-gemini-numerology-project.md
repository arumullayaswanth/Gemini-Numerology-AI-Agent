# 🔮 Gemini Numerology AI Assistant

## 🤖 Google Gemini AI Automation Project using n8n (AI Studio)

## ✅ Step 0: Get Gemini API Key

1. Go to [Google](https://www.google.com)
2. Search: `Google AI Studio`
3. Click the official link to [Google AI Studio](https://makersuite.google.com/)
4. Sign in with your Google account
5. Click **“Get API Key”**
6. Select **Gemini API**
7. Choose to **Create API Key in Existing Project**
8. Click **Create**
9. **Copy the API Key** and keep it safe

---


## 📍 Step 1: Visit n8n Official Website
1. Go to [Google](https://www.google.com) → search for **"n8n"** → click the official n8n link (https://n8n.io) → click **“Get started for free”** → fill the form:
   - Full Name: `Arumulla Yaswanth Reddy`
   - Company Email: `Yaswanth.arumulla@gmail.com`
   - Confirm Email: `Yaswanth.arumulla@gmail.com`
   - Password: `************`
   - Account Name: `yaswanth-app.n8n.cloud` *(avoid double dots)*
   - Click **Start free 14-day trial** 
   - Answer onboarding questions (usage: Personal learning, role: Engineer, source: Google)
   - start automation.

## ⚙️ Step 2: Start Your First Automation in n8n

### 🔄 Step 2.1: Chart Trigger (Start Point)

- Click **“Create Workflow”**
- Click the **( + )** button
- Under **“What triggers this workflow”**, search: `Chart Trigger`
- Add **Chart Trigger**
- Click **Execute Step**
- Then **Back to Canvas**
- ✅ **Test**: Click **Open Chat** → type any message like “Hello”

---

### 🧠 Step 2.2: Add Gemini AI Chat Model (AI Agent)

- Click the **( + )** button → Search `AI` → Select `AI Agent`
- Double-click **AI Agent**:
  - Under **Options**, click **"Add Option"**
  - Add new **System Message**
  - **Replace existing message** with:

    ```
    Act as an expert numerologist. Given a person's full name and date of birth, generate a detailed Personal Numerology Report in a fixed structure: (1) Name & Birth Details, (2) Core Numbers Summary (Life Path, Expression, Soul Urge, Personality, Birthday, Maturity), (3) Interpret each number in 1 paragraph each, (4) Include Hidden Challenges, Pinnacle Cycles, and a short Personal Year Forecast, (5) End with 2 lines of uplifting guidance. Always use a warm, wise tone and keep the format consistent for every report.

    ```

- Click **Execute Step**
- Click **Back to Canvas**

---

### 🤖 Step 2.3: Add Google Gemini Chat Model

- Click **( chat modal + )** → Search `Google Gemini Chat Model`
- Under **Credential to connect with**, click **Create New Credential**
  - **Host**: leave default
  - **API Key**: Paste your **Gemini API Key**
  - Save
- Double-click **Google Gemini Chat Model**:
  - Select **Model**: `models/gemini-2.0-pro` *(or latest available)*
- Click **Back to Canvas**

✅ **Test**: Open Chart → Type:
```
Hi
You didn't get any answer because there is no memory we won't add memory
```

---

### 🧠 Step 2.4: Add Memory to Maintain Context

- Click **( memory + )** → Search `Simple Memory`
- Select it
- Set **Context Window Length**: `50`
- Click **Back to Canvas**

✅ **Test**: Open Chart → Type:
```
Hi, my name is Yaswanth
What is my name?
Can you prepare a numerology report?
Yaswanth Reddy 23-06-2002
```
---

### 📧 Step 2.5: Add Gmail Tool for Emailing Reports

- Click **( Tool + )** → Search `Gmail Tool`
- Under **Credential to connect with**, click **Create New Credential**
  - Sign in with Google and authorize
- Fill parameters:
  - **To**: `Let the model define this parameter`
  - **Subject**: `Let the model define this parameter`
  - **Message**: `Let the model define this parameter`
  - **Email Type**: `text`
- Click **Execute Step** → **Back to Canvas**

✅ **Test**:
```
Prepare a numerology report for Yaswanth Reddy, DOB 23-06-2002
Mail it to Yaswanth.20bes7010@vitap.ac.in
```

---

### 📲 Step 2.6: Add Telegram Tool for Sending Reports

- In Telegram:
  - Search for `@BotFather`
  - Click **Start**
  - Send `/newbot`
  - Choose a bot name (e.g., `NumerologyBot`)
  - Copy the **HTTP API Token**
- Start the bot (click the link from BotFather)

- In n8n:
  - Click **( Tool+ )** → Search `Telegram Tool`
  - Under **Credential to connect with**, click **Create New Credential**
  - Paste your **Access Token**
  - Set:
    - **Chat ID**: `Let the model define this parameter`
    - **Text**: `Let the model define this parameter`
- Click **Execute Step** → **Back to Canvas**

✅ **Test** in Chat:
```
Send my numerology report to Telegram.
```

---

## 🌍 Step 3: Make It Public & Share

- Click **“Activate”** on top-right
- Save the project
- Double-click **Chart Trigger**
  - Enable: **Make chart publicly available**
- Copy **Public Chat URL**
- Paste it in your browser — ✅ Your AI Numerologist is live!

---

### ✅ Final Test Example

Type in chat:

```
Hi! My name is Yaswanth Reddy and my date of birth is 23-06-2002. Please generate my numerology report and email it to Yaswanth.20bes7010@vitap.ac.in and also send it on Telegram.
```
