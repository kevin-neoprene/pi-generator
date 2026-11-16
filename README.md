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
- Quotation: same Tianchi layout as QUOTATION_Tianchi.xlsx (Customer / Contact / Project / Quote No. / Valid Until, SUB TOTAL / Freight / TOTAL, EXW / USD / TT terms, no bank block, no tax), plus a price calculator for neoprene sheets. The calculator prices the SHEET (raw material) and the product table prices the FINISHED product — they are separate: a calc line only computes a USD/sheet price, and "→ 产品" copies that price into a product row while the finished-product name stays the user's own text. Cost = rubber ¥/mm × (thickness − fabric+glue) + fabric faces + lamination × faces; fabric+glue is ~0.25mm per laminated face (0.5 double-sided, 0.25 single-sided). Lamination can be single-sided or double-sided (price differs). Fabric is free text — any fabric may be entered with its own ¥/face price, not only the rate-card presets. The rubber hardness (e.g. 9°) is not written into the product description; it belongs in the Special Notes. The RMB cost is shown only in the calculator, never on the customer-facing quotation. The supplier rate card is editable and saved in the browser.

Logo: transparent TC logo, top-right of the header, at email/Tel height.
