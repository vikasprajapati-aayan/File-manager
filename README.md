PHP File Manager with Admin Panel

A web-based file manager built with vanilla HTML/CSS/JS on the frontend and PHP + MySQL on the backend. Users can create nested folders, upload files, and organize their data with a familiar Explorer-style interface. A separate admin panel gives administrators user management and a read-only, cross-user view of the entire folder structure.

Features:-

File Manager (User Dashboard):-

Nested folder creation with unlimited depth (self-referencing parent_id structure)
File upload (single and multiple), with type and size validation
Grid view and List view (Name, Date modified, Type, Size) with one click toggle
Breadcrumb navigation resolved from the folder hierarchy
Global search across all folders and files with a dropdown of results and direct navigation
Right-click context menu: Copy, Paste, Move to, Rename, Delete
Move to — nested folder tree picker, with automatic exclusion of a folder's own descendants to prevent circular references
Duplicate name handling on create/rename (auto-suffixes (1), (2), etc.), enforced server-side
File preview/open served through a permission-checked PHP endpoint (no direct public file URLs) 

Admin Panel:- 

User management: view, add, edit, delete users
Role-based access — Admin (1), Subadmin (2), Normal user (3); only Admins can perform write actions, others get a read-only view
Status control — Active / Inactive accounts
Folder management — read-only, paginated drill-down view of every user's folders and files, joined with the owning user's name
All destructive/write actions are re-validated server-side regardless of what the frontend sends
Tech Stack
Frontend: HTML5, CSS3 (custom properties, no framework), vanilla JavaScript (no build step)
Backend: PHP (PDO for database access)
Database: MySQL / MariaDB
