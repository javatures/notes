# Project 1
A Java 8 backend web API and ES6+ HTML/JS web interface with a PostgreSQL database. Submit a README.md with a proposal that matches as many requirements as manageable below. You may use the example proposal below for reference, or as your project itself.

### Tools & APIs
- [] Agile User Stories
- [] Java SE 8
- [] Gradle
- [] JDBC
- [] PostgreSQL
- [] JavaEE Servlet
- [] HTML/JS/CSS
- [] AJAX/Fetch
- [] JUnit
- [] log4j or similar
- [] Jest or similar JS testing framework
- [] Optional:
    - [] Docker, Docker-Compose
    - [] React
    - [] Bootstrap
    - [] Remote hosting (AWS EC2/RDS)
    - [] Jenkins CI automation
    - [] Mockito

### Architecture
- [] Anemic/DDD OR n-tier package & class structure
- [] Design Patterns:
    - [] Dependency Injection
    - [] Data Access Object
    - [] Business Delegate
    - [] Model-View-Controller
    - [] Front Controller
- [] SQL Normalization (3rd form)
- [] PL/pgSQL
- [] Optional:
    - [] Single Page Application

### Functionality
- [] CRUD - Create, Read, Update, Delete
- [] Web App dashboard interface
- [] Asynchronous interface updates
- [] Login - Authentication & Authorization
- [] Database persistance
- [] Session management

### Presentation
- [] Prepare a demonstration of functionality requirements through a browser
- [] Prepare visual aides (slides) introducing the project requirements and features

## Example: Expense Reimbursement System
A web application for managing reimbursement ticket submissions and approvals between employees and their managers.

### User stories
- An Employee...
    - [] can login
    - [] can view the Employee Homepage
    - [] can logout
    - [] can submit a reimbursement request
    - [] can upload an image of his/her receipt as part of the reimbursement request
    - [] can view their pending reimbursement requests
    - [] can view their resolved reimbursement requests
    - [] can view their information
    - [] can update their information
    - [] receives an email when one of their reimbursement requests is resolved (optional)

- A Manager...
    - [] can login
    - [] can view the Manager Homepage
    - [] can logout
    - [] can approve/deny pending reimbursement requests
    - [] can view all pending requests from all employees
    - [] can view images of the receipts from reimbursement requests
    - [] can view all resolved requests from all employees and see which manager resolved it
    - [] can view all Employees
    - [] can view reimbursement requests from a single Employee 
