# 📊 MongoDB Data Modeling Practice: Optical Store (Óptica Cul d'Ampolla)

## 📌 Description

The objective of this project is to design a NoSQL data model using MongoDB based on a real-world business scenario.

An optical store ("Cul d'Ampolla") needs to manage clients, glasses purchases, and providers efficiently.  
The data model is built by analyzing a user interface and structuring the information to optimize read operations.

The focus is on applying MongoDB design principles such as document-oriented modeling, embedded documents, and arrays.

## 🛠 Technologies

- MongoDB (Compass)
- JSON
- Draw.io (for database diagram)

## 📂 Project Structure

MongoDB-estructura/

`opticaClienteUIData.json` → MongoDB document structure  
`opticaClienteUI.png` → Data model diagram  
`README.md` → Project documentation  

## 🧠 What was Practiced

### 🔹 NoSQL Data Modeling

- Designing a database based on application UI  
- Structuring documents instead of relational tables  
- Understanding document-oriented thinking
- 
### 🔹 Embedded Documents

- Use of nested objects for:
  - Address (cliente y proveedor)  
  - Glasses (gafas)  
  - Provider inside glasses
  - 
### 🔹 Arrays
- Implementation of arrays to represent:
  - Client purchases (`compras`)  

### 🔹 Relationships in MongoDB

- **1:N relationship using arrays**:
  - Cliente → Compras  

- **1:1 embedded relationships**:
  - Compras → Gafas  
  - Gafas → Proveedor  

### 🔹 Data Organization

- Grouping related data into a single document  
- Avoiding JOIN operations  
- Structuring data for fast read operations  

## 📈 Design Approach

The model follows a **UI-driven design approach**:

- Data shown together in the interface is stored together  
- Embedded documents reduce query complexity  
- Structure optimized for fast data retrieval  

## 🔗 Key Design Decisions

- ✅ One document per client  
- ✅ Purchases stored as an array  
- ✅ Glasses embedded within purchases  
- ✅ Provider embedded within glasses  
- ✅ No use of relational joins  
- ✅ Structure aligned with application view  

## 🚀 How to Use

1. Open MongoDB Compass  
2. Create database: `bottleBottomOptic`  
3. Create collection: `clients`  
4. Import file: `optica_clientes.json`  
5. Explore the data  

