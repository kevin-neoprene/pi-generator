# PI / CI / Packing List / Quotation Generator — Tianchi Technology Co., Ltd.

Single-file document generator. Open index.html in a browser, pick the
document type (Proforma Invoice, Commercial Invoice, Packing List or
Quotation), fill in buyer / products / extras, and download Excel (.xlsx), PDF (via print)
or Word (.doc). No server, no account needed. Excel export uses ExcelJS from CDN;
import of existing PI / CI / Packing List / Quotation files (.xls / .xlsx / .pdf) uses SheetJS from CDN for Excel and PDF.js from CDN for PDF (text is read back into the table grid by position).

- Import: click "导入 PI / CI / 装箱单 / 报价单" and pick an existing .xls / .xlsx / .pdf file —
  buyer, products, extras, dates and ref are read from the file and filled in
  automatically, so the same data can be re-issued as PI, CI, Packing List or Quotation.
- Company header is editable: company name, email, web, tel, fax, cel, address and
  FM contact can be changed in the form (a preset list offers both Tianchi
  Technology Co., Ltd. and Hunan Tianchi Polymer New Material Co., Ltd.).

- Proforma Invoice: terms, bank block (HK / US / custom), remarks.
- Commercial Invoice: same layout and totals, no terms or bank block, free Note line.
- Packing List: cartons, net/gross weight and dimensions per product, with totals.
- Quotation: same Tianchi layout as QUOTATION_Tianchi.xlsx (Customer / Contact / Project / Quote No. / Valid Until, SUB TOTAL / Freight / TOTAL, EXW / USD / TT terms, no bank block, no tax), plus a price calculator for neoprene sheets: pick the rubber type, total thickness and the two fabric faces and it computes the RMB cost (rubber ¥/mm × (thickness − 0.5) + fabric A + fabric B + lamination × 2, from the supplier's rate card) and converts it to a USD EXW unit price (RMB ÷ exchange rate, default 6.6, plus markup %). The RMB cost is shown only in the calculator, never on the customer-facing quotation. The supplier rate card is editable and saved in the browser.

Logo: transparent TC logo, top-right of the header, at email/Tel height.
