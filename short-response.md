# Short Response Questions

Answer each question below in your own words. Aim for 3–5 sentences per answer. Be specific — use the exact terms and concepts from the lesson.

Your responses will each be evaluated out of 6 points. You can earn 3 points for writing quality and 3 points for the accuracy and precision of the technical content per question.

---

## Question 1:

Why is it unsafe to make requests to a third-party API (like Giphy) directly from frontend JavaScript code? What specific risk does this create, and how can a malicious user exploit it?

**Your answer here**:

Making requests to a third-party **API** from **frontend JavaScript** is unsafe because users can see and steal API keys from the **code** or **network requests**. A malicious user could misuse the key to make unlimited requests, causing costs or rate-limit issues.

---

## Question 2:

What is the proxy server strategy? How does it help avoid exposing API Keys in client-side code while still providing access to APIs that require keys?

**Your answer here**:

The **proxy server** strategy involves sending **API** requests from the **frontend** to your own **backend server** instead of directly to the third‑party API. The backend acts as a middle layer (proxy) that stores the API **key** securely, usually in **environment variables**, and then makes the request to the external API on behalf of the **client**. This prevents the API key from being exposed in **client-side code** because the browser only communicates with your server, not the third-party service directly. As a result, users cannot access or steal the API key while still being able to receive the data from the API through your backend.

---

## Question 3:

What is an environment variable, and why do we store API keys in a .env file instead of directly in source code? What role does .gitignore play in this setup, and what could go wrong if the .env file were accidentally committed to GitHub?

**Your answer here**:

An **environment variable** stores sensitive values like **API keys** outside your code so they aren’t exposed. We keep them in a `.env` file and add it to `.gitignore` to prevent committing it to **GitHub**. If the file is accidentally pushed, anyone could see and misuse the keys, causing unauthorized requests, rate-limit issues, or unexpected costs.

---
