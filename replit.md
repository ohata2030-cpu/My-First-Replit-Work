# IgedeVoice - Cultural Community Platform

## Overview
IgedeVoice is a comprehensive web platform designed to preserve and celebrate Igede culture while connecting the global Igede community. The application serves as a central hub for news, cultural content, music, blogging, and community dating services. It aims to provide both public access to cultural content and authenticated user features for community engagement, with a vision to be a central online repository for Igede heritage.

## User Preferences
Preferred communication style: Simple, everyday language.

## System Architecture
### Frontend Architecture
- **Framework**: React 18 with TypeScript (Vite build tool)
- **Routing**: Wouter
- **UI Components**: Radix UI primitives with shadcn/ui
- **Styling**: Tailwind CSS with custom Igede cultural color variables
- **State Management**: TanStack Query (React Query)
- **Forms**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API architecture
- **Middleware**: Express middleware for logging, JSON parsing, error handling

### Database Architecture
- **Database**: PostgreSQL (Neon serverless)
- **ORM**: Drizzle ORM with TypeScript schema definitions
- **Migrations**: Drizzle Kit
- **Connection**: Connection pooling with `@neondatabase/serverless`

### Key Components
- **Authentication**: Replit Authentication (OpenID Connect), Express sessions with PostgreSQL store.
- **Content Management**: CRUD for news, celebrity posts, cultural blogs, music hosting; includes like/dislike, view tracking, commenting.
- **Dating Community**: Age-verified profiles, matching, direct messaging, privacy controls.
- **Media Handling**: Support for images and audio with organized asset management.

### Data Flow
- **Public Content**: Anonymous browsing of content via REST API with pagination and view tracking.
- **Authenticated User**: Replit OAuth authentication, session persistence, access to dating community, content engagement.
- **Content Creation**: Admin/authorized user content creation, Zod validation, Drizzle ORM operations, React Query cache invalidation for real-time updates.

## External Dependencies
### Core Infrastructure
- **Hosting**: Replit platform
- **Database**: Neon PostgreSQL
- **Authentication**: Replit Authentication service
- **CDN**: Replit's infrastructure

### Third-Party Services
- **Payment Gateway**: Paystack (for premium dating features)
- **Email**: Ready for SMTP integration
- **Analytics**: Prepared for Google Analytics
- **Social Media**: Facebook, Twitter, WhatsApp sharing

### Development Tools
- **TypeScript**: For type safety
- **ESLint/Prettier**: For code quality and formatting
- **Vite**: For fast development builds
- **PostCSS**: For CSS processing with Tailwind

## Recent Updates

### February 14, 2025
- **Critical Bug Fix: Dating Registration**: Resolved "413 request entity too large" and foreign key constraint errors
- **Mobile Music UX Enhancement**: Significantly improved music interface for mobile devices with larger touch targets and better visual hierarchy
- **Dating Community Navigation**: Added convenient X close button in dating dashboard for easy homepage return

### August 16, 2025
- **GitHub Integration Setup**: Configured Git repository for GitHub transfer with proper branch structure (main/replit-agent)
- **Main Pages Development**: Continuing enhancement work on Landing, Home, Music, and Dating pages from previous session