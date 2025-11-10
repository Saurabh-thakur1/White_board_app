# Whiteboard Application

A collaborative real-time whiteboard application built with Node.js backend and React frontend. Users can draw, share boards, and collaborate in real-time.

## Features

- 🎨 **Real-time Drawing** - Draw on a shared whiteboard with instant synchronization
- 👥 **User Authentication** - Secure login and registration system
- 🤝 **Collaborative Drawing** - Multiple users can draw on the same board simultaneously
- 📱 **Responsive Design** - Works on desktop and tablet devices
- 🎯 **Drawing Tools** - Various tools including pen, eraser, shapes, and more
- 💾 **Canvas Management** - Save, load, and manage multiple canvases

## Project Structure

```
whiteboard_az/
├── backend/                 # Node.js Express server
│   ├── config/
│   │   └── db.js           # Database configuration
│   ├── controllers/        # Route controllers
│   │   ├── canvasController.js
│   │   └── userController.js
│   ├── middlewares/        # Express middlewares
│   │   └── authMiddleware.js
│   ├── models/             # Database models
│   │   ├── canvasModel.js
│   │   └── userModel.js
│   ├── routes/             # API routes
│   │   ├── canvasRoutes.js
│   │   └── userRoutes.js
│   ├── server.js           # Main server file
│   ├── package.json
│   └── vercel.json         # Vercel deployment config
│
└── frontend/               # React application
    ├── public/
    │   ├── index.html
    │   └── ...
    ├── src/
    │   ├── components/     # React components
    │   │   ├── Board/
    │   │   ├── Login/
    │   │   ├── Register/
    │   │   ├── Sidebar/
    │   │   ├── Toolbar/
    │   │   └── Toolbox/
    │   ├── store/          # Context & state management
    │   │   ├── board-context.js
    │   │   ├── BoardProvider.js
    │   │   ├── toolbox-context.js
    │   │   └── ToolboxProvider.js
    │   ├── utils/          # Utility functions
    │   │   ├── api.js
    │   │   ├── element.js
    │   │   ├── math.js
    │   │   └── socket.js
    │   ├── App.js
    │   ├── index.js
    │   └── index.css
    ├── package.json
    ├── tailwind.config.js
    └── README.md
```

## Tech Stack

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - Database (or your database)
- **Socket.io** - Real-time communication
- **JWT** - Authentication

### Frontend
- **React** - UI library
- **Tailwind CSS** - Styling
- **Socket.io Client** - Real-time updates
- **Context API** - State management

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Saurabh-thakur1/White_board_app.git
   cd whiteboard_az
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   
   # Create a .env file and configure your database
   # Example .env:
   # MONGODB_URI=your_mongodb_connection_string
   # JWT_SECRET=your_jwt_secret
   # PORT=5000
   
   npm start
   ```

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   npm start
   ```

The application will open at `http://localhost:3000`

## Usage

1. **Register** - Create a new account with your email and password
2. **Login** - Sign in with your credentials
3. **Create Board** - Create a new whiteboard
4. **Draw** - Use the toolbar to select drawing tools
5. **Share** - Share your board link with others to collaborate
6. **Real-time Sync** - See other users' drawings in real-time

## API Endpoints

### User Routes
- `POST /api/users/register` - Register new user
- `POST /api/users/login` - Login user
- `GET /api/users/profile` - Get user profile (protected)

### Canvas Routes
- `GET /api/canvas` - Get all canvases
- `POST /api/canvas` - Create new canvas
- `GET /api/canvas/:id` - Get specific canvas
- `PUT /api/canvas/:id` - Update canvas
- `DELETE /api/canvas/:id` - Delete canvas

## Real-time Events (Socket.io)

- `draw` - Drawing event from user
- `clear` - Clear canvas event
- `undo` - Undo action
- `user-joined` - New user joined
- `user-left` - User left

## Environment Variables

Create a `.env` file in the backend directory:

```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=5000
NODE_ENV=development
```

## Scripts

### Backend
```bash
npm start          # Start production server
npm run dev        # Start with nodemon for development
```

### Frontend
```bash
npm start          # Start development server
npm run build      # Build for production
npm test           # Run tests
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

**Saurabh Thakur**
- GitHub: [@Saurabh-thakur1](https://github.com/Saurabh-thakur1)

## Support

If you have any questions or run into issues, please open an issue on GitHub.

## Roadmap

- [ ] Add text annotation tool
- [ ] Add shape recognition
- [ ] Add export to image/PDF
- [ ] Add collaborative comments
- [ ] Add version history
- [ ] Mobile app support

---

Made with ❤️ by Saurabh Thakur
