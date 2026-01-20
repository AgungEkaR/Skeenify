# Skeenify - Intelligent Skincare Analysis System

A sophisticated web application that analyzes your skin condition using natural language processing and provides personalized skincare ingredient recommendations.

## ✨ Features

### 🧠 Advanced NLP Analysis
- **Context-aware skin type detection** (Oily, Dry, Combination, Sensitive, Normal)
- **Negation handling** ("NOT oily" is correctly interpreted)
- **Intensity modifiers** (very, extremely, slightly)
- **Severity assessment** (mild, moderate, severe)
- **Confidence scoring** for all detections
- **Multi-word phrase detection**

### 🔐 Authentication System
- User and Admin roles
- Login/Register pages
- Protected routes
- Session persistence with localStorage
- Demo accounts included:
  - User: `user@skeenify.com` / `user123`
  - Admin: `admin@skeenify.com` / `admin123`

### 📚 Ingredient Encyclopedia
- **30+ detailed ingredient profiles**
- Clickable ingredient badges from analysis results
- Comprehensive information for each ingredient:
  - Benefits and how it works
  - Usage guidelines and concentration
  - Safety information and side effects
  - Pairing recommendations
  - Pregnancy safety
- Searchable ingredient index
- Smart back navigation

### 👤 User Features
- Skin analysis with natural language input
- Example prompts for guidance
- Visual confidence indicators
- Severity badges for concerns
- Interactive ingredient exploration

### 👨‍💼 Admin Features
- Admin dashboard with user management
- System statistics
- User role management

## 🎨 Design

- Modern glass morphism UI
- Dark purple gradient theme
- Smooth animations and transitions
- Fully responsive (mobile-first)
- Accessible components

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm/pnpm
- Modern web browser

### Installation

```bash
# Install dependencies
npm install
# or
pnpm install

# Run development server
npm run dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📁 Project Structure

```
skeenify-barebone/
├── app/
│   ├── page.tsx              # Home page with skin analyzer
│   ├── login/                # Login page
│   ├── register/             # Registration page
│   ├── admin/                # Admin dashboard
│   └── ingredients/          # Ingredient encyclopedia
│       ├── page.tsx          # Index with search
│       └── [slug]/           # Dynamic ingredient pages
├── components/
│   ├── skin-analyzer-form.tsx    # Main analysis form
│   ├── analysis-results.tsx      # Results display
│   ├── concerns-grid.tsx         # Ingredient recommendations
│   ├── header.tsx                # Navigation with auth
│   ├── protected-route.tsx       # Route protection
│   └── ui/                       # Reusable UI components
├── contexts/
│   └── auth-context.tsx          # Authentication state
├── lib/
│   ├── nlp-engine.ts             # Enhanced NLP analysis
│   ├── ingredients-database.ts   # 30+ ingredient profiles
│   ├── auth.ts                   # Authentication logic
│   └── utils.ts                  # Helper functions
└── styles/
    └── globals.css               # Global styles
```

## 🧪 How It Works

### 1. Natural Language Analysis
The NLP engine analyzes user input like:
- "My skin is very oily with severe acne"
- "I have dry skin BUT NOT sensitive"
- "combination skin with mild redness"

It detects:
- Skin type with confidence score
- Concerns with severity levels
- Negations and context

### 2. Ingredient Recommendations
Based on detected concerns, the system recommends:
- Specific active ingredients
- Proper usage guidelines
- Safety information
- Product pairing suggestions

### 3. Educational Resources
Users can click any ingredient to learn:
- What it does and how it works
- When and how to use it
- Potential side effects
- Safe combinations
- Pregnancy safety

## 🔒 Authentication Flow

1. User registers or logs in
2. Session stored in localStorage
3. Protected routes check authentication
4. Role-based access (user vs admin)
5. Persistent sessions across page reloads

## 🎯 Key Technologies

- **Next.js 16** - React framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Radix UI** - Accessible components
- **Custom NLP Engine** - No external AI APIs

## 📝 Usage Examples

### Basic Analysis
```
Input: "I have oily skin with acne"
Output: 
- Skin Type: Oily (confidence: 95%)
- Concerns: Acne (severity: moderate)
- Ingredients: Salicylic Acid, Niacinamide, Benzoyl Peroxide
```

### With Negation
```
Input: "My skin is oily but NOT sensitive"
Output:
- Skin Type: Oily (confidence: 90%)
- Excludes: Sensitive skin products
- Focuses: Oil control without gentle formulations
```

### Multiple Concerns
```
Input: "dry skin with severe aging and dark spots"
Output:
- Skin Type: Dry (confidence: 95%)
- Concerns: 
  - Aging (severity: severe)
  - Pigmentation (severity: moderate)
- Ingredients: Retinol, Hyaluronic Acid, Vitamin C
```

## 🛠️ Development

### Adding New Ingredients
Edit `lib/ingredients-database.ts`:
```typescript
export const ingredientsDatabase: Record<string, IngredientInfo> = {
  "your-ingredient": {
    id: "your-ingredient",
    name: "Your Ingredient",
    category: "Category",
    description: "...",
    benefits: ["..."],
    // ... more properties
  }
}
```

### Customizing NLP
Edit `lib/nlp-engine.ts` to adjust:
- Keyword patterns
- Confidence thresholds
- Severity detection
- Context rules

## 📄 License

MIT License - feel free to use for personal or commercial projects.

## 🤝 Contributing

Contributions welcome! Please feel free to submit a Pull Request.

---

Built with ❤️ for better skincare education
=======
>>>>>>> 704980e268f06b2272ae9a226023c5e3107979ba
