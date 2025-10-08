# Library Management System Design Guidelines

## Design Approach
**Utility-Focused Dashboard Design** - Following established patterns from Koha and modern library catalog interfaces, prioritizing data density, efficient workflows, and clear information hierarchy. This is a productivity tool where usability and quick task completion are paramount.

## Color System

**Primary Palette:**
- Primary: #2C5282 (Navy Blue) - Headers, primary actions, navigation
- Secondary: #38A169 (Forest Green) - Success states, available books
- Warning: #D69E2E (Amber) - Due soon alerts, warnings
- Accent: #805AD5 (Purple) - Highlights, active states
- Danger: #E53E3E (Red) - Overdue items, critical alerts

**Neutral Palette:**
- Background: #F7FAFC (Light Blue-Grey) - Main background
- Surface: #FFFFFF - Cards, tables, modals
- Text Primary: #2D3748 (Charcoal) - Main text
- Text Secondary: #718096 - Supporting text, labels
- Border: #E2E8F0 - Dividers, table borders

**Status Colors:**
- Available: #38A169 (Forest Green)
- Checked Out: #3182CE (Blue)
- Overdue: #E53E3E (Red)
- Due Soon: #D69E2E (Amber)

## Typography

**Font Families:**
- Primary: 'Inter', system-ui, sans-serif (headings, UI elements)
- Secondary: 'Source Sans Pro', system-ui, sans-serif (body text, data tables)

**Type Scale:**
- Page Title: 32px/40px, font-weight: 600
- Section Header: 24px/32px, font-weight: 600
- Card Title: 18px/24px, font-weight: 500
- Body Text: 16px/24px, font-weight: 400
- Table Data: 14px/20px, font-weight: 400
- Labels: 14px/20px, font-weight: 500
- Small Text: 12px/16px, font-weight: 400

## Layout System

**Spacing Scale (Tailwind Units):**
- Use consistent spacing: 2, 4, 6, 8, 12, 16 units
- Section padding: p-6 to p-8
- Card padding: p-6
- Table cells: px-4 py-3
- Button padding: px-6 py-2.5
- Form fields: p-3

**Grid System:**
- Dashboard Layout: Sidebar (280px) + Main content area
- Content max-width: 1400px for tables, 1200px for forms
- Card grids: 1 column mobile, 2-3 columns tablet, 3-4 columns desktop
- Table: Full-width responsive with horizontal scroll on mobile

## Component Library

**Navigation:**
- Left sidebar with collapsible sections
- Top bar with search, notifications, user profile
- Breadcrumb navigation for context
- Active state: Left border accent (4px) in primary color

**Data Tables:**
- Zebra striping for rows (alternating background #F7FAFC)
- Sticky header on scroll
- Sortable columns with arrow indicators
- Row hover: background #EDF2F7
- Pagination controls at bottom
- Action buttons: icon-only on hover for space efficiency
- Filters: Collapsible panel above table

**Cards:**
- White background with subtle shadow (0 1px 3px rgba(0,0,0,0.1))
- 12px border-radius
- Book cards: Cover thumbnail + title/author/ISBN/status badge
- Borrower cards: Avatar + name/contact/active loans count
- Hover effect: Slight elevation increase

**Forms:**
- Label above input pattern
- Input fields: border #E2E8F0, focus ring primary color
- Required fields: asterisk in danger color
- Error states: Red border + error message below
- Success states: Green checkmark icon
- Multi-step forms: Progress indicator at top

**Buttons:**
- Primary: Solid primary color, white text
- Secondary: Outline primary color, primary text
- Success: Solid secondary color (green), white text
- Danger: Solid red, white text
- Ghost: Transparent with hover background
- Icon buttons: 40px square, centered icon
- Heights: 40px standard, 36px compact, 48px large

**Status Badges:**
- Available: Green background #F0FFF4, green text #38A169
- Checked Out: Blue background #EBF8FF, blue text #3182CE
- Overdue: Red background #FFF5F5, red text #E53E3E
- Due Soon: Amber background #FEFCBF, amber text #D69E2E
- Shape: Rounded-full, px-3 py-1, 12px font-size

**Search & Filters:**
- Prominent search bar with icon
- Advanced filters: Dropdown panels
- Active filters: Removable chips/tags
- Clear all filters option
- Search suggestions dropdown

**Modals & Overlays:**
- Add/Edit book: Center modal, max-width 600px
- Delete confirmation: Smaller center modal
- Quick view: Slide-over panel from right
- Backdrop: rgba(0,0,0,0.5)
- Close button: Top-right, clearly visible

**Dashboard Widgets:**
- Summary cards: Total books, active loans, overdue count, available books
- Icon + large number + label format
- Color-coded based on metric type
- Quick action links in footer

**Charts & Visualizations:**
- Simple bar charts for lending trends
- Pie chart for category distribution
- Minimal styling, focus on data clarity
- Color scheme consistent with status colors

## Page-Specific Layouts

**Dashboard Home:**
- 4-column summary cards at top
- Recent activity feed (left 60%) + Quick actions (right 40%)
- Overdue alerts prominently displayed
- Upcoming due dates list

**Books Inventory:**
- Search bar + filter toggles at top
- View toggle: Table view / Card grid view
- Bulk action toolbar when items selected
- Add new book: Primary button top-right

**Borrowers:**
- Searchable table with avatar column
- Quick actions: View profile, Check borrowing history
- Add borrower: Slide-over form panel

**Checkout System:**
- Two-column layout: Book selection (left) + Borrower selection (right)
- Date picker for due date
- Summary panel showing all selections before confirm
- Barcode scanner integration visual cue

**Overdue Management:**
- Filtered table showing only overdue items
- Days overdue counter prominently displayed
- Bulk reminder sending capability
- Export overdue list functionality

## Interactive States

**Hover:**
- Table rows: Light grey background
- Cards: Subtle shadow elevation
- Buttons: Slight darkening of background

**Active/Focus:**
- Input fields: 2px ring in primary color
- Selected rows: Light primary background tint
- Active nav items: Left border + background tint

**Loading:**
- Skeleton screens for tables
- Spinner for button actions
- Progress bar for batch operations

## Responsive Behavior

**Desktop (1024px+):**
- Full sidebar visible
- Multi-column layouts active
- Table shows all columns

**Tablet (768px-1023px):**
- Collapsible sidebar with overlay
- 2-column max for cards
- Table: Hide less critical columns

**Mobile (<768px):**
- Bottom tab navigation
- Single column stacks
- Table: Card-based view or horizontal scroll
- Floating action button for primary actions

## Accessibility
- WCAG AA contrast ratios maintained
- Keyboard navigation for all interactions
- Clear focus indicators (2px ring)
- Screen reader labels for icon-only buttons
- Form validation announcements

This design system creates an efficient, professional library management interface that prioritizes data clarity, quick task completion, and organized workflows while maintaining visual consistency throughout the application.