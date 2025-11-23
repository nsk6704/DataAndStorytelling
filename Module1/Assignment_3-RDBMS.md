# **Information Required for a Relational Model (Construction Company)**

## **1. Core Entities (Tables)**

Identify the main objects the company works with:

* **Projects**
* **Clients**
* **Employees / Workers**
* **Materials**
* **Vendors / Suppliers**
* **Equipment / Machinery**
* **Sites / Locations**
* **Payments / Billing**
* **Contracts**
* **Tasks / Activities**


## **2. Attributes for Each Entity**

List what information each table stores.

### **Projects**

* Project_ID
* Name
* Start_date
* End_date
* Budget
* Status
* Client_ID *(foreign key)*

### **Employees**

* Employee_ID
* Name
* Role
* Salary
* Skill_level
* Assigned_Project_ID *(foreign key)*

### **Materials**

* Material_ID
* Name
* Cost_per_unit
* Vendor_ID *(foreign key)*
* Quantity_available


## **3. Relationships**

Determine how tables connect:

* **Client → Project**: One-to-Many
* **Project ↔ Employee**: Many-to-Many *(via assignment table)*
* **Project ↔ Material**: Many-to-Many *(via material usage table)*
* **Vendor → Materials**: One-to-Many
* **Project → Payments**: One-to-Many
* **Project → Tasks**: One-to-Many


## **4. Constraints**

Rules the database must enforce:

* **Primary Keys** (unique identifiers)
* **Foreign Keys** (linking related tables)
* **Not Null** constraints (mandatory fields like project name)
* **Check** constraints *(e.g., Budget > 0)*
* **Unique** constraints *(e.g., PAN, phone numbers)*


## **5. Business Rules**

Shape how the relational structure works:

* One project belongs to one client.
* An employee may work on multiple projects.
* Materials must be purchased only from approved vendors.
* Each payment belongs to a single project.
* A project must have at least one task.


## **6. Processes to Capture**

Understanding workflows helps build the tables:

* Project planning
* Material purchase
* Work allocation
* Attendance and payroll
* Equipment usage logging
* Vendor billing
* Site inspections and reports


