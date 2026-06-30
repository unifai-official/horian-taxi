═══════════════════════════════════════════════════════════════
  Horian Premium Taxi — דף נחיתה | צ'קליסט השקה ומדריך
═══════════════════════════════════════════════════════════════

📁 מבנה הקבצים
─────────────────────────────────────────────
  index.html              ← הדף המלא (HTML+CSS+JS בקובץ אחד)
  robots.txt              ← לדרוס דומיין בתוכו
  sitemap.xml             ← לדרוס דומיין בתוכו
  assets/
    car-hero-*.webp       ← תמונת Hero (LCP)
    car-4seat / 6seat / minibus / access -*.webp  ← כרטיסי רכב
    logo-96 / logo-256.webp, favicon-32 / favicon-180.png
    og-image.jpg          ← תמונת שיתוף (1200×630)
    fonts/                ← לשים כאן את ה-woff2 (ראו README-fonts.txt)

  קבצי המקור (Logo.jpg, מונית*.png) ו-node_modules/ — לא נחוצים
  לפרודקשן, אפשר למחוק לפני העלאה.


✅ צ'קליסט לפני העלאה לאוויר
─────────────────────────────────────────────
□ 1. דומיין — להחליף "horiantaxi.co.il" בדומיין האמיתי ב:
     • index.html: canonical, og:url, og:image, twitter:image,
       JSON-LD (url + image בשני הבלוקים)
     • robots.txt (שורת Sitemap)
     • sitemap.xml (loc)
     חיפוש-והחלף גלובלי של "horiantaxi.co.il" יתפוס הכל.

□ 2. פונטים — להוריד 7 קבצי woff2 (ראו assets/fonts/README-fonts.txt)
     ולשים ב-assets/fonts/. בלעדיהם הדף עובד עם פונט מערכת.

□ 3. טלפון — מאומת: 053-633-3537 / 972536333537.
     אם משתנה — לעדכן ב-CONFIG (index.html, בתוך <script>):
     whatsappNumber + displayPhone, וגם ב-JSON-LD telephone.

□ 4. אנליטיקס — למלא ב-CONFIG:
     ga4Id: "G-XXXXXXX"     (Google Analytics 4)
     metaPixelId: "XXXXXX"  (Meta/Facebook Pixel)
     האירועים lead_whatsapp / lead_whatsapp_general נשלחים אוטומטית.

□ 5. ערים — CONFIG.cities מכיל ~60 ערים. להוסיף/להסיר לפי הצורך
     (משמש גם ל-autocomplete וגם ל"אזורי שירות"). אם מוסיפים ערים
     מרכזיות — כדאי להוסיפן גם ל-areaServed ב-JSON-LD (SEO מקומי).

□ 6. תמונת OG — assets/og-image.jpg מוכנה. לבדוק תצוגה ב:
     https://www.opengraph.xyz/ (להדביק את ה-URL אחרי העלייה).


🚀 העלאה ל-Vercel
─────────────────────────────────────────────
  אפשרות א (הכי קל): גרירת התיקייה ל-vercel.com/new → Deploy.
  אפשרות ב: vercel CLI → "vercel --prod" מתוך התיקייה.
  אין build — זה אתר סטטי. Vercel מגיש את index.html ישירות.
  לאחר חיבור דומיין: לוודא HTTPS פעיל (אוטומטי ב-Vercel).


🔎 אחרי ההשקה — SEO ו-Google
─────────────────────────────────────────────
□ Google Search Console — לאמת בעלות על הדומיין, להגיש sitemap.xml.
□ בדיקת Schema — https://search.google.com/test/rich-results
   (להדביק URL — לוודא TaxiService + FAQPage תקינים).
□ PageSpeed — https://pagespeed.web.dev/ (לוודא LCP < 2.5ש' במובייל).
□ Google Business Profile (GBP) — לפתוח/לאמת פרופיל עסקי:
   שם: Horian Premium Taxi · טלפון: 053-633-3537 · קטגוריה: שירות מוניות
   אזור שירות (לא כתובת פיזית) · שעות: 24/7 · קישור לאתר.
   זה הדרייבר #1 לתנועה מקומית ("מונית ליד" / "מונית ב{עיר}").
□ פיקסלים — לבדוק ש-GA4 ו-Meta Pixel קולטים את אירוע lead_whatsapp
   (ללחוץ "שלח בוואטסאפ" ולראות באירועים בזמן אמת).


♿ נגישות (ת"י 5568)
─────────────────────────────────────────────
  הדף כולל ווידג'ט נגישות מובנה (כפתור בפינה שמאלית-תחתונה):
  הגדלת טקסט · ניגודיות גבוהה · הדגשת קישורים · עצירת אנימציות · איפוס.
  בנוסף: skip-link, focus states, ARIA למודאל, ניווט מקלדת, alt לתמונות,
  ותמיכה ב-prefers-reduced-motion.
  ⚠️ מומלץ: להוסיף "הצהרת נגישות" (דף/עמוד נפרד) — חובה חוקית בישראל
  לעסקים. אפשר ליצור חינם ב: https://www.gov.il (חיפוש "הצהרת נגישות").


📋 מה שכבר טופל (אין צורך לגעת)
─────────────────────────────────────────────
  ✓ תמונות WebP responsive (חיסכון ~96% מהמקור)
  ✓ פונטים מקומיים + preload (אחרי הורדתם)
  ✓ Hero image כ-LCP עם fetchpriority + srcset
  ✓ JSON-LD: TaxiService + LocalBusiness + FAQPage (5 שאלות, תואם לדף)
  ✓ OG + Twitter cards
  ✓ מודאל דו-שלבי + autocomplete + deep-link וואטסאפ + אנליטיקס
  ✓ הודעת וואטסאפ לפי התבנית: "שלום, מעוניין/ת להזמין {רכב}..."
  ✓ כפתור וואטסאפ צף (ימין, RTL)
  ✓ אינטרו קצר (0.9ש') בלי נעילת גלילה — LCP מהיר
═══════════════════════════════════════════════════════════════