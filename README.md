# SERVICE-NOW-
# Enforcing Mandatory Fields Using UI Policies and Migrating Changes with Update Sets

## 📌 Overview

This project demonstrates how to enforce mandatory fields dynamically using UI Policies and how to migrate those configurations across environments using Update Sets. It is particularly useful in platforms like ServiceNow for maintaining consistency, improving data quality, and managing configuration changes efficiently.

---

## 🎯 Objectives

* Enforce mandatory fields based on conditions using UI Policies
* Avoid scripting where possible by leveraging declarative configurations
* Capture and migrate changes using Update Sets
* Ensure smooth deployment across development, test, and production environments

---

## 🛠️ Technologies Used

* ServiceNow Platform
* UI Policies
* Update Sets

---

## 📂 Features

### 1. UI Policy for Mandatory Fields

UI Policies allow you to dynamically control form behavior without writing scripts.

#### Key Capabilities:

* Make fields mandatory
* Show or hide fields
* Make fields read-only

#### Example Use Case:

When a user selects **"High Priority"**, additional fields such as *Justification* become mandatory.

#### Steps:

1. Navigate to **UI Policies**
2. Click **New**
3. Configure:

   * Table
   * Conditions (e.g., Priority = High)
4. Add **UI Policy Actions**

   * Set fields to *Mandatory = True*

---

### 2. Using Update Sets for Migration

Update Sets help track and move configuration changes between instances.

#### Steps to Create an Update Set:

1. Go to **Update Sets > Local Update Sets**
2. Click **New**
3. Provide:

   * Name
   * Description
4. Set it as **Current Update Set**

#### Capturing Changes:

* All UI Policy changes are automatically recorded in the active Update Set

#### Moving Update Sets:

1. Export Update Set as XML
2. Import into target instance
3. Preview Update Set
4. Resolve conflicts (if any)
5. Commit Update Set

---

## 🔄 Workflow Summary

1. Create UI Policy
2. Configure mandatory fields
3. Test in development instance
4. Capture changes in Update Set
5. Move Update Set to higher environments
6. Validate and commit

---

## ⚠️ Best Practices

* Always test UI Policies in a development instance
* Use meaningful names for Update Sets
* Avoid large Update Sets; keep them modular
* Preview Update Sets before committing
* Resolve conflicts carefully

---

## 🚀 Benefits

* Improves data accuracy
* Reduces need for client-side scripting
* Simplifies change management
* Ensures consistency across environments

---

## 📌 Conclusion

Using UI Policies to enforce mandatory fields simplifies form customization, while Update Sets provide a reliable way to migrate configurations. Together, they form a powerful approach for maintaining scalable and manageable system configurations.

---

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for improvements or additional use cases.

