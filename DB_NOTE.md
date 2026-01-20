# Track 3: The Evidence Locker - Project Documentation

## 1. How I Did It
* **Firebase Setup:** I began by creating a project in the Firebase Console. I provisioned a **Cloud Firestore** database and configured the security rules to **Test Mode**, allowing for immediate read/write access during development.
* **Schema Design:** I followed a NoSQL document-oriented approach. I initialized a collection named `evidence` and manually seeded it with two documents: `case_001` and `case_002`.
* **Data Fields:** Each document was assigned a `clue_type` (string), `is_verified` (boolean), and a `timestamp` (Firestore Timestamp object), along with custom test fields like `location`.
* **Front-End Integration:** I developed an HTML5 page utilizing the **Firebase JS SDK (v10)**. I used the `getDocs` function to fetch data in real-time and the `addDoc` function to enable CRUD (Create, Read, Update, Delete) functionality directly from the browser.

## 2. Screenshots
### Firestore Database Structure
![App Screenshot](![alt text](image2.png))
*Description: This screenshot shows the 'evidence' collection with documents case_001 and case_002.*

### Working Front-End Application
![App Screenshot](![alt text](image.png))
*Description: This screenshot shows the HTML interface successfully displaying the evidence records from the database.*

## 3. What is a NoSQL Database?
A **NoSQL (Not Only SQL)** database provides a mechanism for storage and retrieval of data that is modeled in means other than the tabular relations used in relational databases (SQL).

* **Flexible Schema:** Unlike traditional SQL databases that require a predefined table schema, NoSQL databases like Firestore allow each document to have a different set of fields. This is ideal for evidence where different cases may have different types of metadata.
* **Scalability:** NoSQL databases are built to be "distributed," meaning they can handle massive spikes in data traffic by adding more servers (horizontal scaling) rather than just making one server bigger (vertical scaling).
* **Document-Oriented:** Firestore specifically stores data as "Documents" (key-value pairs) organized into "Collections." This structure is very similar to JSON, making it easy for web developers to work with.