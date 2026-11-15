# Little Moon Light — free CBSE learning app

**Little Moon Light** is the free version of Little Moon for CBSE learners in Classes 1–8. It includes key words, fresh multiple-choice practice with explanations, custom-mark timed question papers, PDF downloads, and fun facts.

There is no sign-in, trial timer, subscription, or access approval in Little Moon Light. The Razorpay donation form is optional; learners can use the app without donating.

## Run locally

1. Install Python 3.12.
2. Create and activate a virtual environment.
3. Install dependencies with `pip install -r requirements.txt`.
4. Add `GEMINI_API_KEY` to `.streamlit/secrets.toml` or your environment.
5. Run `streamlit run app.py`.

Example `.streamlit/secrets.toml`:

```toml
GEMINI_API_KEY = "your-key"
```

Never commit a real API key. Add it in the deployed app's Secrets.

## Deploy as a new Streamlit app

1. In Streamlit Community Cloud, create a new app from **`75neel-ops/little-moon-light`**, branch **`main`**, main file **`app.py`**.
2. Add `GEMINI_API_KEY` under the new app's **Settings → Secrets**.
3. Deploy and share the new Streamlit URL. This is a separate app from the paid Little Moon deployment.

The optional donation button is already configured with the Razorpay button ID supplied by the owner: `pl_Tvez6NOZsFJFmN`. To change it later, update the `data-payment_button_id` value in `app.py`.

## Optional install page

This repository includes the Little Moon Light install page. To use it:

1. Deploy the Streamlit app and copy its URL into `app-url.txt`.
2. Enable GitHub Pages for the `main` branch using the repository root.
3. Open `https://75neel-ops.github.io/little-moon-light/` and install it from the browser menu. On iPhone or iPad, use **Share → Add to Home Screen**.

The install page will remain on its welcome screen until a Streamlit app URL is added to `app-url.txt`.

## Curriculum note

Chapter suggestions are broad CBSE/NCERT examples. Schools may use different textbooks, subjects, and chapter names, so learners can enter their own chapter. English and Bengali are the language subjects offered; generated content for the other subjects is in English.
