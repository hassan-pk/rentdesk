# RentDesk business workflow

RentDesk is a single-computer offline pilot for equipment, tool, dress and other date-based rental businesses. Configure the business and owner first. It keeps its own database and backups.

## Modules

- **Customers:** contact/address records and notes.
- **Rental assets:** unique asset codes, category, rentable quantity, standard daily rate, asset photo and condition notes.
- **Rental bookings:** customer, asset, pickup/due dates, quantity, agreed days/rate, initial/final condition, rent/fees, rental collections and informational security deposit fields.
- **Maintenance:** dated service/inspection notes and cost for each asset.
- **Expenses:** operating costs recorded separately from rent collections.

## First working day

1. Enter customers and assets. For identical pooled items, set Total rentable quantity to the available pool. Use whole units; set quantity zero to block new bookings while the entire pool is out of service. For individually tracked items, create a separate asset record and capacity one.
2. Create a Rental booking with pickup and due dates and quantity. Overlapping active bookings may not exceed the selected asset's capacity.
3. Enter the agreed billable days and unit daily rate explicitly. The app calculates quantity ? rate ? days, then adds any manually entered late/damage fee. It does not infer the commercial billing policy from dates.
4. Enter only rental payments in Rental amount collected. Record a held security deposit separately in its informational field; it is excluded from rent collection totals and outstanding balance.
5. Print the booking, record the issue condition and move Reserved ? Issued.
6. On return, enter actual return date, inspection/damage notes, final fees and deposit-return state before marking Returned. Returned is terminal and releases booking capacity.
7. Collect any remaining rental balance, record expenses and keep an external backup.

## Capacity and dates

Availability is checked over inclusive pickup/due-return dates for active Reserved/Issued bookings. Returned/Cancelled records no longer reserve capacity. There is no hourly scheduling or automatic serial-number assignment. The app does not impose opening hours. A past due date is a record to review, not an automated penalty. Finalize future edits before marking Returned because terminal records cannot be edited.

Maintenance records do not automatically reduce availability. Adjust asset capacity and review existing reservations when taking units out of service. Capacity cannot be reduced below simultaneous existing reservations. The pilot cannot silently reallocate existing bookings for you.

## Deposits, charges and accounting

The security deposit fields are an informational custody record only. They do not add rent income, create a payment-ledger entry, calculate refunds or manage liability accounts. Reconcile received/returned deposits separately against actual cash or bank receipts. Do not put refundable deposits into the rental-paid field, because rental paid is bounded by the rent/fees total.

Billable days, agreed rates, late/damage fees and actual returns are manual. Maintenance cost is a service record; if recording its actual outflow in Expenses, avoid counting the same amount twice in an external accounting summary. This is not a full accounting/deposit-refund system.

## Current limits

No hourly rental rules, serial-to-reservation allocation, automated penalties, refundable-deposit ledger, refunds, tax accounting, digital contracts or customer signatures. One owner and one computer, without network synchronization. Keep independent backups and review overdue issued items manually.

This document describes the configured pilot and makes no claim of unperformed live-business or hardware tests. See repository verification notes for executed checks.
