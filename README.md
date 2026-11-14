# Ibrahim Khalil AI 🤖

A sleek, modern, and fully responsive AI chat assistant interface powered by an unofficial ChatGPT backend. Built with vanilla HTML, CSS, and JavaScript, and deployed on Vercel using Serverless Functions.

## 🚀 Features

- **💬 Real-time AI Chat:** Interactive chat interface with a DeepSeek-inspired dark theme.
- **🖼️ Image Upload (Multimodal):** Attach images to your messages and let the AI analyze them.
- **💻 Code Highlighting:** Supports Markdown rendering with syntax highlighting and a "Copy Code" button.
- **⚡ API Generator:** Built-in tool to generate and test API URLs directly from the UI.
- **📱 Mobile-First Design:** Fully responsive layout with a smooth sidebar for mobile devices.
- **☁️ Serverless Architecture:** Uses Vercel Serverless Functions as a proxy to bypass CORS and interact with the AI backend anonymously.

## 📁 Project Structure

```text
├── api/
│   ├── chat.js          # Serverless proxy for text-based AI responses
│   └── chat-image.js    # Serverless proxy for image uploads & multimodal AI
├── public/
│   └── index.html       # Complete frontend (HTML, CSS, JS)
├── vercel.json          # Vercel routing and configuration
└── AGENTS.md            # Development guidelines and notes
```

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3 (Vanilla), JavaScript (ES6+)
- **Backend:** Node.js (Vercel Serverless Functions)
- **Libraries (CDN):** [Marked](https://marked.js.org/) (Markdown parsing), [Highlight.js](https://highlightjs.org/) (Syntax highlighting)

## 🌐 Live Demo & Deployment

This project is configured for zero-config deployment on **Vercel**.

### How to Deploy:
1. Fork or Clone this repository.
2. Go to [Vercel](https://vercel.com) and sign in with GitHub.
3. Click **"Add New"** -> **"Project"**.
4. Import this repository.
5. Click **"Deploy"**. Vercel will automatically detect the `public` folder and the `api` serverless functions.

## 🔌 API Endpoints

If you want to use this backend for your own applications:

### 1. Text Chat (GET)
```http
GET /api/chat?message=Hello%20AI
```

### 2. Image Chat (POST)
```http
POST /api/chat-image
Content-Type: application/json

{
  "message": "What is in this image?",
  "images": [
    {
      "base64": "iVBORw0KGgoAAAANSUhEUgAA...",
      "mime": "image/png",
      "name": "image.png"
    }
  ]
}
```

## ⚠️ Disclaimer

This project uses an **unofficial, reverse-engineered API** to communicate with OpenAI's services. It fabricates Android client headers and Cloudflare cookies to mimic the official ChatGPT app. 
*This project is for **educational purposes only**. OpenAI may patch this endpoint at any time, which could result in 403 Forbidden errors or service unavailability. Use it at your own risk.*

## 👨‍💻 Developer

**Ibrahim Khalil**
- WhatsApp: [Contact Me](https://wa.me/8801838852487)

---
*© 2026 Ibrahim Khalil. All rights reserved.*
