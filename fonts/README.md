# Fonts Pack — פונטי המותג

הפונטים והצבעים של הקורס, מוכנים להדבקה. **אין צורך להוריד קבצי פונט** — הכל נטען מ-CDN. פשוט הוסיפו את הקישורים ל-`<head>` או ייבאו את `brand-fonts.css`.

## הפונטים

| תפקיד | פונט ראשי | Fallback | מקור |
|---|---|---|---|
| כותרות לטיניות / מספרים / "Claude Code" | **Clash Display** | Space Grotesk | Fontshare |
| כותרות עברית | **Polin** | Assistant | CDN ידני (אם זמין) → אחרת Assistant |
| גוף עברית | **Assistant** | Heebo | Google Fonts |
| Fallback לטיני | **Space Grotesk** | system-ui | Google Fonts |

> כלל מותג: **אסור Inter / Roboto** ככותרות. Heebo רק כ-fallback אחרון, לעולם לא לבד.

## דרך 1 — תגי `<link>` ב-`<head>` (מומלץ)

```html
<!-- Google Fonts: Assistant + Space Grotesk -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Assistant:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

<!-- Fontshare: Clash Display -->
<link href="https://api.fontshare.com/v2/css?f[]=clash-display@400,500,600,700&display=swap" rel="stylesheet">
```

## דרך 2 — `@import` ב-CSS

ייבאו את הקובץ המצורף, או העתיקו את ראש [`brand-fonts.css`](brand-fonts.css):

```css
@import url('https://fonts.googleapis.com/css2?family=Assistant:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap');
@import url('https://api.fontshare.com/v2/css?f[]=clash-display@400,500,600,700&display=swap');
```

## משתני ה-CSS

הקובץ [`brand-fonts.css`](brand-fonts.css) כולל את כל ה-`--font-*` ואת פלטת הצבעים (`--bg`, `--accent` ועוד) ב-`:root` — מוכן לשימוש:

```css
--font-display: "Clash Display", "Space Grotesk", system-ui, sans-serif;
--font-he-head: "Polin", "Assistant", system-ui, sans-serif;
--font-he-body: "Assistant", "Heebo", system-ui, sans-serif;
```

## על Polin

**Font Polin** הוא פונט הכותרות העברי המועדף, אך הוא **אינו ב-Google Fonts**. אם יש ברשותכם קישור CDN רשמי שלו — הוסיפו אותו ל-`<head>` או כ-`@import` נוסף. בלעדיו, כותרות העברית נופלות אוטומטית ל-**Assistant** (שכבר נטען), כך שהדף נשאר תקין.

## RTL

הדפים בעברית הם `dir="rtl"`. עטפו מספרים/קוד/אנגלית בתוך עברית ב-`<span dir="ltr">` כשצריך, והשתמשו ב-logical properties (`margin-inline`, `padding-inline`).
