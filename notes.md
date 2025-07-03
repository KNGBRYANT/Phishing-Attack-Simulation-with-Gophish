# 🗒️ Project Notes – Phishing Simulation with Gophish

## 🧠 Why This Project?
I built this project to understand how phishing works from the attacker's perspective, so I can better defend against it. It’s also a hands-on way to learn about tools, user behavior, and phishing campaign structures.

---

## 🔧 What I Did

- ✅ Deployed Gophish using Railway (Docker template)
- ✅ Created a realistic phishing email template
- ✅ Hid the raw phishing link using HTML to make the email look legitimate (e.g., hyperlinking button text instead of showing full URL)
- ✅ Set up a landing page that mimics a login form
- ✅ Linked the landing page to the email via campaign
- ✅ Used Gmail SMTP to send emails (for testing only)
- ⚠️ Skipped full HTTPS config due to SSL limitations

---

## 🚧 Challenges Faced

- ❌ Couldn't get SSL (HTTPS) working — browser forced HTTPS, while Gophish only served HTTP
- ❌ Campaign links led to 404 because listener wasn’t reachable via HTTPS
- ⚠️ Had to use plain HTTP as a workaround for demo purposes
- ❌ Gmail SMTP gave errors until correct settings + password were used
- ⛔ Campaign status showed "error" until I fixed the envelope sender and SMTP auth

---

## 🧪 Testing Summary

- Emails were received successfully
- Link in email redirected to landing page (HTTP workaround)
- Campaign dashboard tracked clicks and data submissions (where applicable)

---

## 📝 Lessons Learned

- TLS/SSL is critical when deploying phishing simulations for realism
- Users often overlook URLs if the email is convincing enough
- SPF/DKIM checks can block or flag emails — envelope sender matters
- Campaigns must have properly mapped landing pages and listener URLs
