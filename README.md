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
- Quotation: same Tianchi layout as QUOTATION_Tianchi.xlsx (Customer / Contact / Project / Quote No. / Valid Until, SUB TOTAL / Freight / TOTAL, EXW / USD / TT terms, no bank block, no tax), plus a price calculator for neoprene sheets. The calculator prices the SHEET (raw material) and the product table prices the FINISHED product — they are separate: a calc line only computes a USD/sheet price, and "→ 产品" copies that price into a product row while the finished-product name stays the user's own text. Cost = rubber ¥/mm × (thickness − fabric+glue) + fabric faces + lamination × faces; fabric+glue is ~0.25mm per laminated face (0.5 double-sided, 0.25 single-sided). The standard sheet size is 51" x 130" (inches, ~1.3 x 3.3 m); the size shown in a calc line is the sheet size as typed, in inches unless stated otherwise. Lamination can be single-sided or double-sided (price differs). Fabric is free text — any fabric may be entered with its own ¥/face price, not only the rate-card presets. Rubber (CR/SBR/SCR) and fabric prices float: they are editable both in the supplier rate card (the default for new lines) and per calc line (the ¥/mm and ¥/face boxes in the calc row — changing one only changes that line), and the totals recalculate immediately. The rubber hardness (e.g. 9°) is not written into the product description; it belongs in the Special Notes. The quotation template (RickQT sample: three sheet lines with their prices) and a blank quotation coexist as two one-click options: "Rick（报价单 · 算价示例）" loads the template, "空白报价单" starts a fresh blank quotation (empty buyer and product table, one default calc line, a fresh QT-YYMMDD-01 reference). The product table is shared across PI / CI / QT, so an old order can be re-issued as a different document type. The RMB cost is shown only in the calculator, never on the customer-facing quotation. The supplier rate card is editable and saved in the browser.

Logo: transparent TC logo, top-LEFT of the header for all document types. The header (company name, email/web, tel/fax/cel, address) is merged across the full width B:I, like the original sample PIs.

Bank block (PI only): the first line "Bank information: (TT PAYMENT)" is red; the account details (account name, account number, bank name, address, SWIFT/BIC, currency) and the Note line are black. Both lines are Arial 12 bold.

History: every PI / CI / PL / Quotation that is downloaded (Excel / Word) or printed is auto-saved to a history list in the browser (localStorage, this computer only, max 100 entries). The "历史记录" section at the top of the page lists them (type, customer, reference, date, total) with search, "载入" to reload one into the form as a template, "删除" per entry and "清空历史". Re-downloading the same reference updates its entry instead of duplicating it. A "保存当前到历史" button saves the current form without downloading.
