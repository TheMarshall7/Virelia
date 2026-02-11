# GoHighLevel Form Setup for Contact / Opt-in (Compliance Review)

The contact page uses a **GoHighLevel (GHL) form embed** so the Areo/GHL compliance review can detect your disclosures. Follow these steps.

---

## 1. Create the form in GoHighLevel

1. In **GoHighLevel**, go to **Forms** (or **Snap** / **Funnels** > form).
2. Create a new form or use an existing one. Add fields you need: First Name, Last Name, Email, Phone, Message, etc.
3. **Do not** make the consent checkbox required (GHL and carriers require it to be optional).

---

## 2. Add compliant opt-in language in the form

In the form builder, add a **Text** or **Description** block (and/or use the **Terms & Conditions** element if available) that includes **all** of the following. This is what the compliance review looks for:

- **Business name:** e.g. “Virelia Insurance Group”
- **Message type disclosure:** e.g. “You may receive: responses to your inquiry, appointment reminders, follow-ups, and occasional marketing (email, phone, and/or SMS).”
- **Message frequency disclosure:** e.g. “Message frequency varies.”
- **Message & data rates disclosure:** e.g. “Message and data rates may apply.”
- **Opt-out instructions:** e.g. “Reply STOP to unsubscribe. Reply HELP for help.”

Example block you can paste into the form description:

```
By submitting, you agree to receive text messages and communications from Virelia Insurance Group. Message types: responses to your inquiry, appointment reminders, follow-ups, and occasional marketing. Message frequency varies. Message and data rates may apply. Reply STOP to unsubscribe. Reply HELP for help.
```

4. Add a **consent checkbox** (optional, not required) with short consent text.
5. At the **bottom of the form**, add links to your **Privacy Policy** and **Terms of Service** (same URLs as on your site, e.g. yourdomain.com/privacy-policy.html and yourdomain.com/terms-of-service.html).

---

## 3. Get the form embed URL

1. Open your form in GHL.
2. Go to **Share** or **Embed**.
3. Copy the **embed URL** or **iframe src**. It may look like:
   - `https://forms.leadconnectorhq.com/forms/XXXXXXXX/embed`
   - or `https://api.leadconnectorhq.com/widget/...`

---

## 4. Update contact.html with your form URL

1. Open `contact.html` in your project.
2. Find the iframe with `src="https://forms.leadconnectorhq.com/forms/REPLACE_WITH_YOUR_GHL_FORM_ID/embed"`.
3. Replace **REPLACE_WITH_YOUR_GHL_FORM_ID** (or the whole `src`) with your actual GHL form embed URL.
4. Save and publish your site.

---

## 5. Point compliance review at the right URL

- In Areo/GHL compliance or A2P registration, set the **opt-in form URL** to your **contact page** (e.g. `https://yourdomain.com/contact.html`).
- The review may also accept the **direct GHL form URL** if the form is public. Check the compliance tool’s instructions.

Once the form is built in GHL with the language above and embedded on your contact page, the automated review should recognize the disclosures because they live inside the GHL form it’s designed to scan.
