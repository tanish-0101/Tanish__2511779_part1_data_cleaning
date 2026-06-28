# Data Cleaning Log

## Issues Found

-   Extra spaces and inconsistent text formatting
-   Missing values in Region, Ship Mode and Discount
-   Duplicate records and duplicate Order IDs
-   Invalid discounts and date inconsistencies
-   Ship dates earlier than Order dates in some records

## Cleaning Actions Performed

-   Standardized text fields
-   Trimmed extra spaces
-   Filled missing Region and Ship Mode with `Unknown`
-   Treated blank discounts as 0 where appropriate
-   Flagged invalid discounts
-   Standardized date formats
-   Added calculated columns
-   Flagged records with data quality issues

## Business Rules Applied

-   Missing Region → Unknown
-   Missing Ship Mode → Unknown
-   Blank Discount → 0 (when valid)
-   Cancelled and failed payment orders excluded from completed sales
    analysis
-   Refunded orders summarized separately
-   Invalid shipping dates flagged

## Assumptions

-   Unknown values were retained instead of deleting records.
-   Invalid records were flagged for review.

## Records Removed

No records were deleted without review.

## Records Flagged

Records with duplicate IDs, invalid discounts, or date issues were
flagged.

## Limitations

Cleaning was performed using only the provided dataset.
