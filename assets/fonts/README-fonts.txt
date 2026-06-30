=== הוראות הורדת פונטים מקומיים (Horian Taxi) ===

הדף בנוי לטעון פונטים מקומית (ביצועים + אפס תלות ב-Google).
עד שתורידי את הקבצים, הדף עובד מצוין עם פונטי מערכת (fallback).

להורדה (קל, בקליק):
1. היכנסי ל-  https://gwfh.mranftl.com/fonts
2. הורידי את שני הפונטים האלה, פורמט "Modern Browsers" (woff2):
   • Heebo  — משקלים: 300, 400, 500, 700
   • Frank Ruhl Libre — משקלים: 400, 700, 900
3. שמרי את קבצי ה-.woff2 בתיקייה הזו (assets/fonts/) עם השמות:
   heebo-300.woff2  heebo-400.woff2  heebo-500.woff2  heebo-700.woff2
   frankruhl-400.woff2  frankruhl-700.woff2  frankruhl-900.woff2

זהו. ה-@font-face ב-index.html כבר מצביע על השמות האלה.