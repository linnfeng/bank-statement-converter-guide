# Bank Statement Converter

Turn bank statement PDFs and photos into spreadsheet rows you can reconcile.

Most small-business bookkeeping does not fail on arithmetic. It fails on
transcription. A statement already exists as a PDF, and someone reads it carefully
and retypes 200 rows by hand. That is where a digit slips, a date shifts by a day,
and the closing balance no longer matches the figure the bank printed.

The practical fix is to remove the retyping step while keeping the checking step.
Those are two different jobs, and treating them as one is why people either trust
an extraction blindly or reject it out of habit.

## What it does

- Reads a PDF exported from online banking structurally, because it has a real text
  layer, and handles phone photos of printed pages.
- Exports to Excel for manual review, CSV for accounting imports and scripts, or
  JSON when rows merge with another source.
- Keeps transaction date, description, debit, credit and balance, plus currency and
  account identifier so one workbook cannot quietly mix two accounts.

## Why the closing balance matters

Take the last exported row and compare it against the printed closing balance.
Matching to the cent means the table is very likely right. A mismatch means find the
difference first, because every total below it inherits that error.

## Try it

[Bank Statement Converter](https://bank-statement-converter.online/) converts a
statement PDF or photo into Excel, CSV or JSON.

The habit matters more than the tool: a recurring slot, every account processed in
one sitting, and each balance reconciled before moving on.
