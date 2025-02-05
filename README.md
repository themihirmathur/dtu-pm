# DTU-PM (DTU Project Manager) | Complete Project Management Dashboard

<p align="left">
  <img src="https://www.animatedimages.org/data/media/562/animated-line-image-0184.gif" width="1920" 
</p>

`DTU-PM` is a comprehensive project management dashboard designed to simplify project management tasks such as planning, tracking, and reporting. Built using modern web technologies and cloud services, it provides a robust platform for managing project data, resources, and collaboration. This application leverages Next.js for the frontend, Node.js with Express for the backend, and various AWS services to ensure scalability, security, and high availability.

![Screenshot 2024-09-13 at 5 48 08 PM](https://github.com/user-attachments/assets/40a2d0bc-c34a-4738-9887-a276626bdc44)

## Technology Stack

### Frontend
- **Next.js**: React-based framework for server-side rendering and static site generation.
- **Tailwind CSS**: Utility-first CSS framework for rapid UI development.
- **Redux Toolkit**: State management solution for managing complex state logic.
- **Redux Toolkit Query**: For managing API requests and caching.
- **Material UI Data Grid**: For displaying tabular data with sorting, filtering, and pagination.

### Backend
- **Node.js with Express**: Server-side framework for building RESTful APIs.
- **Prisma**: PostgreSQL ORM for managing database interactions.

### Database
- **PostgreSQL**: Relational database management system.
- **PgAdmin**: Open-source administration and management tool for PostgreSQL.

### Cloud Services (AWS)
- **AWS EC2**: For hosting the application.
- **AWS RDS**: Managed PostgreSQL database.
- **AWS API Gateway**: For creating and managing APIs.
- **AWS Amplify**: For continuous deployment and hosting.
- **AWS S3**: For storing static assets like images and documents.
- **AWS Lambda**: Serverless computing service for handling backend logic.
- **AWS Cognito**: User authentication and authorization.

![Screenshot 2024-09-13 at 5 48 38 PM](https://github.com/user-attachments/assets/ab5bed48-62f2-4a9d-83a9-3b2516fe52f1)

## Features

- **User Authentication and Authorization**: Secure user login, registration, and access management using AWS Cognito.
- **Project Management**: Create, update, delete, and manage projects and tasks.
- **Resource Allocation**: Efficiently manage and allocate resources.
- **Collaboration Tools**: Facilitate team communication and collaboration.
- **Data Visualization**: Visualize project progress with Gantt charts and other data visualization tools.
- **Real-time Updates**: Track changes and updates in real-time using WebSockets.
- **Cloud Storage Integration**: Seamless integration with AWS S3 for storing and retrieving files.

## Getting Started

### Prerequisites

Before running the application, ensure that you have the following tools installed on your local machine:

- [Git](https://git-scm.com/downloads)
- [Node.js](https://nodejs.org/) (includes npm)
- [PostgreSQL](https://www.postgresql.org/download/)
- [PgAdmin](https://www.pgadmin.org/download/)

### Installation Steps

1. **Clone the Repository**
    ```bash
    git clone https://github.com/themihirmathur/dtu-pm
    cd dtu-pm
    ```

2. **Install Dependencies**
   - For the client:
    ```bash
    cd client
    npm install
    cd ..
    ```
   - For the server:
    ```bash
    cd server
    npm install
    cd ..
    ```

3. **Set Up the Database**
    ```bash
    npx prisma generate
    npx prisma migrate dev --name init
    npm run seed
    ```

4. **Configure Environment Variables**
   - Create and configure `.env` for server settings:
    ```plaintext
    PORT=your_port_number
    DATABASE_URL=your_database_url
    ```
   - Create and configure `.env.local` for client settings:
    ```plaintext
    NEXT_PUBLIC_API_BASE_URL=your_api_base_url
    ```

5. **Run the Project**
    ```bash
    npm run dev
    ```

## Project Structure

```
project-management/
│
├── client/                   # Frontend code
│   ├── pages/                # Next.js pages
│   ├── components/           # Reusable React components
│   ├── store/                # Redux Toolkit configuration
│   ├── public/               # Public assets (images, icons, etc.)
│   └── styles/               # Tailwind CSS and global styles
│
├── server/                   # Backend code
│   ├── prisma/               # Prisma ORM configurations
│   ├── controllers/          # Express route controllers
│   ├── models/               # Database models
│   └── routes/               # Express routes
│
└── README.md                 # Project documentation
```

## Additional Resources

- **Code Repositories and Configuration Files:**
  - Complete project code on [GitHub](https://github.com/themihirmathur/dtu-pm)
  - Tailwind CSS configuration
  - Redux Toolkit setup
  - Database seed files
  - Image files for UI components
  - `globals.css` file for Gantt charts

- **Diagrams and Models:**
  - Data model diagram
  - AWS architecture diagram
  - AWS Cognito flow diagram

## AWS Deployment Guide

1. **AWS EC2 Configuration**: Set up an EC2 instance to host the application. Follow the AWS documentation for instance creation, security group setup, and SSH access.
2. **AWS RDS Configuration**: Create and configure an RDS PostgreSQL instance for the application database.
3. **AWS S3 Configuration**: Set up an S3 bucket for storing static assets and enable CORS to allow access from the frontend.
4. **AWS Cognito Configuration**: Create a user pool and identity pool for managing authentication and authorization.
5. **AWS Lambda Functions**: Deploy backend functions for serverless tasks such as notifications and file processing.

![Screenshot 2024-09-13 at 5 48 26 PM](https://github.com/user-attachments/assets/299b220a-4317-4d55-acc6-5a890f3262da)

## Database Management Commands

To reset the ID in a table:
```sql
SELECT setval(pg_get_serial_sequence('"[DATA_MODEL_NAME_HERE]"', 'id'), coalesce(max(id)+1, 1), false) FROM "[DATA_MODEL_NAME_HERE]";
```

## Contributing

We welcome contributions from the community. To contribute, please fork the repository and submit a pull request. Ensure that your code follows the project’s coding standards and includes proper documentation.

## Contact

For questions or feedback, please reach out to [Mihir Mathur](mailto:themihirmathur@gmail.com).

---

By providing a detailed overview, this README helps developers and users understand the purpose, setup, and usage of the DTU Project Manager, making it easier to contribute to or deploy the application.

<p align="left">
  <img src="https://www.animatedimages.org/data/media/562/animated-line-image-0184.gif" width="1920" 
</p>
