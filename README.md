# SAP Business One HANA Reporting Library

A structured portfolio library of reusable SAP Business One HANA SQL reporting patterns.

## Status

**Ongoing portfolio project.** Queries should be validated in a non-production environment and adjusted for the target SAP B1 version, localization and custom fields.

## Planned Report Categories

- Purchasing: PR, PO, GRPO, A/P Invoice and open commitments
- Sales: Sales Order, Delivery, A/R Invoice and open deliveries
- Inventory: stock by warehouse, batch/serial information and inventory audit support
- Finance: customer/vendor outstanding, journal impact and document reconciliation
- Production: BOM, Production Order, component issue and finished-goods receipt
- Service: open service calls and response tracking

## Query Standards

- SAP HANA quoted identifiers
- Clear table aliases
- Parameterized date, branch and business-partner filters
- Explicit document-status logic
- Canceled-document handling
- Comments explaining joins and business assumptions

## Suggested Structure

queries/
  purchasing/
  sales/
  inventory/
  finance/
  production/
  service/
docs/
  data-dictionary.md
  validation-checklist.md

## Validation Checklist

1. Compare totals with the SAP B1 standard report.
2. Check canceled, closed and partially open documents.
3. Test multi-branch and multi-currency scenarios.
4. Validate quantities and values independently.
5. Confirm performance before production use.

## Data Protection

Publish only generic SQL patterns. Remove company schemas, server names, credentials and proprietary UDF names unless replaced with safe examples.
