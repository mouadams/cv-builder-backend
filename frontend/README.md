# CV Builder Frontend

A professional CV/Resume builder application built with Angular.

This is a standalone frontend repository. The backend is in a separate repository.

## Features

- 🎨 Multiple professional resume templates (Atlas, Nova)
- ✏️ Real-time preview while editing
- 💾 Save resumes to database or localStorage
- 📄 Export to PDF
- 🖨️ Print directly
- 🌐 Right-to-left (RTL) text support
- 🔄 Template switching without page refresh

## Project Structure

```
frontend/
├── src/                    # Angular frontend
│   └── app/
│       ├── features/        # Feature modules
│       └── core/           # Core services and models
```

## Prerequisites

- Node.js 20.19+ or 22.12+
- npm 11.6.2+

## Getting Started

1. Clone this repository:
```bash
git clone <frontend-repository-url>
cd <frontend-repository-name>
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The frontend will be available at `http://localhost:4200`

## Backend Integration

This frontend expects a backend API running at `http://localhost:8080`. Make sure to:

1. Clone and run the backend repository separately
2. Ensure the backend is running on port 8080
3. The backend should have CORS configured to allow requests from `http://localhost:4200`

## API Endpoints

- `POST /api/resumes` - Create a new resume
- `GET /api/resumes/{id}` - Get a resume by ID
- `GET /api/resumes` - Get all resumes
- `PUT /api/resumes/{id}` - Update a resume
- `DELETE /api/resumes/{id}` - Delete a resume

## API Configuration

The frontend is configured to communicate with the backend API at `http://localhost:8080/api/resumes`.

To change the API endpoint, update `src/app/core/services/resume-api.service.ts`:

```typescript
private readonly apiUrl = 'http://localhost:8080/api/resumes';
```

## Development

- Angular 21.1.1
- Angular Material
- TypeScript 5.9.2

## License

This project is open source and available for personal and commercial use.
