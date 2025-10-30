# Ticket Booking - CRUD Application

A comprehensive Node.js application for managing ticket bookings using Mongoose and MongoDB. This project demonstrates fundamental CRUD (Create, Read, Update, Delete) operations with proper data validation and error handling.

## Objective

The primary objective of this project is to learn and implement basic CRUD operations on a MongoDB collection using Mongoose in Node.js. This application helps you understand:

- Schema design and data modeling
- Database connectivity using Mongoose
- Implementing RESTful API endpoints for CRUD operations
- Data validation and error handling
- Best practices in Node.js application development

## Features

- **Create**: Add new ticket bookings to the database
- **Read**: Retrieve all bookings or fetch specific bookings by ID
- **Update**: Modify existing ticket booking details
- **Delete**: Remove ticket bookings from the database
- **Data Validation**: Ensure data integrity with Mongoose schema validation
- **Error Handling**: Comprehensive error handling for all operations
- **RESTful API**: Clean and intuitive API endpoints for all operations

## Installation

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or MongoDB Atlas connection)
- npm or yarn package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/RajAstha1/ticket-booking.git
   cd ticket-booking
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   Create a `.env` file in the root directory:
   ```
   MONGODB_URI=mongodb://localhost:27017/ticket_booking
   PORT=5000
   NODE_ENV=development
   ```

4. **Start the application**
   ```bash
   npm start
   ```

   The server will run on `http://localhost:5000`

## Usage

### API Endpoints

#### 1. Create a New Booking
- **POST** `/api/bookings`
- Request body:
  ```json
  {
    "customerName": "John Doe",
    "ticketType": "Premium",
    "quantity": 2,
    "price": 500,
    "eventDate": "2025-12-15"
  }
  ```

#### 2. Get All Bookings
- **GET** `/api/bookings`
- Returns all bookings in the database

#### 3. Get Booking by ID
- **GET** `/api/bookings/:id`
- Returns a specific booking by its ID

#### 4. Update a Booking
- **PUT** `/api/bookings/:id`
- Request body (same format as Create)

#### 5. Delete a Booking
- **DELETE** `/api/bookings/:id`
- Removes the booking from the database

## Project Structure

```
ticket-booking/
├── models/
│   └── Booking.js          # Mongoose schema and model
├── routes/
│   └── bookings.js         # API route definitions
├── controllers/
│   └── bookingController.js # Business logic for CRUD operations
├── middleware/
│   └── errorHandler.js     # Error handling middleware
├── .env                     # Environment variables
├── server.js               # Main application entry point
├── package.json            # Project dependencies
└── README.md               # Project documentation
```

## Technologies Used

- **Node.js**: JavaScript runtime environment
- **Express.js**: Web application framework
- **MongoDB**: NoSQL database
- **Mongoose**: MongoDB object modeling tool
- **dotenv**: Environment variable management

## Learning Outcomes

After completing this project, you will have a solid understanding of:

- How to design database schemas using Mongoose
- Implementing RESTful APIs with Express.js
- CRUD operations in Node.js
- Error handling and data validation
- Working with MongoDB and object-relational mapping

## Contributing

Contributions are welcome! Feel free to fork this repository and submit pull requests with improvements.

## License

This project is open-source and available under the MIT License.

## Support

For any questions or issues, please open an issue on the GitHub repository.
