# [JobAnalog 🔗](https://job-analog.vercel.app/)


JobAnalog is your AI-powered career companion — helping you craft professional resumes, generate personalized cover letters, practice interviews, and optimize your job search with intelligent insights and automated tools. Built for simplicity, effectiveness, and smarter career advancement.

## 🌟 Features

### Core Functionality
- **📊 Interactive Dashboard**: Real-time overview of your career progress with analytics and insights
- **📄 Resume Builder**: Create professional resumes with AI-powered content suggestions
- **💼 AI Cover Letter Generator**: Personalized cover letters tailored to specific job applications
- **🎤 Interview Preparation**: AI-powered mock interviews with feedback and improvement tips
- **📱 Onboarding Flow**: Seamless user setup and profile configuration

### AI-Powered Features
- **🤖 AI Career Insights**: Personalized career recommendations using Google Gemini AI
- **📝 Content Generation**: AI-driven resume and cover letter content optimization
- **🎯 Job Matching**: Intelligent job recommendations based on skills and preferences
- **📊 Performance Analysis**: AI-driven career progress analysis and improvement suggestions

### User Experience
- **🔐 Secure Authentication**: Enterprise-grade authentication with Clerk
- **📱 Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **🎨 Modern UI**: Clean, intuitive interface built with Tailwind CSS and Shadcn UI
- **🌙 Dark Mode**: Beautiful dark and light theme support

## 🛠️ Technologies Used

### Frontend & Backend
- **Next.js 15**: Full-stack React framework with App Router
- **React 19**: Latest React with concurrent features
- **Tailwind CSS**: Utility-first CSS framework
- **Shadcn UI**: Beautiful and accessible component library
- **Radix UI**: Primitive UI components

### Database & ORM
- **PostgreSQL**: Robust relational database with Neon DB
- **Prisma**: Modern database ORM with type safety

### Authentication & Security
- **Clerk**: Complete authentication solution with secure user management
- **Next.js Middleware**: Route protection and security

### AI & External Services
- **Google Gemini AI**: Advanced AI for career insights and content generation
- **Inngest**: Background job processing for AI workflows

### Development Tools
- **ESLint**: Code linting and formatting
- **PostCSS**: CSS processing
- **React Hook Form**: Form state management
- **Zod**: Schema validation
- **Date-fns**: Modern date utility library

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- PostgreSQL database (Neon DB recommended)
- Clerk account for authentication
- Google Cloud account for Gemini AI

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Ramprakash852/JobAnalog.git
   cd JobAnalog
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   
   Create a `.env` file in the root directory:
   ```env
   # Database Configuration
   DATABASE_URL="your-neon-postgresql-connection-string"
   
   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your-clerk-publishable-key"
   CLERK_SECRET_KEY="your-clerk-secret-key"
   NEXT_PUBLIC_CLERK_SIGN_IN_URL="/sign-in"
   NEXT_PUBLIC_CLERK_SIGN_UP_URL="/sign-up"
   NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL="/onboarding"
   NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL="/onboarding"
   
   # AI Services
   GEMINI_API_KEY="your-google-gemini-api-key"
   ```

### Database Setup

1. **Run Prisma migrations**
   ```bash
   npx prisma migrate deploy
   ```

2. **Generate Prisma client**
   ```bash
   npx prisma generate
   ```

3. **Seed the database (optional)**
   ```bash
   npm run seed
   ```

### Development

1. **Start the development server**
   ```bash
   npm run dev
   ```

2. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
JobAnalog/
├── app/                    # Next.js app directory
│   ├── (auth)/            # Authentication pages
│   │   ├── sign-in/       # Sign in page
│   │   └── sign-up/       # Sign up page
│   ├── (main)/            # Main application pages
│   │   ├── dashboard/     # User dashboard
│   │   ├── onboarding/    # User onboarding flow
│   │   ├── resume/        # Resume builder
│   │   ├── ai-cover-letter/ # Cover letter generator
│   │   └── interview/     # Interview preparation
│   ├── api/               # API routes
│   └── globals.css        # Global styles
├── components/            # Reusable UI components
│   ├── ui/               # Base UI components (Shadcn)
│   ├── header.jsx        # Navigation header
│   └── hero.jsx          # Landing page hero
├── actions/              # Server actions
├── lib/                  # Utility functions and configurations
├── hooks/                # Custom React hooks
├── data/                 # Static data files
├── prisma/               # Database schema and migrations
└── public/               # Static assets
```

## 🔧 Available Scripts

```bash
npm run dev          # Start development server with Turbopack
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npx prisma studio    # Open Prisma database studio
```

## 🗃️ Database Schema

### Core Models
- **Users**: User profile and authentication data
- **Resumes**: Resume templates and content
- **CoverLetters**: Generated cover letter records
- **Interviews**: Interview session data and feedback
- **JobApplications**: Job application tracking

### Key Features
- UUID primary keys for security
- Cascading deletes for data integrity
- Indexed foreign keys for performance
- Enum types for data consistency

## 🔐 Authentication Flow

1. User signs up/signs in through Clerk
2. User profile is automatically created in the database
3. Onboarding flow collects career information
4. Protected routes redirect unauthenticated users
5. Server actions validate user permissions

## 🤖 AI Features

### Resume Enhancement
- AI-powered content suggestions
- Industry-specific formatting recommendations
- Keyword optimization for ATS systems
- Skills gap analysis

### Cover Letter Generation
- Job-specific personalization
- Company research integration
- Tone and style optimization
- A/B testing capabilities

### Interview Preparation
- Common question practice
- Behavioral interview coaching
- Industry-specific scenarios
- Real-time feedback and improvement tips

## 📊 Career Analytics

- Application tracking and success rates
- Resume performance metrics
- Interview preparation progress
- Career goal milestone tracking
- Market trend insights

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

### Environment Variables

Ensure all production environment variables are set:
- Use production Clerk keys
- Configure production database (Neon DB)
- Set up production AI service limits
- Configure proper CORS settings

### Recommended Platforms
- **Vercel**: Optimal for Next.js applications
- **Netlify**: Great alternative with easy setup
- **Railway**: Good for full-stack applications
- **AWS/GCP/Azure**: Enterprise-grade hosting

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run E2E tests
npm run test:e2e
```

## 📈 Performance

- Server-side rendering for fast initial loads
- Optimized database queries with Prisma
- Image optimization with Next.js
- Code splitting and lazy loading
- AI response caching for improved performance

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow React and Next.js best practices
- Write tests for new features
- Follow the existing code style
- Update documentation for new features
- Ensure AI features are cost-effective

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: support@jobanalog.com
- 💬 Discord: [Community Server](https://discord.gg/jobanalog)
- 📚 Documentation: [Full Documentation](https://docs.jobanalog.com)

## 🎯 Roadmap

- [ ] Mobile app development (React Native)
- [ ] Advanced AI career coaching features
- [ ] Integration with major job boards
- [ ] LinkedIn profile optimization
- [ ] Salary negotiation assistant
- [ ] Career path recommendations
- [ ] Networking opportunity suggestions
- [ ] Skills assessment and certification tracking

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing framework
- [Clerk](https://clerk.dev/) for authentication services
- [Prisma](https://prisma.io/) for database management
- [Google](https://cloud.google.com/vertex-ai) for AI capabilities
- [Shadcn UI](https://ui.shadcn.com/) for beautiful components
- [Vercel](https://vercel.com/) for hosting platform

---

**Made with ❤️ for better career opportunities**
