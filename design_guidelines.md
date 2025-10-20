# MailPilot Design Guidelines

## Design Approach
**Reference-Based Approach**: Drawing inspiration from Linear (clean data tables, subtle interactions), Notion (card-based layouts), and Stripe (professional dashboard aesthetics) while incorporating MailPilot's distinctive purple-accented data visualization style as shown in the provided screenshots.

## Core Design Elements

### A. Color Palette

**Primary Colors:**
- Primary Blue: 203 100% 52% (existing #0B63FF for CTAs, active states, brand elements)
- Primary Purple: 270 85% 65% (for charts, graphs, data visualizations, accent elements)
- Success Green: 142 71% 45%
- Warning Amber: 38 92% 50%
- Danger Red: 0 84% 60%

**Background & Surface (Light Mode):**
- Background: 220 23% 97% (existing #F5F7FB)
- Surface: 0 0% 100% (white cards)
- Surface Secondary: 210 20% 98%

**Background & Surface (Dark Mode):**
- Background: 217 19% 18%
- Surface: 217 19% 27%
- Surface Secondary: 215 16% 30%

**Text Colors:**
- Primary Text: 217 91% 15% (light mode) / 210 17% 98% (dark mode)
- Secondary Text: 214 14% 53%
- Muted Text: 214 13% 68%

**Status Colors:**
- Running: 142 71% 45% (green)
- Paused: 215 16% 47% (gray)
- Completed: 197 71% 39% (blue)
- Draft: 215 16% 47% (gray)

**Data Visualization:**
- Chart Primary: 270 85% 65% (purple for main data lines/bars)
- Chart Secondary: 203 100% 52% (blue for secondary metrics)
- Chart Tertiary: 142 71% 45% (green for positive trends)
- Chart Gradient: Linear gradient from purple to blue for area charts

### B. Typography
- Font Family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif
- Headings: 600-700 weight
- Body: 400 weight
- Emphasis: 500-600 weight
- Page Titles: 18px / 600 weight
- Section Headings: 16px / 600 weight
- Card Titles: 14px / 500 weight
- Body Text: 14px / 400 weight
- Small Text: 12px / 400 weight

### C. Layout System
**Spacing Primitives**: Use Tailwind units of 2, 3, 4, 6, 8, 12 (0.5rem, 0.75rem, 1rem, 1.5rem, 2rem, 3rem)
- Card Padding: p-6
- Section Spacing: space-y-6
- Component Gap: gap-4
- Sidebar Width: 260px (expanded), 72px (collapsed)
- Top Bar Height: 64px

### D. Component Library

**Cards:**
- White background with subtle shadow (0 1px 3px rgba(0,0,0,0.1))
- Border radius: 8-12px
- Hover lift effect: subtle shadow increase + 1-2px translate up
- KPI cards include sparkline charts in purple/blue gradients

**Buttons:**
- Primary: Blue background, white text, 8px radius
- Secondary: White/surface background, border, 8px radius
- Outlined: Transparent background with blue border
- Icon buttons: 40px square, surface-secondary background, 8px radius
- All buttons have 150ms ease transitions

**Navigation:**
- Sidebar: Fixed left, 260px width, collapsible to 72px icon-only
- Nav items: 12px padding vertical, 24px horizontal, 8px radius
- Active state: Blue background with white text
- Hover state: Surface-secondary background

**Forms:**
- Input height: 40px
- Border: 1px solid border color
- Focus: Blue border with subtle shadow
- Radius: 6px
- Labels: 12px, 500 weight, text-secondary color

**Data Tables:**
- Header: Surface-secondary background, 14px/500 weight text
- Rows: White background, 1px border-light dividers
- Hover: Surface-secondary background
- Action icons: 20px size, text-secondary color, hover to text-primary
- Status badges: Pill-shaped with color-coded backgrounds

**Charts & Graphs:**
- Circular Gauge: 0-100 score with color bands (red <40, amber 40-70, green >70)
- Sparklines: 30-day trend lines in purple, 2px stroke width
- Progress Bars: 4px height, rounded ends, purple fill
- Animated chart drawing on page load (500ms ease)

**Modals:**
- Centered overlay with backdrop blur
- White card with 16px radius
- Max width: 600px for forms, 800px for previews
- Close button in top-right corner

**Notifications:**
- Toast style in top-right corner
- Icons on left (color-coded by type)
- Dismissible with X button
- Auto-dismiss after 5 seconds
- Dropdown from bell icon with timestamped list

**AI Suggestion Cards:**
- White background with blue/purple gradient border-left accent
- Icon in colored circle (blue for cart, purple for package)
- Title in 14px/500 weight
- Description in 12px/400 weight text-secondary
- Impact badge in green with percentage
- Two-button layout: "Create Pre-filled" (primary) + "Dismiss" (secondary)
- Hover X icon in top-right for quick dismiss

### E. Animations
Use sparingly - only for:
- Chart/gauge drawing on initial load (500ms ease)
- Card hover lift effects (150ms ease)
- Button scale on hover (150ms ease, scale 1.02)
- Page transitions (200ms fade)
- Loading spinners for data fetching

## Page-Specific Layouts

**Dashboard (Overview):**
- Peace of Mind banner at top (blue shield icon, dismissible)
- 4 KPI cards in grid (emails sent, open rate, click rate, balance) with sparkline charts
- Two-column layout: Account Quality gauge (left) + AI Suggestions feed (right)
- Recent Campaigns table below with 5 columns
- Quick Actions bar at bottom with 4 outlined buttons

**Campaigns Page:**
- Search bar with filter dropdown (status/type)
- Campaign cards/table with progress bars in purple
- Action icons: view (eye), play/pause, copy, delete
- Create Campaign button (primary, top-right)

**Templates Library:**
- Card grid layout (3 columns on desktop, 1 on mobile)
- Template preview thumbnails with variable tags
- Hover actions: Preview, Copy, Delete

**Billing & Payments:**
- Large wallet balance card with purple accent
- Quick add funds with preset amounts in grid
- Payment gateway selector (Cashfree/Razorpay/PayPal/Stripe)
- Transaction history table with export button
- Currency selector dropdown (USD/EUR/GBP/INR)

**Settings:**
- Three tabs: Sender Profiles, Preferences, Account
- Form layouts with left-aligned labels
- Toggle switches for boolean preferences
- Save button (primary, bottom-right)

## Images
No hero images required - this is a dashboard application focused on data visualization and functionality. All visual interest comes from charts, graphs, and data displays in purple/blue color schemes.