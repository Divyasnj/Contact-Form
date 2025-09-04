
# 📬 Contact Form (HTML + CSS + Web3Forms Integration)

A responsive **Contact Form** built with **HTML, CSS**, and integrated with **Web3Forms API** for form submissions without needing a backend.  

This project is ideal for portfolios and real-world projects where you want a quick and secure way to collect user messages.

---

## 🚀 Features
- **Responsive Design** – Works seamlessly on desktop and mobile.
- **Form Validation (HTML5)** – Required fields (`name`, `email`, `message`) ensure valid input.
- **Web3Forms Integration** – Collects form submissions using API (no backend required).
- **Modern UI/UX** – Gradient backgrounds, styled inputs, and submit button with an icon.
- **Accessibility** – Semantic HTML structure with placeholders and focus styles.

---

## 🛠️ Technologies Used
- **HTML5** – Structure of the form and layout.
- **CSS3 (Flexbox + Media Queries)** – Responsive design, modern styling, gradients.
- **Web3Forms API** – Handles form submissions securely with an `access_key`.

---

## 📂 Project Structure



---

## ⚙️ How It Works (Core Logic)
1. The form uses `action="https://api.web3forms.com/submit"` with `method="POST"`.
2. A hidden input (`access_key`) authenticates requests with Web3Forms API.
3. User fills **Name**, **Email**, and **Message**.
4. On submit, data is sent directly to Web3Forms servers → delivered to the configured email.
5. No backend server or database is required.

---

## 📱 Responsive Design
- On screens smaller than **600px**, the form adjusts:
  - Input fields shrink to **80% width**.
  - The right-side illustration is hidden.

---

## 🔑 Key Interview Talking Points
If asked about this project in an **interview**, you can highlight:
- **Form Handling without Backend**: Using Web3Forms API to bypass writing custom backend code.
- **Security Consideration**: Using an API key (`access_key`) instead of exposing email directly.
- **Responsive UI/UX**: Applying Flexbox and media queries for adaptability.
- **Scalability**: Could integrate with backend later (Node.js, Express, MongoDB).
- **Accessibility & Usability**: Clear placeholders, focus styles, and semantic structure.

**Example Interview Answer:**  
> *“In this project, I built a responsive contact form using HTML and CSS, and integrated it with Web3Forms API. The form validates input using built-in HTML5 validation and securely submits data via POST requests. I focused on responsive design with media queries and styled components for better user experience. This approach is lightweight and scalable, and can later be extended with a backend for advanced features.”*

---

## 📸 Screenshot
*(Add your screenshot here for better presentation)*

---

## 📩 Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Divyasnj/contact-form.git


   🔑 Core Logic Code
1. Form Submission with Web3Forms
<form action="https://api.web3forms.com/submit" method="POST" class="contact-left">
    <!-- API Key (hidden for security) -->
    <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY_HERE">

    <!-- User Inputs -->
    <input type="text" name="name" placeholder="Your Name" class="contact-inputs" required>
    <input type="email" name="email" placeholder="Your Email" class="contact-inputs" required>
    <textarea name="message" placeholder="Your Suggestion" class="contact-inputs" required></textarea>

    <!-- Submit Button -->
    <button type="submit">Submit</button>
</form>


✅ Core logic:

action="https://api.web3forms.com/submit" → sends data directly to Web3Forms server.

method="POST" → ensures data is sent securely.

input type="hidden" with access_key → authenticates the request.

required → enforces HTML5 form validation (no empty fields).

2. Responsive Design with Media Queries
/* Input field styling */
.contact-inputs {
    width: 400px;
    height: 50px;
    padding-left: 25px;
    border-radius: 50px;
    border: none;
    outline: none;
    font-weight: 600;
}

/* Textarea adjustment */
.contact-left textarea {
    height: 140px;
    padding-top: 25px;
    border-radius: 20px;
}

/* On smaller screens */
@media (max-width: 600px) {
    .contact-inputs {
        width: 80vw; /* Auto adjusts to screen width */
    }
    .contact-right {
        display: none; /* Hide image on mobile */
    }
}


✅ Core logic:

Inputs styled for clarity.

Textarea taller for longer messages.

Media query makes form adapt to smaller devices.

3. Focus & Placeholder Styling
/* Highlight active input */
.contact-inputs:focus {
    border: 2px solid #c7334f;
}

/* Light gray placeholder text */
.contact-inputs::placeholder {
    color: #a9a9a9;
}


✅ Core logic:

Visual feedback when a user clicks inside a field.

Improves UX & accessibility.
