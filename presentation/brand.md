# Brand & Design Tokens — סדנת Claude Code & Antigravity

> זהות ויזואלית משותפת למצגת (presentation/) ולדף הנחיתה (landing/). כל סוכן בונה-ויזואל קורא קובץ זה לפני עבודה. אסור לסטות מהפלטה/פונטים בלי סיבה.

## עקרון

dark-first, חם, מעשי, "סטודיו". לא קורפורייט קר, לא AI-slop. אסימטריה > grids מרכזיים. הרבה שטח שחור, אקסנט coral נקודתי, טיפוגרפיה גדולה ובוטחת.

## פלטה (CSS variables)

```css
:root {
  /* בסיס כהה */
  --bg:            #0E0D0C;   /* near-black graphite — רקע ראשי */
  --bg-elev:       #1A1816;   /* כרטיסים / שכבות מוגבהות */
  --bg-elev-2:     #242019;   /* hover / שכבה שנייה */
  --line:          #322C26;   /* גבולות עדינים */

  /* אקסנט חם (Claude/Anthropic-ish) */
  --accent:        #E8633A;   /* coral/orange ראשי — CTA, הדגשות */
  --accent-soft:   #F0875F;   /* hover בהיר יותר */
  --accent-deep:   #C24A26;   /* active / לחיצה */
  --accent-2:      #F2C14E;   /* אקסנט משני — חם זהוב, להדגשות נקודתיות */

  /* טקסט */
  --text:          #F5EFE8;   /* טקסט ראשי על כהה — שמנת חם, לא לבן צרוף */
  --text-dim:      #B8AEA3;   /* טקסט משני */
  --text-faint:    #7C736A;   /* metadata / hints */

  /* סמנטי */
  --ok:            #7FB069;
  --warn:          #F2C14E;

  /* צללים צבעוניים (לא אפור) */
  --shadow-accent: 0 18px 50px -12px rgba(232, 99, 58, 0.35);
  --shadow-soft:   0 12px 40px -16px rgba(0, 0, 0, 0.6);

  /* radii */
  --r-sm: 10px; --r-md: 16px; --r-lg: 26px; --r-pill: 999px;
}
```

חוקים: אסור `#ffffff` כרקע hero. אסור raw tailwind colors כ-brand (להשתמש ב-vars). צללים תמיד גוון accent/חם, opacity נמוך.

## טיפוגרפיה

- **Latin display (כותרות לטיניות / מספרים / "Claude Code"):** Clash Display (ראשי) → Space Grotesk (fallback). אסור Inter/Roboto.
- **עברית — כותרות:** Font Polin (אם זמין דרך CDN) → Assistant. **גוף עברי:** Assistant. Heebo רק כ-fallback אחרון, לעולם לא לבד.
- מ-Google Fonts זמינים: Assistant, Heebo, Space Grotesk. Clash Display / Font Polin — דרך Fontshare/CDN; אם לא נטען, fallback ל-Space Grotesk / Assistant בהתאמה.

```css
--font-display: "Clash Display", "Space Grotesk", system-ui, sans-serif; /* לטינית */
--font-he-head: "Polin", "Assistant", system-ui, sans-serif;            /* כותרות עברית */
--font-he-body: "Assistant", "Heebo", system-ui, sans-serif;            /* גוף עברית */
```

סקאלה: כותרת hero clamp(2.6rem, 6vw, 5.5rem), bold/extrabold. גוף 1.05–1.2rem, line-height ~1.65 לעברית. measure ≤ 70 תווים.

## RTL

- `dir="rtl"` ב-`<html>`. כל ה-layouts ממוסכים (logical properties: margin-inline, padding-inline, inset-inline).
- מספרים/קוד/אנגלית בתוך עברית — לעטוף ב-`<span dir="ltr">` כשצריך.
- inputs ב-RTL, אייקונים ממוסכים בכיוון.

## טון קולי (copy voice)

- ישיר, חם, ביטחון בלי יוהרה. "אתם המנהלים, הסוכן עובד."
- משפטים קצרים. פועל ראשון. בלי באז-וורדס ("מהפכני", "פורץ דרך" — אסור).
- מספרים קונקרטיים: "יום אחד", "10 מקומות", "מאפס ועד מוצר חי".
- דוגמה hero: "תבנו מוצר אמיתי. ביום אחד. בלי לדעת קוד."

## מוטיבים ויזואליים

- "terminal/agent" subtle: caret מהבהב, mono ל-snippets, prompt `›`.
- צעדי agent: קורא → מתכנן → כותב → מריץ → מתקן (loop) — מוטיב חוזר.
- placeholder לצילום מסך: מסגרת חלון (dots אדום/צהוב/ירוק בפינה) + **עיגול אדום** מודגש על האזור שמדגימים. ברירת מחדל לכל שקופית 🔴.
- gradient mesh עדין coral→שקוף ברקע hero; noise/grain עדין מותר.

## נגישות

- ניגודיות AA: --text על --bg עובר 4.5:1. אקסנט coral על כהה לטקסט גדול בלבד; ל-CTA טקסט כהה (#0E0D0C) על coral.
- focus ring נראה (accent, 2px). מבנה כותרות h1→h6. alt לכל תמונה. ראו skill israeli-accessibility-compliance ל-IS 5568.
