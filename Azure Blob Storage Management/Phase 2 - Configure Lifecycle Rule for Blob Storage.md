## 🛠️ Add a Lifecycle Policy to the img Folder

- At the top breadcrumb, click Storage accounts to return to the storage account dashboard
- In the left navigation, select Lifecycle Management
- Click + Add a rule

## 🔧 Rule Configuration – Step 1
- Setting	Value
- Rule name	30days
- Rule scope	Limit blobs with filters
- Blob type	Block blobs
- Blob subtype	Base blobs
- Click Next

## 🔧 Rule Configuration – Step 2
- Setting	Value
- More than (days ago)	30
- Then	Delete the blob
- Click Next

33 🔧 Rule Configuration – Step 3: Prefix Filter

- Under Prefix match, enter:

holidaysale/img/

Click Add to create the rule.

## ✅ 4. Verify the Lifecycle Rule

1. On the Lifecycle Management page, locate the rule named 30days

2. Click it to review and confirm the configuration
