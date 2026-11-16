# PI / CI / Packing List Generator — Tianchi Technology Co., Ltd.

Single-file document generator. Open index.html in a browser, pick the
document type (Proforma Invoice, Commercial Invoice or Packing List),
fill in buyer / products / extras, and download Excel (.xlsx), PDF (via print)
or Word (.doc). No server, no account needed. Excel export uses ExcelJS from CDN;
import of existing PI / CI / Packing List files (.xls / .xlsx / .pdf) uses SheetJS from CDN for Excel and PDF.js from CDN for PDF (text is read back into the table grid by position).

- Import: click "导入 PI / CI / 装箱单" and pick an existing .xls / .xlsx / .pdf file —
  buyer, products, extras, dates and ref are read from the file and filled in
  automatically, so the same data can be re-issued as PI, CI or Packing List.
- Company header is editable: company name, email, web, tel, fax, cel, address and
  FM contact can be changed in the form (a preset list offers both Tianchi
  Technology Co., Ltd. and Hunan Tianchi Polymer New Material Co., Ltd.).

- Proforma Invoice: terms, bank block (HK / US / custom), remarks.
- Commercial Invoice: same layout and totals, no terms or bank block, free Note line.
- Packing List: cartons, net/gross weight and dimensions per product, with totals.

Logo: transparent TC logo, top-right of the header, at email/Tel height.
