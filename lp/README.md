# 令和ボイス (Reiwa Voice) - Landing Page

Professional civic tech website for "令和ボイス" - a non-profit civic tech platform that converts citizen voices into formal petitions delivered to local governments by elected officials.

## Files Created

### 1. **index.html** - Landing Page
- Hero section with gradient background and call-to-action buttons
- Stats bar loaded from Google Sheets CSV
- 3-step process explanation
- Recent petitions grid (last 4 from CSV)
- Trust/credibility cards
- Final CTA section
- Features: CSV data loading, dynamic stats calculation

### 2. **about.html** - How It Works Page
- Detailed 5-step process with numbered steps
- FAQ section with accordion toggle functionality
- Non-profit statement section
- Professional typography and spacing

### 3. **petitions.html** - Petitions List Page
- Filter bar (status, prefecture, keyword search)
- Petition cards in responsive grid
- Pagination system
- Dynamic data loading from Google Sheets
- Status badges with color coding
- Like count display

### 4. **results.html** - Results/Activity Page
- Stats overview (petitions, submitted, approved, likes)
- List of submitted/approved petitions
- Detailed petition cards with meta information
- Empty state handling

### 5. **team.html** - Team Page
- Team member cards with images and quotes
  - へずまりゅう (Representative/Nara City Councilor)
  - 丸吉孝文 (Secretary/Developer/AI Engineer)
- Recruitment section for supporting members
- All 47 prefectures grid (Nara highlighted as active)

### 6. **form.html** - Form Submission Guide
- Clear explanation of the submission process
- Step-by-step flow explanation
- Privacy notice and FAQs
- Google Form embed/link: https://docs.google.com/forms/d/e/1FAIpQLSdYMoS5_MkVQFoRoMxrPFbFnxCGx0QrFf-_JA5bVOqSZ5FHIA/viewform
- Privacy assurance messaging

### 7. **privacy.html** - Privacy Policy
- Comprehensive privacy policy with 16 sections
- Clear explanation of data handling
- Non-profit and citizen-focused approach
- Data security information
- Contact information
- Last updated: 2025-03-05

## Design Features

### Color Scheme
- **Primary**: #1e40af (Deep Blue) - Trust, authority
- **Secondary**: #059669 (Green) - Growth, positive change
- **Background**: #ffffff (White) - Clean, professional
- **Gray surfaces**: #f8fafc - Subtle separation

### CSS Features
- CSS Variables for consistent theming
- Mobile-responsive with hamburger menu
- Smooth transitions and hover effects
- Card-based UI with subtle shadows
- Grid layouts for petitions and stats
- Sticky header navigation
- Professional typography

### Key Components
- **Header**: Sticky navigation with logo and mobile menu
- **Footer**: Consistent across all pages with links and non-profit badge
- **Navigation**: 5 main links + CTA button
- **Cards**: Reusable card components for petitions, stats, team members
- **Forms**: Filter bars, search, status badges
- **Data Loading**: CSV parsing via fetch API

## Data Integration

### Google Sheets CSV
- **URL**: https://docs.google.com/spreadsheets/d/e/2PACX-1vQpmRYjyz365eM2kyhPenekUNsQSNF_0o7tDnBve_K7djXMs7WQocFWhjLSfysuFdY3Bp0tKhh0tK2y/pub?gid=1599355687&single=true&output=csv
- **Column Mapping**:
  - 0: timestamp
  - 1: prefecture
  - 2: municipality
  - 3: age
  - 4: gender
  - 5: category
  - 6: status
  - 7: petitionUrl
  - 8: likeCount
  - 9: title

### GAS API
- **URL**: https://script.google.com/macros/s/AKfycbzl9Qt83DpHWsE6QaUY6VCuofFsoABP33d6Bq-7uCSGoEnOjxnyKN4paQNH0oA9t7Nn6w/exec
- **Secret**: reiwa2024voice!secure

## Image Assets Required

The site references:
- `../images/hezuma.jpg` - へずまりゅう profile photo
- `../images/maruyoshi.jpg` - 丸吉孝文 profile photo

These should be placed in `/sessions/confident-nifty-sagan/mnt/outputs/images/` directory.

## Status Badges

Petitions use color-coded status badges:
- **募集中 (Recruiting)**: Blue (#3b82f6)
- **準備中 (Preparing)**: Orange (#f59e0b)
- **送付済 (Submitted)**: Purple (#8b5cf6)
- **承認済 (Approved)**: Green (#10b981)

## Mobile Responsiveness

All pages feature:
- Hamburger menu for mobile navigation
- Responsive grid layouts
- Touch-friendly buttons (1rem padding)
- Readable text sizing (16px minimum)
- Stacked layouts on small screens

## Non-Profit Messaging

Every page emphasizes:
- "✅ 非営利サービス｜完全無料" (Non-profit service | Completely free)
- Clear privacy protection messaging
- Mission-driven language
- Transparency about operations

## JavaScript Features

### On All Pages
- `toggleNav()` - Mobile hamburger menu toggle

### Index Page
- `loadStats()` - Async CSV data loading and calculation
- `loadRecentPetitions()` - Load and display last 4 petitions
- Status color and label functions

### Petitions Page
- `filterPetitions()` - Multi-filter functionality
- `renderPetitions()` - Dynamic card rendering
- `renderPagination()` - Pagination controls
- `changePage()` - Page navigation

### Results Page
- `loadResults()` - Load submitted petitions from CSV
- `renderResults()` - Display with detail cards

### Team Page
- `initPrefectures()` - Initialize 47 prefecture grid

### About Page
- `toggleFaq()` - FAQ accordion toggle

## Accessibility Considerations

- Semantic HTML structure
- Clear heading hierarchy
- Color-coded elements supplemented with text labels
- Sufficient color contrast
- Mobile-friendly touch targets
- Form labels and inputs properly associated

## Performance Notes

- Inline CSS (no external stylesheet requests)
- Async data loading to prevent blocking
- Efficient grid layouts
- Minimal JavaScript
- CSV parsing is fast for typical data sizes

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Next Steps

1. Add image assets to `/images/` directory
2. Test CSV data loading
3. Configure email for form submissions
4. Set up analytics if needed
5. Deploy to production server
6. Enable HTTPS for secure data transmission

---

Created: 2025-03-05
Non-profit Civic Tech Service
