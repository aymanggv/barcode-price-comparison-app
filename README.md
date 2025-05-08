# 📱 Pricezilla – A Bar-code Based Price Comparison App

**A Final Year Individual Project**  
**Author:** Ayman (MISIS: M00649153)  
**Institution:** Middlesex University Dubai  
**Module:** CST3515 – Embedded Linux System and Application Development

---

## 📖 Overview

Pricezilla is a barcode-based price comparison Android app designed to help users compare product prices across local and supermarket retailers in the UAE. With integrated barcode scanning, Google Maps links, and nutritional info retrieval, it aims to empower budget-conscious consumers, students, the elderly, and the unemployed to make smarter, quicker, and more economical purchasing decisions.

---

## 🎯 Features

- 🔍 **Barcode Scanning** – Quickly scan product barcodes using the camera.
- 🏷️ **Price Comparison** – Instantly compare prices of products across multiple stores.
- 🗺️ **Store Locator** – Find the nearest store via integrated Google Maps links.
- 🧾 **Nutritional Info** – View nutritional facts for scanned food items.
- 📝 **Product Entry** – Users can manually add missing products to the database.
- 🔄 **Real-Time Database** – Powered by Firebase Firestore for live updates and data retrieval.

---

## 💡 Motivation

Consumers often overpay due to lack of access to real-time price data across various stores. Most existing apps do not:

- Cover local UAE grocery stores
- Offer barcode scanning for localized products
- Enable adding new product data
- Provide intuitive navigation or design

**Pricezilla** bridges this gap with a localized and user-friendly solution.

---

## 🛠️ Tech Stack

| Category           | Tools & Libraries                        |
|--------------------|------------------------------------------|
| Platform           | Android (Java, XML via Android Studio)   |
| Backend/Database   | Firebase Firestore (Real-time DB)        |
| Barcode Processing | Firebase ML Kit Vision                   |
| UI Design          | draw.io for mockups, XML for layout      |
| IDE                | Android Studio                           |

---

## 🗂️ Project Structure
```
├── app/
│ ├── src/
│ │ ├── main/
│ │ │ ├── java/
│ │ │ │ ├── com/
│ │ │ │ │ └── pricezilla/
│ │ │ │ ├── MainActivity.java
│ │ │ │ ├── Product.java
│ │ │ │ ├── Details.java
│ │ │ │ ├── ProductUtil.java
│ │ │ │ ├── ProductBaseActivity.java
│ │ │ │ ├── ProductAdditionActivity.java
│ │ │ │ ├── ProductReaderActivity.java
│ │ │ │ ├── ProductDetails.java
│ │ │ │ └── SplashActivity.java
│ │ │ └── res/
│ │ │ ├── layout/
│ │ │ │ ├── activity_main.xml
│ │ │ │ ├── product_addition.xml
│ │ │ │ ├── product_reader.xml
│ │ │ │ ├── product_details.xml
│ │ │ │ └── splash_activity.xml
│ │ │ └── drawable/ (images/icons)
│ ├── build.gradle
├── .gitignore
├── README.md
└── thesis/
└── Individual project report.pdf
```

## 🖥️ App Architecture

```plaintext
User ↔ Android App ↔ Firestore DB
     ↕              ↕
 Camera         Firebase ML Kit
```

- App scans barcodes via camera and Firebase ML Kit
- Barcode number is used to query product info in Firestore
- Results (price, stores, nutritional facts) are shown in-app
- Google Maps links assist in store navigation
