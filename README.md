# Find Ur Belongingzzzz 🔍
> *"Lost it? Let's find it!"*

**Find Ur Belongingzzzz** is a modern, responsive, high-performance campus Lost & Found web application designed for university communities. It pairs students who have misplaced belongings with fellow students or campus facilities staff who found them, powered by an intelligent **Smart Match AI Correlation Engine**.

---

## 🌟 Key Features

### 1. Smart Match AI Engine
- **Multi-Factor Correlation Algorithm**:
  - **Category Compatibility** (+35 pts): Validates functional type alignment.
  - **Keyword & Semantic Overlap** (+35 pts): Tokenizes titles, descriptions, brands, and identifying attributes (filtering common stop words) to compute similarity.
  - **Campus Vicinity & Zone Match** (+18 pts): Checks exact campus building (e.g. Central Library, Main Canteen, CS Block, North Parking) or proximate zones.
  - **Timeline Proximity** (+12 pts): Rewards reports filed within 24 to 72 hours of each other.
- **Visual Confidence Score**: Displays clear badges (e.g., `Smart Match 93%`).
- **Granular Match Reasons**: Gives human-readable explanations like:
  - `✓ Identical category: Electronics`
  - `✓ Similar keywords: "sony", "headphones", "matte", "black"`
  - `✓ Same campus zone: Central Library`
  - `✓ Same day discovery: reported on the exact same date`
- **Interactive Side-by-Side Comparison**: Dual-column modal allowing students to inspect both items side-by-side with match metrics and 1-click claim action.

### 2. Student Authentication & Demo Personas
- Instant 1-click sign-in with 4 realistic student personas:
  - **Aarav Sharma** (Computer Science, 3rd Year)
  - **Priya Patel** (Electronics & Comm, 2nd Year)
  - **Rohan Verma** (Mechanical Engineering, 4th Year)
  - **Ananya Rao** (Biotechnology, 3rd Year)
- Full custom registration and sign-in flow.
- Campus Trust / Karma rating system with progress tracker and honors.

### 3. Comprehensive Dashboard
- **Live Statistics Overview**: Total Lost Items, Total Found Items, Successfully Returned Items, Potential Smart Matches.
- **Quick Action Bar**: 1-click access to Report Lost, Report Found, and Browse.
- **Smart Match Spotlight**: Immediate preview of high-confidence matches.
- **Recent Listings Filter**: Toggle between All, Lost Only, and Found Only.

### 4. Report Lost & Found Belongings
- Fast, intuitive workflow tailored to campus needs:
  - Select item category (Electronics, IDs, Wallets, Books, Keys, etc.)
  - Set specific campus room / table / zone
  - Select from categorized preset photo gallery, upload a local photo, or supply an image URL
  - Record private identifying details for secure verification
  - **For Found Items**: Safe drop-off holding location recorder (e.g. "Library Circulation Desk", "Canteen Supervisor Counter", "Security Gate 1")
  - **For Lost Items**: Optional reward/incentive offer
  - Automatic Smart Match calculation upon report submission with instant toast & notification!

### 5. Browse & Discovery
- Full-text instant search across item titles, descriptions, and locations.
- Segmented status filters: All Items, Lost Only, Found Only, Returned.
- Category filter dropdown.
- Campus location filter dropdown.
- Sort by Newest, Oldest, or Alphabetical.
- Empty states with recovery prompts and reset buttons.

### 6. Ownership Verification & Claim Flow
- Honor-code certified claim modal with proof-of-ownership prompt (e.g., secret lockscreen, engraving, internal contents).
- Contact finder via in-app message, student campus email, or phone with 1-click copy.
- "Mark as Returned" flow that celebrates with confetti animation, rewards +50 Karma points, and logs community resolution.

### 7. Notification Center & Toast Feedback
- Dedicated notification dropdown tracking AI matches, claim inquiries, and status updates.
- Real-time floating stacked toasts with custom color-coded styling (Success, Smart Match, Warning, Error, Info).

---

## 🎨 UI/UX Design System

- **Palette**: Dark navy & deep slate background (`#080b14`, `#0d1322`, `#0f172a`) with vibrant indigo (`#6366f1`), violet (`#8b5cf6`), electric cyan (`#06b6d4`), emerald (`#10b981`), and warm rose (`#f43f5e`).
- **Typography**: Plus Jakarta Sans for crisp modern headings and body, JetBrains Mono for codes and tags.
- **Micro-Interactions**: Smooth hover elevations, glowing gradient borders, pulsing match indicators, celebratory confetti on item returns.
- **Iconography**: Complete Lucide React icon suite.
- **Responsiveness**: Fully fluid layout optimized for Desktop, Laptop, Tablet, and Mobile screens.

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+ or v24 LTS)
- npm

### Installation & Run

1. Clone or navigate to the project directory:
   ```bash
   cd c:\Users\Administrator\Documents\PROJECT
   ```

2. Install dependencies (already installed):
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:5173/
   ```

5. Build for production:
   ```bash
   npm run build
   ```

---

## 📁 Key File Structure

```
PROJECT/
├── index.html                   # HTML entry point with Plus Jakarta Sans & JetBrains Mono
├── package.json                 # Project dependencies (React 19, Tailwind CSS v4, Lucide React, Confetti)
├── vite.config.ts               # Vite configuration with Tailwind CSS plugin
├── src/
│   ├── main.tsx                 # React DOM mount point
│   ├── App.tsx                  # Root component, routing, and layout coordinator
│   ├── index.css                # Tailwind CSS v4 import, scrollbars, and glassmorphism
│   ├── types/
│   │   └── index.ts             # TypeScript interfaces for Items, Users, Matches, Claims
│   ├── data/
│   │   └── mockData.ts          # Realistic campus items, locations, notifications, and student personas
│   ├── context/
│   │   └── AppContext.tsx       # Global state management with LocalStorage persistence
│   ├── utils/
│   │   ├── smartMatch.ts        # AI Smart Match multi-criteria correlation algorithm
│   │   └── helpers.ts           # Date formatters, category badges, sample photo presets
│   ├── components/
│   │   ├── common/
│   │   │   ├── Badge.tsx        # Lost/Found, Category, and Smart Match percentage badges
│   │   │   ├── Button.tsx       # Purpose-built variants (Report Lost, Report Found, Claim, Match)
│   │   │   ├── Modal.tsx        # Accessible backdrop blur modal with Escape key handling
│   │   │   ├── Toast.tsx        # Animated floating notification toasts
│   │   │   ├── EmptyState.tsx   # Polished empty state with action triggers
│   │   │   └── StatsCard.tsx    # Dashboard statistic card with gradient glow
│   │   ├── items/
│   │   │   ├── ItemCard.tsx     # Item card with match badge, metadata, and detail trigger
│   │   │   ├── ItemDetailModal.tsx # Full item view with reporter info and match alert
│   │   │   ├── ClaimModal.tsx   # Ownership proof verification dialog
│   │   │   └── ContactModal.tsx # Student contact dialog with quick message form
│   │   ├── smartmatch/
│   │   │   ├── SmartMatchCard.tsx # Dual preview card with match reasons and score gauge
│   │   │   └── CompareModal.tsx # Side-by-side comparison modal
│   │   ├── notifications/
│   │   │   └── NotificationDropdown.tsx # Bell icon dropdown with unread count
│   │   └── layout/
│   │       ├── Navbar.tsx       # Top navbar with quick actions and persona switcher
│   │       ├── Sidebar.tsx      # Desktop fixed & mobile drawer navigation
│   │       └── Footer.tsx       # Campus hubs, honor code, and links
│   └── views/
│       ├── LandingView.tsx      # Hero page with live radar, 3-step guide, and metrics
│       ├── DashboardView.tsx    # Metrics, quick actions, match highlights, recent listings
│       ├── BrowseView.tsx       # Search and multi-filter discovery explorer
│       ├── ReportItemView.tsx   # Lost & Found reporting form with photo presets
│       ├── SmartMatchesView.tsx # Dedicated AI correlation hub with confidence filtering
│       ├── MyItemsView.tsx      # User's items manager with "Mark as Returned" celebration
│       ├── ProfileView.tsx      # Student profile, karma rating, and badges
│       └── AuthModal.tsx        # Authentication modal with 1-click demo logins
```

---

## 🏆 Competition Checklist (P0, P1, P2)

- [x] **P0 — MUST WORK**:
  - [x] Application builds and starts successfully with 0 errors
  - [x] Smooth navigation between Landing, Dashboard, Browse, Report, Smart Matches, My Items, Profile
  - [x] Dashboard with active statistics, quick actions, and recent listings
  - [x] Lost item reporting with category, location, date, photo, and details
  - [x] Found item reporting with safe holding drop-off location
  - [x] Browse & search with real-time text query and category/location/type filtering
  - [x] Detailed item view modal with reporter card and actions
  - [x] Smart Match system calculating match percentage and displaying matching reasons
- [x] **P1 — IMPORTANT**:
  - [x] Student authentication and 1-click persona switching
  - [x] Live toast notification system + Notification dropdown
  - [x] Student profile with Karma score and achievement badges
  - [x] Mobile and tablet responsive navigation and layouts
  - [x] Proof of ownership verification modal
  - [x] "Mark as Returned" resolution flow with confetti celebration
- [x] **P2 — POLISH**:
  - [x] Dark navy/purple startup aesthetic with glowing accents
  - [x] Lucide icons throughout
  - [x] Pre-populated realistic campus data with high-res photos
  - [x] LocalStorage persistence with 1-click demo reset button
