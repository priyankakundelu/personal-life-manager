# Personal Life Manager

A comprehensive all-in-one application to manage your life - expenses, planning, household tasks, nutrition, and fitness tracking.

## Features

### 💰 Finance
- Track expenses and income
- Create and monitor budgets
- View financial summaries and balance

### 📅 Planner
- Task management with priorities
- Goal tracking with progress
- Event calendar

### 🏠 Household
- Shopping lists with items
- Chore management and assignments
- Family organization

### 🥗 Nutrition
- Recipe management
- Meal planning
- Food diary tracking
- Calorie monitoring

### 💪 Fitness
- Workout logging
- Exercise tracking
- Fitness goals with progress
- Workout summaries

## Tech Stack

### Backend
- **Node.js** with **Express**
- **TypeScript** for type safety
- **SQLite** database
- RESTful API

### Frontend
- **React** with **TypeScript**
- **Vite** for fast development
- **Tailwind CSS** for styling
- **React Router** for navigation
- **Axios** for API calls

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn

## Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd personal-life-manager
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend` directory:

```env
PORT=5000
NODE_ENV=development
DB_PATH=./database/life_manager.db
```

Initialize the database:

```bash
npm run init-db
```

Start the backend server:

```bash
npm run dev
```

The backend will run on `http://localhost:5000`

### 3. Frontend Setup

Open a new terminal:

```bash
cd frontend
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will run on `http://localhost:3000`

## Project Structure

```
personal-life-manager/
├── backend/
│   ├── src/
│   │   ├── database/
│   │   │   ├── db.ts          # Database connection
│   │   │   ├── schema.sql     # Database schema
│   │   │   └── init.ts        # Database initialization
│   │   ├── routes/
│   │   │   ├── finance.ts     # Finance API routes
│   │   │   ├── planner.ts     # Planner API routes
│   │   │   ├── household.ts   # Household API routes
│   │   │   ├── nutrition.ts   # Nutrition API routes
│   │   │   └── fitness.ts     # Fitness API routes
│   │   └── server.ts          # Express server setup
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   └── Layout.tsx     # Main layout component
│   │   ├── pages/
│   │   │   ├── Dashboard.tsx  # Dashboard page
│   │   │   ├── Finance.tsx    # Finance page
│   │   │   ├── Planner.tsx    # Planner page
│   │   │   ├── Household.tsx # Household page
│   │   │   ├── Nutrition.tsx  # Nutrition page
│   │   │   └── Fitness.tsx    # Fitness page
│   │   ├── api/
│   │   │   └── client.ts      # API client setup
│   │   ├── App.tsx            # Main app component
│   │   └── main.tsx           # Entry point
│   └── package.json
└── README.md
```

## API Endpoints

### Finance
- `GET /api/finance/expenses` - Get all expenses
- `POST /api/finance/expenses` - Create expense
- `PUT /api/finance/expenses/:id` - Update expense
- `DELETE /api/finance/expenses/:id` - Delete expense
- `GET /api/finance/income` - Get all income
- `POST /api/finance/income` - Create income
- `GET /api/finance/budgets` - Get all budgets
- `POST /api/finance/budgets` - Create budget
- `GET /api/finance/summary` - Get financial summary

### Planner
- `GET /api/planner/tasks` - Get all tasks
- `POST /api/planner/tasks` - Create task
- `PUT /api/planner/tasks/:id` - Update task
- `DELETE /api/planner/tasks/:id` - Delete task
- `GET /api/planner/goals` - Get all goals
- `POST /api/planner/goals` - Create goal
- `GET /api/planner/events` - Get all events
- `POST /api/planner/events` - Create event

### Household
- `GET /api/household/shopping-lists` - Get all lists
- `POST /api/household/shopping-lists` - Create list
- `GET /api/household/shopping-lists/:id/items` - Get list items
- `POST /api/household/shopping-lists/:id/items` - Add item
- `GET /api/household/chores` - Get all chores
- `POST /api/household/chores` - Create chore

### Nutrition
- `GET /api/nutrition/recipes` - Get all recipes
- `POST /api/nutrition/recipes` - Create recipe
- `GET /api/nutrition/meal-plans` - Get meal plans
- `POST /api/nutrition/meal-plans` - Create meal plan
- `GET /api/nutrition/food-diary` - Get food diary
- `POST /api/nutrition/food-diary` - Add food entry
- `GET /api/nutrition/summary` - Get nutrition summary

### Fitness
- `GET /api/fitness/workouts` - Get all workouts
- `POST /api/fitness/workouts` - Create workout
- `GET /api/fitness/workouts/:id` - Get workout with exercises
- `POST /api/fitness/workouts/:id/exercises` - Add exercise
- `GET /api/fitness/goals` - Get all goals
- `POST /api/fitness/goals` - Create goal
- `GET /api/fitness/summary` - Get fitness summary

## Development

### Backend Development

```bash
cd backend
npm run dev
```

### Frontend Development

```bash
cd frontend
npm run dev
```

### Building for Production

**Backend:**
```bash
cd backend
npm run build
npm start
```

**Frontend:**
```bash
cd frontend
npm run build
```

The built files will be in `frontend/dist` directory.

## Database

The application uses SQLite for data storage. The database file is created automatically when you run `npm run init-db` in the backend directory.

Database location: `backend/database/life_manager.db`

## Environment Variables

### Backend (.env)
- `PORT` - Server port (default: 5000)
- `NODE_ENV` - Environment (development/production)
- `DB_PATH` - Path to SQLite database file

### Frontend
- `VITE_API_URL` - Backend API URL (default: http://localhost:5000/api)

## Deployment

To deploy this application and make it publicly accessible, see the [DEPLOYMENT.md](./DEPLOYMENT.md) guide.

**Quick Start:**
1. Push your code to GitHub
2. Deploy backend to [Railway](https://railway.app) (set root directory to `backend`)
3. Deploy frontend to [Vercel](https://vercel.com) (set root directory to `frontend`)
4. Configure environment variables as described in [DEPLOYMENT.md](./DEPLOYMENT.md)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License

## Support

For issues and questions, please open an issue on GitHub.

---

Built with ❤️ for managing your life better!

