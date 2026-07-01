# How to update My Picks

Your Picks page is now connected to your Google Sheet (**My_Picks**). You edit the
sheet, and the website updates itself within a few minutes. You do not touch code.

---

## To add, change, or remove a product

Do it all in the Google Sheet, in the tab for that store (Daraz, Amazon, etc.):

- **Add**: add a new row and fill the columns (see below).
- **Change**: edit any cell.
- **Remove**: delete the row.
- **Reorder**: drag rows.

Save happens automatically. The website picks up the change on its own (Google
refreshes the published data roughly every 5 minutes).

### The columns

| Column       | What to put                                                          |
|--------------|----------------------------------------------------------------------|
| `Image`      | A link to the product photo (right click the Daraz photo, Copy image address), or a file name if you uploaded a photo to `assets/img/affiliates/`. Leave empty and a soft placeholder is shown. |
| `Name`       | The product name (card title)                                        |
| `Subtitle`   | A short line under the name (optional)                               |
| `Description`| One or two lines on why you love it (optional)                       |
| `Category`   | Pick from the dropdown. Categories become the sub-menu tabs.         |
| `Link`       | The product / affiliate link                                         |

---

## To add a whole new store (Daraz, Amazon, AliExpress, Other)

This is the only time you touch the website file, and only once per store.

1. In Google Sheets: **File → Share → Publish to web**, choose that store's tab,
   choose **Comma-separated values (.csv)**, and click **Publish**. Copy the link.
2. Open `affiliates/index.html`, find the `SHEETS` list near the bottom, and add a
   line with the store name and the link, for example:

       { store:"Amazon", csv:"PASTE_THE_LINK_HERE" },

3. Save. That store's products now appear, with its own colour and buy button.

---

## A note on previewing

The page reads your products live from Google. When the site is **live on your domain
(https)**, this works perfectly. If you open the file straight from your computer by
double clicking it, your browser may block it from reading remote data (a security
rule for local files), so the products may not show. That is normal and only happens
in local preview. Once published to GitHub Pages, it loads correctly.

---

That is the whole system: live products from your sheet, edited from anywhere,
including your phone.
