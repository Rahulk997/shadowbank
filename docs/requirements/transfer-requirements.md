# Transfer Service — Business Requirements

## Purpose

The Transfer Service allows an authenticated customer to transfer
money from one active account to another active account.

## Initial Business Rules

1. The source account must exist.
2. The destination account must exist.
3. Both accounts must be active.
4. The transfer amount must be greater than zero.
5. The source account must have sufficient available balance.
6. The source and destination accounts must not be the same.
7. A duplicate request must not result in multiple debits.
8. Every successful transfer must have a unique transfer identifier.
9. Every transfer must have a status.
10. Failed transfers must return a clear error response.

## Initial Transfer Statuses

- PENDING
- COMPLETED
- FAILED

## Questions to Investigate

- Should transfer amount be represented as a number or string?
- Should currency be part of the transfer request?
- Who generates the transfer ID?
- Should the client provide an idempotency key?
- What HTTP status should a successful transfer return?
- What should happen when the same request is submitted twice?
- What information should be included in an error response?