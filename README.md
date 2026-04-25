# Spliter - Expense Splitting Application

A comprehensive full-stack web application for tracking, splitting, and settling shared expenses between individuals and groups.

## 📚 Documentation

Complete project documentation is available in the following files:

- **[Complete Documentation](./DOCUMENTATION.md)** - Full project documentation including scope, tech stack, and data schema
- **[ERD (Entity Relationship Diagram)](./docs/ERD.md)** - Database schema and relationships
- **[Use Case Diagram](./docs/USE_CASE_DIAGRAM.md)** - System use cases and user flows
- **[Data Dictionary](./docs/DATA_DICTIONARY.md)** - Detailed field descriptions and constraints
- **[UI Documentation](./docs/UI_DOCUMENTATION.md)** - User interface design and component library

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Convex account
- Clerk account

### Run with Docker

1. Create an environment file (for example `.env.production`) containing the variables listed in [Documentation](./PROJECT_INTEGRATIONS_EXPLAINED.md#-environment-variables-required).
2. Build the image (pass the public env vars required at build time):
   ```bash
   docker build \
     --build-arg NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_xxx \
     --build-arg NEXT_PUBLIC_CONVEX_URL=https://your.convex.cloud \
     -t spliter .
   ```
3. Run the container while injecting the env file (contains the remaining secrets such as `CLERK_SECRET_KEY`, `RESEND_API_KEY`, etc.):
   ```bash
   docker run --env-file .env.production -p 3000:3000 spliter
   ```
4. Open [http://localhost:3000](http://localhost:3000) to access the app.

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd splitter
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
```bash
cp .env.example .env.local
```

Fill in the required environment variables:
- `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY`
- `CLERK_SECRET_KEY`
- `CLERK_JWT_ISSUER_DOMAIN`
- `NEXT_PUBLIC_CONVEX_URL`
- `CONVEX_DEPLOY_KEY`

4. Run the development server
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser

## 🛠️ Tech Stack

- **Frontend**: Next.js 15, React 19, Tailwind CSS
- **Backend**: Convex (Serverless)
- **Authentication**: Clerk
- **UI Components**: shadcn/ui, Radix UI
- **Forms**: React Hook Form, Zod
- **Charts**: Recharts

## 📖 Features

- ✅ Individual and group expense tracking
- ✅ Multiple split types (equal, percentage, exact)
- ✅ Settlement recording and tracking
- ✅ Balance calculations
- ✅ Expense categorization
- ✅ Spending analytics
- ✅ Real-time updates
- ✅ User search and contacts
- ✅ Payment reminders (via Inngest)

## 📝 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## 📄 License

This project is private and proprietary.

## 🤝 Contributing

This is a private project. For questions or issues, please contact the development team.
