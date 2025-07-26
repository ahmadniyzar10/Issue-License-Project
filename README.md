# DCWP Issued Licenses Project
This dataset features licenses issued by the NYC Department of Consumer and Worker Protection (DCWP)—formerly the Department of Consumer Affairs (DCA).

## Data Source: NYC Issued Licenses

This dataset, retrieved from NYC Open Data, contains issued business licenses from the Department of Consumer and Worker Protection (DCWP). It includes metadata such as business name, license type, issue/expiry dates, and NYC location identifiers.

### Raw Schema (Preserved from Source)

| Column | Type | Notes |
|--------|------|-------|
| license_number | TEXT | Primary ID |
| business_name | TEXT | Legal name |
| DBA/Trade Name | TEXT | Trade Name" registered with the NYS Department of State. |
| Business_Unique_ID | TEXT | An identification number assigned by DCWP to track unique businesses across its systems |
| Business_Category | TEXT | The business activity or business category requiring a DCWP-issued license in order to operate legally within NYC. |
| License_Type | TEXT | Indicates whether the license is issued to an individual or an organization. |
| License_Status | TEXT | Indicates the current status of the license. |
| ... | ... | Full list in [`schema/raw_issued_licenses.sql`](./schema/raw_issued_licenses.sql) |
