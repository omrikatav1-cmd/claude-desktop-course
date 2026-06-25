# 30 סקילים מומלצים — קורס Claude Desktop

> **חלק מחבילת הבונוסים.** הרשימה היא הצעה — ערכו לפי הצרכים שלכם.
> 15 מועדפי עומרי · 15 מועדפי טל. סה"כ 30 סקילים בשישה תחומים.

---

## תחום 1 · עיצוב ופרונט

| סקיל | תיאור | בחירת מי |
|---|---|---|
| `ui-ux-pro-max` | עיצוב UI/UX ברמה גבוהה — מבנה, היררכיה, חוויית משתמש | עומרי |
| `frontend-design-pro` | פרונטאנד בסטנדרט גבוה: ריספונסיב, RTL, accessibility מובנה | עומרי |
| `landing-page-design` | עיצוב דפי נחיתה ממירים — מבנה סקשנים, CTA, עיצוב visual | עומרי |
| `premium-experience` | ממשקים פרימיום: מיקרואינטראקציות, פרטים, תחושת high-end | עומרי |
| `animation-designer` | אנימציות UI ידידותיות — CSS transitions, hover states, entrance | טל |
| `motion-framer` | אנימציות מתקדמות עם Framer Motion ב-React | טל |
| `glassmorphism` | עיצוב זכוכית/blur — שכבות, שקיפות, depth | טל |
| `design-system` | בניית design system מלא: tokens, components, variants | עומרי |

---

## תחום 2 · בנייה ופיתוח

| סקיל | תיאור | בחירת מי |
|---|---|---|
| `test-driven-development` | כתיבת בדיקות לפני קוד — unit, integration, TDD cycle | טל |
| `systematic-debugging` | גישה מובנית לאיתור ותיקון באגים — לוגים, bisect, hypothesis | טל |
| `bash-script-generator` | יצירת סקריפטים bash לאוטומציה, CI, עיבוד קבצים | טל |
| `github-actions-generator` | בניית pipelines CI/CD ב-GitHub Actions | טל |
| `dockerfile-generator` | יצירת Dockerfiles נקיים, multi-stage, production-ready | טל |

---

## תחום 3 · תוכן ושיווק

| סקיל | תיאור | בחירת מי |
|---|---|---|
| `copywriting` | כתיבת קופי ממיר — כותרות, CTAs, תיאורים, מסרים | עומרי |
| `page-cro` | אופטימיזציה לשיעור המרה: ניתוח דף, הצעות שיפור, A/B | עומרי |
| `email-sequence` | בניית רצף מיילים אוטומטי — welcome, nurture, re-engagement | עומרי |
| `cold-email` | כתיבת מיילים קרים שנפתחים — נושא, גוף, CTA | עומרי |
| `content-strategy` | אסטרטגיית תוכן: פרסונות, ערוצים, לוח שנה, מסרי ליבה | עומרי |
| `marketing-psychology` | שילוב עקרונות פסיכולוגיה בשיווק: דחיפות, הוכחה חברתית, framing | עומרי |
| `seo-audit` | ביקורת SEO מלאה: meta, structure, speed, internal links | טל |

---

## תחום 4 · ישראלי ונגישות

| סקיל | תיאור | בחירת מי |
|---|---|---|
| `israeli-accessibility-compliance` | עמידה בתקן IS 5568 + WCAG 2.1 AA — חובה לכל אתר ישראלי | עומרי |
| `hebrew-rtl-best-practices` | RTL נכון בעברית: מיקומים, inputs, ניגודים, קריאות | עומרי |
| `hebrew-content-writer` | כתיבת תוכן איכותי בעברית בגובה העיניים — ישיר, ברור, ממיר | עומרי |
| `israeli-ui-design-system` | design system מותאם לישראל: RTL, מרווחים, פונטים | טל |
| `hebrew-tailwind-preset` | הגדרת Tailwind מותאמת לעברית ו-RTL מהיום הראשון | טל |

---

## תחום 5 · אוטומציה ו-DevOps

| סקיל | תיאור | בחירת מי |
|---|---|---|
| `github-actions-generator` | (ראה תחום 2) | טל |
| `terraform-generator` | כתיבת Terraform ל-infrastructure as code | טל |
| `k8s-yaml-generator` | יצירת manifests ל-Kubernetes — deployments, services, ingress | טל |
| `ai-seo` | SEO מבוסס AI: keyword research, content briefs, schema | עומרי |
| `programmatic-seo` | בניית עמודי SEO בקנה מידה — templates, data-driven pages | עומרי |

---

## תחום 6 · מטא וניהול

| סקיל | תיאור | בחירת מי |
|---|---|---|
| `writing-plans` | כתיבת Plans מפורטים לפני קוד — ארכיטקטורה, שלבים, קבצים | טל |
| `brainstorming` | סיעור מוחות מובנה: רעיונות, אפשרויות, פרוריטיזציה | עומרי |
| `find-skills` | מחפש סקילים מתאימים לפי משימה — discovery כלי | טל |
| `skill-creator` | יוצר סקיל חדש מהיסוד לפי הצורך שלך | עומרי |
| `deep-research` | מחקר מעמיק על נושא — מקורות, ניתוח, סיכום מובנה | עומרי |

---

## איך מתקינים ומשתמשים בסקיל ב-Claude Code

### התקנה — שיטה 1: npx (הכי פשוטה)

פתח טרמינל בתיקיית הפרויקט שלך והרץ:

```bash
npx skills add [שם-הסקיל]
```

לדוגמה:

```bash
npx skills add israeli-accessibility-compliance
npx skills add copywriting
npx skills add landing-page-design
```

הסקיל יתווסף אוטומטית לפרויקט.

### התקנה — שיטה 2: מ-Claude Code עצמו

בתוך שיחה ב-Claude Code אפשר לכתוב:

```
/skills add [שם-הסקיל]
```

### שימוש בסקיל

לאחר ההתקנה, פשוט ציין את הסקיל בפרומפט שלך:

```
בנה לי דף נחיתה. השתמש ב-skill: landing-page-design ו-israeli-accessibility-compliance
```

Claude Code יטעין את הסקיל וימלא אחרי ההנחיות שלו.

### עצה מעשית

הוסף את הסקילים הנפוצים ביותר שלך ישירות ל-**CLAUDE.md** של הפרויקט, כך שהם תמיד פעילים:

```markdown
## Skills פעילים
- israeli-accessibility-compliance
- hebrew-rtl-best-practices
- copywriting
```

כך כל פרומפט בפרויקט ייהנה מהם אוטומטית, בלי לציין בכל פעם.

### גילוי סקילים חדשים

כדי לגלות מה עוד קיים, הרץ:

```bash
npx skills find [נושא]
```

לדוגמה: `npx skills find animation` יחזיר את כל הסקילים הקשורים לאנימציה.

או השתמש ב-skill `find-skills` ישירות בתוך Claude Code.
