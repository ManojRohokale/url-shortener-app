# URL Shortener 🔗

A full-stack URL shortener application that allows users to create shortened URLs and manage them through an admin dashboard. Built with React frontend and Node.js backend.

## ✨ Features

- **URL Shortening**: Convert long URLs into short, shareable links
- **Admin Dashboard**: Manage and view all shortened URLs
- **Clean Interface**: User-friendly design for easy navigation
- **Real-time Updates**: Instant URL generation and management
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🏗️ Project Structure

```
├── backend/                 # Node.js Express server
│   ├── models/             # Database models
│   │   └── url.js         # URL model schema
│   ├── routes/            # API route handlers
│   │   └── url.js        # URL-related endpoints
│   ├── server.js         # Server entry point
│   ├── package.json      # Backend dependencies
│   └── package-lock.json
└── frontend/               # React application
    ├── src/               # Source code
    │   ├── components/   # React components
    │   │   ├── Admin.js # Admin dashboard
    │   │   └── Admin.css
    │   ├── App.js       # Main app component
    │   ├── App.css      # App styles
    │   ├── index.js     # React entry point
    │   └── index.css    # Global styles
    ├── public/           # Static assets
    │   ├── index.html
    │   ├── manifest.json
    │   └── robots.txt
    ├── package.json     # Frontend dependencies
    └── package-lock.json
```

## 🚀 Getting Started

### Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)
- **Git** - [Download here](https://git-scm.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/url-shortener.git
   cd url-shortener
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

### 🏃‍♂️ Running the Application

The application requires both frontend and backend servers to be running simultaneously.

#### Method 1: Using Two Terminal Windows/Tabs

**Terminal 1 - Backend Server:**
```bash
cd backend
npm start
```
The backend server will start on `http://localhost:5000` (or your configured port)

**Terminal 2 - Frontend Server:**
```bash
cd frontend
npm start
```
The frontend application will open automatically in your browser at `http://localhost:3000`

#### Method 2: Using Terminal Splitting (if supported)

If your terminal supports splitting or you're using an IDE:
- Split your terminal into two panes
- Run backend in one pane: `cd backend && npm start`
- Run frontend in the other pane: `cd frontend && npm start`

### 📱 Accessing the Application

Once both servers are running:

- **Main Application**: http://localhost:3000
- **Admin Dashboard**: http://localhost:3000/admin (if applicable)
- **API Endpoints**: http://localhost:5000/api

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the backend directory for environment-specific configurations:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
BASE_URL=http://localhost:5000
```

### Database Setup

If using MongoDB:
1. Install MongoDB locally or use MongoDB Atlas
2. Update the connection string in your configuration
3. The application will create necessary collections automatically

## 🎯 Usage

1. **Creating Short URLs**:
   - Enter a long URL in the input field
   - Click "Shorten" button
   - Copy and share the generated short URL

2. **Admin Dashboard**:
   - Access the admin panel to view all URLs
   - Monitor click statistics and manage URLs
   - Delete or modify existing short URLs

## 🛠️ Technologies Used

### Frontend
- **React** - UI library
- **CSS3** - Styling
- **JavaScript (ES6+)** - Programming language

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** (if applicable) - Database
- **Mongoose** (if applicable) - ODM

## 📝 API Endpoints

- `POST /api/urls` - Create a new short URL
- `GET /api/urls` - Retrieve all URLs
- `GET /api/urls/:id` - Get specific URL
- `DELETE /api/urls/:id` - Delete a URL
- `GET /:shortUrl` - Redirect to original URL

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Troubleshooting

### Common Issues

1. **Port already in use**:
   - Change the port in your configuration
   - Kill existing processes: `lsof -ti:3000 | xargs kill -9`

2. **Module not found errors**:
   - Delete `node_modules` and `package-lock.json`
   - Run `npm install` again

3. **CORS issues**:
   - Ensure backend is configured to accept requests from frontend origin

4. **Database connection issues**:
   - Verify database is running
   - Check connection string in environment variables
---

**Happy URL Shortening!** 🎉
