Book Store Web ApplicationA full-stack web application designed to manage a virtual bookstore. 
This project allows for the management of book inventories and the dynamic serving of media assets like book covers.
🚀 FeaturesBook Management: (Core CRUD functionality for adding, editing, and deleting books).
Dynamic File Serving: A dedicated FileController handles the retrieval of images (PNG, JPG, GIF, WebP) for the frontend.
Smart Storage Lookup: The system automatically checks a system-wide temporary directory (bookstore-uploads) and falls back to internal static resources if the file is not found.
Responsive Design: Optimized for web viewing with inline content disposition for media.
🛠️ Tech StackBackend: Java, Spring Boot (Spring MVC)Build Tool: Maven (indicated by the .project nature and structure)
Media Handling: FileSystemResource with dynamic MIME type detection.

📂 Project StructurePlaintextsrc/
├── main/
│   ├── java/
│   │   └── com/Anudip/FinalProject/
│   │       └── controller/
│   │           └── FileController.java   <-- Manages image uploads
│   └── resources/
│       └── static/
│           └── uploads/                 <-- Fallback storage for assets


⚙️ Installation & SetupClone the repository:Bashgit clone https://github.com/shivamdhondkar/Book-Store-Web.git
Configure Environment:Ensure your system has a temporary directory accessible to the Java Virtual Machine, as the application uses java.io.tmpdir to store and retrieve book uploads.
Run the Application:If using Maven:Bashmvn spring-boot:run
The server will typically start on http://localhost:9090 (as per your local environment).

📡 API Endpoints (File Management)MethodEndpointDescriptionGET/uploads/{folder}/{filename}Serves the requested image file from the bookstore storage.

Note: Supported file extensions for images include .png, .jpg, .jpeg, .gif, and .webp.
