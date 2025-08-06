# LifeLoop: The Game of Real Worlds

**Live, Dream, Connect — One Life at a Time.**

LifeLoop is a 3D life simulation game built with React, Three.js, and Express.js where you can build your dream life, explore real-world cultures, and form deep emotional connections with AI-powered characters.

## Features

🌆 **Live in immersive 3D cities** - Explore detailed urban environments  
🧠 **AI-driven NPCs** - Powered by OpenAI GPT-4o for realistic conversations  
🎨 **Customizable homes** - Build and decorate your living spaces  
❤️ **Dynamic needs system** - Manage happiness, energy, social, hunger, and hygiene  
🌍 **Real-time progression** - Day/night cycles and character aging  
👨‍👩‍👧‍👦 **Multiple life stages** - Start as child, teen, adult, or elder  

## Quick Start

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd lifeloop-game
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file and add:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

4. **Start the game**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5000`

## Game Controls

- **WASD / Arrow Keys** - Move your character
- **E / Space** - Interact with NPCs and objects
- **ESC / M** - Open menu
- **Mouse** - Look around the 3D world

## Technology Stack

- **Frontend**: React, TypeScript, Three.js (React Three Fiber)
- **Backend**: Express.js, Node.js
- **AI**: OpenAI GPT-4o for NPC conversations
- **State Management**: Zustand
- **Styling**: Tailwind CSS
- **UI Components**: Radix UI
- **Build Tool**: Vite

## Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # React components
│   │   │   ├── game/      # 3D game components
│   │   │   └── ui/        # UI components
│   │   ├── lib/           # Game logic and stores
│   │   │   ├── gameLogic/ # Core game mechanics
│   │   │   └── stores/    # Zustand state management
│   │   └── pages/         # Application pages
│   └── public/            # Static assets
├── server/                # Backend Express application
│   ├── routes/           # API route handlers
│   └── storage.ts        # Data storage layer
└── shared/               # Shared types and schemas
```

## Game Mechanics

### Character System
- **Life Stages**: Child (5-12), Teen (13-19), Adult (20-64), Elder (65+)
- **Personality Traits**: Creativity, Sociability, Ambition, Kindness
- **Needs Management**: Five core needs that decay over time
- **Aging**: Real-time character development and life stage transitions

### Activities System
- Age-appropriate activities for each life stage
- Energy costs and benefits for each action
- Experience gains in different skill areas
- Money earning through work activities

### AI NPCs
- Unique personalities and conversation styles
- Memory of past interactions
- Relationship tracking with player
- Contextual responses based on game state

### Home Customization
- Multiple rooms: Living room, bedroom, kitchen
- Furniture and decoration purchases
- Money management system

## Development

### Adding New Features

1. **New Activities**: Add to `client/src/lib/gameLogic/activities.ts`
2. **New NPCs**: Update `client/src/lib/stores/useNPCs.tsx`
3. **New UI Components**: Add to `client/src/components/ui/`
4. **API Routes**: Add to `server/routes/`

### Environment Setup

The game requires Node.js 18+ and an OpenAI API key for AI features.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source. See LICENSE file for details.

## Support

For questions or support, please open an issue on GitHub.

---

**Start your life simulation journey today with LifeLoop!**