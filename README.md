# REV_AUTOPO

REV Job Pricer: a web tool for sales reps to price a job and copy the PO line item notes. It replaces the "Refresh PO" step in the REV Home Rep Facing Workbook and runs in any tablet, phone or computer browser.

## Files

- `index.html` is the whole tool.
- `prices.json` is the current price list. The tool loads it every time it opens.
- `jspdf.umd.min.js` is the jsPDF library (MIT license) that makes the PO / Invoice PDF.
- `photos/` holds the product photos taken from the product catalog.
- `photos.json` pairs photos with items by tab, section heading or description, so new items in an existing family pick up the photo automatically.

## Updating prices

1. Open the tool and choose **Update price list**.
2. Choose the newest pricing workbook (.xlsx). Check the summary of what changed, then choose **Download prices.json**.
3. In this repository choose **Add file > Upload files**, drop in `prices.json`, and choose **Commit changes**.

Reps get the new prices the next time they open the tool, usually within a few minutes.

The workbook needs the same layout as today: each product tab has Price (or Cost) in cell B1 and a "sub cost" row at the bottom. Markup, sales tax and the three offer levels are read from the workbook too.

## Turning on the site

Settings > Pages > Deploy from a branch > `main`, folder `/ (root)`.
