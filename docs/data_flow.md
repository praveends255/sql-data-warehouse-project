# Data Flow Table

This table describes how data flows from source systems through Bronze, Silver, and Gold layers.

| **Source System** | **Source Object** | **Bronze Layer Object** | **Silver Layer Object** | **Gold Layer Object** |
|------------------|-------------------|------------------------|------------------------|----------------------|
| **CRM** | crm_sales_details | crm_sales_details (raw copy of CRM sales details) | crm_sales_details (cleaned & standardized) | fact_sales (aggregated sales facts for reporting) |
| CRM | crm_cust_info | crm_cust_info (raw CRM customer info) | crm_cust_info (cleansed & enriched) | dim_customers (business-ready customer dimension) |
| CRM | crm_prd_info | crm_prd_info (raw CRM product info) | crm_prd_info (cleansed & enriched) | dim_customers (customer dimension joined with product info if needed) |
| **ERP** | erp_cust_az12 | erp_cust_az12 (raw ERP customer data) | erp_cust_az12 (cleansed & standardized) | dim_products (business-ready product dimension) |
| ERP | erp_loc_a101 | erp_loc_a101 (raw ERP location data) | erp_loc_a101 (cleansed & standardized) | dim_products (business-ready product dimension with location mapping) |
| ERP | erp_px_cat_g1v2 | erp_px_cat_g1v2 (raw ERP product category) | erp_px_cat_g1v2 (cleansed & standardized) | dim_products (business-ready product dimension for categories) |

## Layer Definitions

- **Source System**: The operational system where the data originates (CRM, ERP, etc.).  
- **Bronze Layer Object**: Raw, unprocessed data from the source stored as-is for traceability.  
- **Silver Layer Object**: Cleaned, standardized, and integrated data prepared for analysis.  
- **Gold Layer Object**: Business-ready, curated data (facts and dimensions) optimized for reporting and analytics.
