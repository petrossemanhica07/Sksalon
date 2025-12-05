# SKsalon Design Guidelines

## Design Approach
**Reference-Based Hybrid**: Drawing from modern service platforms (Calendly, Square Appointments) combined with Canva's warm, approachable aesthetic and WhatsApp's familiar chat patterns for the messaging component.

## Core Design Principles
1. **Professional Warmth**: Balance professionalism with approachable, salon-friendly aesthetics
2. **Native App Feel**: Smooth transitions, instant feedback, mobile-first responsive design
3. **Clear Hierarchy**: Distinct visual separation between client and admin interfaces
4. **Trust & Credibility**: Clean layouts that inspire confidence in booking decisions

---

## Typography System

**Primary Font**: Plus Jakarta Sans (via Google Fonts)
- Headings: 700 weight, sizes ranging from text-3xl to text-5xl
- Subheadings: 600 weight, text-xl to text-2xl
- Body: 400-500 weight, text-base
- Small text/labels: 500 weight, text-sm

**Secondary Font**: Inter (for data-heavy sections like schedules/pricing)
- Tables and calendars: 500 weight
- Buttons: 600 weight, uppercase tracking

---

## Layout & Spacing

**Spacing Primitives**: Use Tailwind units of **2, 4, 6, 8, 12, 16** exclusively
- Component padding: p-4 to p-8
- Section spacing: py-12 to py-16
- Card gaps: gap-6
- Grid gutters: gap-8

**Container Strategy**:
- Admin dashboard: Full-width sidebars (w-64), main content max-w-7xl
- Client views: max-w-6xl centered containers
- Forms: max-w-2xl for optimal readability

---

## Component Library

### Navigation
**Admin Sidebar**: Fixed left navigation (w-64) with icon+label menu items, collapsible on mobile to hamburger
**Client Header**: Sticky top navigation with logo, primary nav links, user avatar dropdown, notification bell with badge

### Hero Section
Full-width hero with salon ambiance image background (blurred overlay), centered logo upload area, welcoming headline, primary CTA button ("Agendar Agora"), secondary button ("Ver Serviços")

### Service Catalog
Masonry-style grid (3 columns desktop, 2 tablet, 1 mobile) with:
- Large service image cards
- Service name (text-xl, bold)
- Duration badge
- Price (prominent, text-2xl)
- "Agendar" CTA button
- Hover effect: lift shadow (shadow-lg)

### Appointment Booking Interface
**Calendar Component**: 
- Month/week toggle view
- Color-coded availability (available: green accents, booked: gray, your appointments: primary color)
- Time slot grid with 30-minute increments
- Staff member selector with avatar thumbnails

**Queue Management Display**:
- Live counter showing position (#3 na fila)
- Estimated wait time (circular progress indicator)
- Staff availability status (online/offline badges with pulse animation)

### Chat Interface (WhatsApp-style)
Two-column layout:
- Left: Conversation list with avatars, last message preview, unread badges
- Right: Active chat with message bubbles (client messages align right with primary background, admin messages align left with neutral background)
- Fixed bottom input with emoji picker icon, attachment icon, send button
- Typing indicators with animated dots

### Admin Dashboard Cards
Grid of metric cards (grid-cols-1 md:grid-cols-2 lg:grid-cols-4):
- Large number display (text-4xl)
- Descriptive label
- Trend indicator (↑ with percentage)
- Quick action button
- Subtle gradient backgrounds

### Promotions Section
Banner-style cards with:
- Bold discount percentage (text-6xl)
- Promotion description
- Countdown timer component
- Validity period
- "Resgatar Oferta" button with urgency styling

### Forms & Inputs
Floating label style inputs with:
- Border focus states
- Error states with red accent and helper text
- Success states with green checkmark icon
- Consistent height (h-12)
- Rounded corners (rounded-lg)

### Product Catalog
Card grid with:
- Product image (aspect-ratio-square)
- Product name and category tag
- Price with old price strikethrough if discounted
- Stock status badge
- "Adicionar ao Carrinho" button

---

## Images

**Hero Section**: Full-width salon interior shot showing styling stations, warm lighting, professional atmosphere (1920x800px)

**Service Gallery**: High-quality before/after style photos, hairstyle examples, braiding patterns (square format, 600x600px minimum)

**Staff Photos**: Professional headshots with circular masks for calendar/queue displays (400x400px)

**Product Images**: Clean product photography with white/neutral backgrounds (square format, 800x800px)

**Background Textures**: Subtle geometric patterns for section dividers, very low opacity

---

## Interaction Patterns

**Micro-interactions**:
- Button press: slight scale down (transform scale-95)
- Card hover: subtle lift with increased shadow
- Loading states: skeleton screens with shimmer effect
- Success actions: checkmark animation with confetti particles
- Form submission: progress stepper with active state highlighting

**Real-time Updates**:
- New appointment: toast notification slides from top-right
- Queue position change: number animation with color pulse
- Chat message: gentle bounce animation on new message bubble
- Availability change: calendar cell color fade transition

**Navigation**:
- Page transitions: fade-in content with slight upward movement
- Modal overlays: backdrop blur with scale-in animation
- Drawer menus: slide from left/right with overlay

---

## Accessibility

- Minimum touch target: 44x44px for all interactive elements
- ARIA labels on all icon-only buttons
- Keyboard navigation support with visible focus indicators (ring-2 ring-offset-2)
- Color contrast ratios meeting WCAG AA standards minimum
- Screen reader announcements for real-time updates
- Form validation with both visual and text feedback

---

## Responsive Breakpoints

- Mobile: Full-width cards, stacked layouts, bottom navigation
- Tablet (md): 2-column grids, side drawer navigation
- Desktop (lg+): 3-4 column grids, persistent sidebars, multi-column dashboards

This design creates a comprehensive, professional salon management experience that balances visual appeal with functional efficiency.