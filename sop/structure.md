/src
  /app                       # Next.js App Router pages and layouts
    /api                     # API Routes
      /courses               # Course API endpoints
        /[courseId]          # Course-specific endpoints
          /lessons           # Lesson endpoints for a specific course
            /[lessonId]      # Lesson-specific endpoints
              /route.ts      # CRUD operations for a specific lesson
            /route.ts        # CRUD operations for lessons
          /route.ts          # CRUD operations for specific course
        /route.ts            # CRUD operations for courses
      /progress              # User progress tracking endpoints
        /route.ts            # Mark lessons as complete/incomplete
      /auth                  # Authentication related endpoints (if needed)
        /[...nextauth]       # NextAuth.js configuration (if using)
        /route.ts            # Auth related endpoints

    /(routes)                # App router pages
      /dashboard             # User dashboard
        /page.tsx            # Dashboard homepage
      /courses               # Course pages
        /page.tsx            # Course listing page
        /[courseId]          # Course detail page
          /page.tsx          # Course detail view
          /lessons           # Lesson pages for a course
            /[lessonId]      # Individual lesson page
              /page.tsx      # Lesson content view
      /admin                 # Admin section
        /courses             # Admin course management
          /page.tsx          # List courses for admin
          /new               # Create new course
            /page.tsx        # New course form
          /[courseId]        # Edit course
            /page.tsx        # Edit course form
            /lessons         # Lesson management for a course
              /page.tsx      # List lessons for admin
              /new           # Create new lesson
                /page.tsx    # New lesson form
              /[lessonId]    # Edit lesson
                /page.tsx    # Edit lesson form
      /profile               # User profile section
        /page.tsx            # User profile and settings

    /layout.tsx              # Root layout
    /page.tsx                # Home page

  /components                # Reusable UI components
    /ui                      # Basic UI components (buttons, inputs, etc.)
    /layout                  # Layout components (navbar, sidebar, footer)
    /courses                 # Course-related components
      /CourseCard.tsx        # Course card component
      /CourseForm.tsx        # Course creation/editing form
      /CourseList.tsx        # List of courses
    /lessons                 # Lesson-related components
      /LessonCard.tsx        # Lesson card component
      /LessonForm.tsx        # Lesson creation/editing form
      /LessonList.tsx        # List of lessons
    /progress                # Progress tracking components
      /ProgressBar.tsx       # Progress bar component
      /CompletionBadge.tsx   # Completion badge component

  /lib                       # Shared libraries and utilities
    /db                      # Database related code
      /schema.ts             # Database schema definitions
      /models                # Database models
        /course.ts           # Course model
        /lesson.ts           # Lesson model
        /progress.ts         # Progress model
    /utils                   # Utility functions
      /formatter.ts          # Date/text formatting utilities
      /validators.ts         # Form validation

  /types                     # TypeScript type definitions
    /course.ts               # Course-related types
    /lesson.ts               # Lesson-related types
    /progress.ts             # Progress-related types
    /user.ts                 # User-related types

  /hooks                     # Custom React hooks
    /useCourses.ts           # Hook for course data
    /useLessons.ts           # Hook for lesson data
    /useProgress.ts          # Hook for progress tracking

  /services                  # Service layer for API calls
    /courseService.ts        # Course-related API services
    /lessonService.ts        # Lesson-related API services
    /progressService.ts      # Progress-related API services

  /context                   # React Context for state management
    /CourseContext.tsx       # Context for courses
    /ProgressContext.tsx     # Context for user progress
    /AuthContext.tsx         # Context for authentication (if needed)

  /config                    # Configuration files
    /routes.ts               # Route definitions
    /constants.ts            # App constants

  /data                      # Seed data and static data
    /seed                    # Seed data scripts
      /courses.ts            # Sample course data
      /lessons.ts            # Sample lesson data
      /progress.ts           # Sample progress data

/public                      # Static assets
  /images                    # Image assets
    /courses                 # Course images
    /icons                   # Icon assets

/prisma                      # Prisma ORM files (if using Prisma)
  schema.prisma              # Prisma schema

/scripts                     # Utility scripts
  /seed.ts                   # Database seeding script

.env                         # Environment variables
.env.local                   # Local environment variables