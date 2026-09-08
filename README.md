# מגמות גושיות – עמוד אינטראקטיבי

עמוד HTML עצמאי (ללא תלות בשרת) המציג את מגמות הגושים הפוליטיים לפי סקרים, עם אפשרות מעבר בין שני תרשימים, מצב עמודות/קווים, לג'נדה אינטראקטיבית וקישור להורדת המצגת המקורית.

## פרסום ב-GitHub Pages

1. צרו ריפו חדש ב-GitHub (ציבורי, כדי ש-Pages יעבוד בחינם).
2. העלו את כל הקבצים בתיקייה הזו (`index.html`, `.nojekyll`) לריפו — לדוגמה מהטרמינל:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```

3. בריפו ב-GitHub: **Settings → Pages**.
4. תחת **Build and deployment**, בחרו **Source: Deploy from a branch**.
5. בחרו **Branch: main**, תיקייה **/ (root)**, ולחצו **Save**.
6. אחרי דקה-שתיים העמוד יהיה זמין בכתובת:
   `https://<username>.github.io/<repo-name>/`

## הערות

- הקובץ `index.html` הוא עצמאי לחלוטין — הגרפים (Chart.js) והפונט (Heebo) נטענים מ-CDN, והמצגת המקורית (PPTX) מוטמעת בתוכו כ-base64 להורדה ישירה מהעמוד, כך שאין צורך בקבצים נוספים.
- הקובץ `.nojekyll` מונע מ-GitHub Pages להריץ עיבוד Jekyll על הקובץ (לא הכרחי כאן, אבל מונע בעיות עתידיות אם יתווספו קבצים שמתחילים ב-`_`).
- אם תרצו כתובת מותאמת אישית (דומיין פרטי), אפשר להוסיף קובץ `CNAME` עם הדומיין, ולהגדיר אותו גם אצל ספק הדומיין.
