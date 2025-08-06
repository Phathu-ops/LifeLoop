# Overview

LifeLoop: The Game of Real Worlds is a complete 3D life simulation game built with React, Three.js, and Express.js. Players create characters and navigate through different life stages while managing needs, performing activities, and interacting with NPCs in a dynamic city environment. The game features real-time character development, AI-powered NPC conversations using OpenAI GPT-4o, and a comprehensive needs system that affects character progression.

## Recent Changes (January 2025)
- Fixed all LSP TypeScript errors for clean compilation
- Successfully integrated OpenAI API for realistic NPC conversations
- Added comprehensive documentation (README.md, DEPLOYMENT.md, .gitignore)
- Game is fully functional with all core features working
- Ready for GitHub deployment and sharing

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The client uses React with TypeScript and a 3D canvas powered by React Three Fiber (Three.js wrapper). The architecture follows a component-based design with:

- **3D Rendering**: React Three Fiber handles the game world, including player movement, NPCs, buildings, and environmental systems
- **State Management**: Zustand stores manage game state, character data, NPCs, audio, and time progression
- **UI Components**: Radix UI primitives with Tailwind CSS provide the interface layer over the 3D world
- **Game Logic**: Separate modules handle activities, character needs, and life stage progression

The game uses a real-time update loop through useFrame hooks to manage character needs decay, time progression, and NPC behaviors.

## Backend Architecture
The server follows a RESTful Express.js architecture with:

- **Route Organization**: Modular route handlers for AI conversations, character persistence, and health checks
- **AI Integration**: OpenAI GPT-4o integration for dynamic NPC conversations with personality-based responses
- **Storage Layer**: Abstracted storage interface with in-memory implementation (designed for future database integration)
- **Development Server**: Vite integration for hot module replacement in development

## Data Storage Solutions
Currently uses in-memory storage with a clean interface design for future database migration. The storage layer supports:

- **User Management**: Character creation and persistence
- **Drizzle ORM**: Configured for PostgreSQL with schema definitions ready for database integration
- **Migration System**: Drizzle-kit setup for database schema management

## Authentication and Authorization
The codebase includes basic user schema but authentication is not yet implemented. The storage interface suggests preparation for user-based character saves and game state persistence.

# External Dependencies

## Database Services
- **Neon Database**: PostgreSQL serverless database (configured but not yet connected)
- **Drizzle ORM**: Type-safe database operations with PostgreSQL dialect

## AI Services
- **OpenAI API**: GPT-4o model for NPC conversation generation with structured JSON responses

## Development Tools
- **Vite**: Build tool and development server with React plugin
- **TypeScript**: Type safety across the entire codebase
- **Tailwind CSS**: Utility-first styling with custom design system

## UI and 3D Libraries
- **React Three Fiber**: Three.js integration for 3D game world
- **Radix UI**: Accessible component primitives for UI elements
- **Three.js Ecosystem**: Drei for 3D utilities, postprocessing for visual effects

## Audio and Assets
- **GLSL Shader Support**: Custom shaders for enhanced visual effects
- **Asset Loading**: Support for 3D models (GLTF/GLB) and audio files (MP3/OGG/WAV)