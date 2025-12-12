# ECONOTRACK
## UI/UX Documentation
### Financial Growth Application

---

## 1. Introduction

**EconoTrack** is a mobile application designed to help users build financial habits that support sustainable economic growth. The platform provides comprehensive financial management tools including savings tracking, income/expense monitoring, and career development resources to empower users in their financial journey.

### Key Features:
- **Savings Tracker**: Track and grow savings with detailed entry management
- **Income vs Expenses**: Monitor monthly financial flow and remaining balance
- **Career Development Tips**: Access professional growth resources and productivity tips
- **User Authentication**: Secure Firebase-based authentication system

### UN SDG Alignment:
SDG 8 (Decent Work and Economic Growth) - Supporting users in building sustainable financial habits and career development.

### Target Platform:
Android mobile application built with Kotlin

---

## 2. Color Palette

### Primary Colors

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Background Dark** | `#0F1419` | Main app background |
| **Background Darker** | `#0A0E13` | Secondary background elements |
| **Surface** | `#1E2A3A` | Card backgrounds, elevated surfaces |
| **Black** | `#000000` | Login screen background |

### Accent Colors - Teal

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Teal Primary** | `#26A69A` | Primary accent, feature icons |
| **Teal Dark** | `#00796B` | Gradient end, darker accents |
| **Teal Medium** | `#00897B` | Gradient center |
| **Teal Light** | `#4DB6AC` | Hover states, highlights |

### Gradient Colors

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Gradient Start** | `#667EEA` | Purple gradient start |
| **Gradient End** | `#764BA2` | Purple gradient end |

### Text Colors

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Text Primary** | `#FFFFFF` | Primary text, headings |
| **Text Secondary** | `#9E9E9E` | Secondary text, descriptions |
| **Text Hint** | `#616161` | Input hints, placeholders |
| **Text Muted** | `#8E8E93` | Subtle text, labels |
| **Text Description** | `#B0BEC5` | Long descriptions |
| **Text Feature** | `#7E8B9A` | Feature card descriptions |

### Input & Interactive Colors

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Input Background** | `#1E1E1E` | Input field backgrounds |
| **Input Stroke** | `#333333` | Default input borders |
| **Input Stroke Focused** | `#FFFFFF` | Active input borders |

### Icon Background Colors

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| **Icon BG Teal** | `#26A69A` | Savings Tracker icon |
| **Icon BG Blue** | `#2196F3` | Income/Expenses icon |
| **Icon BG Purple** | `#9C27B0` | Career Tips icon |

---

## 3. Typography

### Font Family
**Poppins** - Google Fonts

### Font Weights Used
- **Poppins Regular** - Body text, descriptions
- **Poppins Bold** - Headings, titles, buttons
- **Poppins Black** - Hero text, emphasis

### Typography Scale

| Element | Font Size | Font Weight | Color | Usage |
|---------|-----------|-------------|-------|-------|
| **Hero Title** | 40sp | Bold | White | Main screen titles |
| **App Title** | 28sp | Bold | White | App branding |
| **Page Heading** | 24sp | Bold | White | User names, section headers |
| **Section Title** | 18sp | Bold | White | Feature section headers |
| **Feature Title** | 16sp | Bold | White | Feature card titles |
| **Body Large** | 16sp | Regular | White/Muted | Subtitles, descriptions |
| **Body Medium** | 15sp | Regular | White | Input fields |
| **Body Small** | 14sp | Regular | Text Secondary | App descriptions |
| **Caption** | 13sp | Regular | Text Feature | Feature descriptions |
| **Label** | 14sp | Regular | White | Input labels |

### Line Spacing
- Body text: `lineSpacingExtra="2dp"`
- Default system line spacing for headings

---

## 4. Screen Documentation

### 4.1 Login Screen (MainActivity)

**Purpose**: User authentication entry point

**Layout Components**:
- Welcome title ("Welcome Back")
- Subtitle ("Sign in to continue")
- Email input field with icon
- Password input field with toggle visibility
- Forgot password link
- Sign in button
- Sign up link

**Color Scheme**:
- Background: Black (#000000)
- Text: White (#FFFFFF)
- Input backgrounds: Custom rounded dark
- Button: White with black text

**Interactions**:
- Email validation
- Password visibility toggle
- Firebase authentication
- Navigation to Register screen
- Navigation to Home on successful login

---

### 4.2 Register Screen (RegisterActivity)

**Purpose**: New user account creation

**Layout Components**:
- Registration header
- Full name input field
- Email input field
- Password input field
- Confirm password input field
- Register button
- Sign in link

**Color Scheme**:
- Background: Dark theme
- Form fields: Consistent with login screen
- Validation indicators

**Interactions**:
- Form validation
- Password confirmation matching
- Firebase user creation
- Firestore user data storage
- Auto-navigation to Home on success

---

### 4.3 Home Screen (HomeActivity)

**Purpose**: Main dashboard and navigation hub

**Layout Structure**:

**Header Section**:
- App icon (✦)
- App title: "EconoTrack"
- Subtitle: "Financial Growth App"
- Background: Teal gradient (#26A69A to #00796B)

**Welcome Card**:
- "Welcome back" greeting
- User's full name (capitalized)
- App description with UN SDG 8 alignment
- Background: Dark card with rounded corners

**Features Section**:
Three feature cards with consistent layout:

1. **Savings Tracker Card**
   - Icon: 🐷
   - Icon background: Teal (#26A69A)
   - Title: "Savings Tracker"
   - Description: "Track and grow your savings"
   - Arrow indicator

2. **Income vs Expenses Card**
   - Icon: 📈
   - Icon background: Blue (#2196F3)
   - Title: "Income vs Expenses"
   - Description: "Monitor your financial flow"
   - Arrow indicator

3. **Career Tips Card**
   - Icon: 💼
   - Icon background: Purple (#9C27B0)
   - Title: "Career Tips"
   - Description: "Grow your professional skills"
   - Arrow indicator

**Logout Section**:
- Centered logout button
- Arrow icon (↗)
- Muted styling

**Interactions**:
- Firebase user data loading
- Navigation to each feature screen
- Logout functionality
- Ripple effects on card taps

---

### 4.4 Savings Tracker Screen (SavingsTrackerActivity)

**Purpose**: Track and manage savings entries

**Layout Components**:
- Header with gradient background
- Total savings display
- Add savings input fields
- Savings entries list (RecyclerView)
- Empty state message

**Features**:
- Add new savings entries with amount and description
- Display list of all savings
- Calculate and show total savings
- Delete individual entries
- Real-time Firebase sync

**Color Scheme**:
- Header: Teal-blue gradient
- Cards: Dark surface color
- Accent: Teal for positive amounts

---

### 4.5 Income vs Expenses Screen (IncomeExpensesActivity)

**Purpose**: Monitor monthly financial flow

**Layout Components**:
- Header with gradient
- Monthly income input/display
- Monthly expenses input/display
- Remaining balance calculation
- Update finances button
- Financial summary section

**Features**:
- Input monthly income
- Input monthly expenses
- Auto-calculate remaining balance
- Color-coded balance (green for positive, red for negative)
- Firebase data persistence

**Color Scheme**:
- Header: Gradient background
- Positive balance: Green/Teal
- Negative balance: Red (warning)

---

### 4.6 Career Tips Screen (CareerTipsActivity)

**Purpose**: Provide career development resources

**Layout Components**:
- Header with purple gradient
- Subtitle: "Grow your career and boost productivity"
- Tips list (RecyclerView)
- Tip cards with badges

**Features**:
- Display career development tips
- Categorized tips (Networking, Skills, Productivity, etc.)
- Category badges with color coding
- Scrollable list of tips

**Color Scheme**:
- Header: Purple gradient (#9C27B0)
- Tip cards: Dark surface
- Badges: Category-specific colors

---

## 5. Design Specifications

### Border Radius
- Cards: `20dp`
- Input fields: `12dp` (rounded style)
- Buttons: `12dp`
- Icon backgrounds: `16dp`

### Padding & Spacing
- Screen horizontal padding: `28dp`
- Card padding: `24dp`
- Feature card padding: `20dp`
- Input field padding: `16dp` (vertical), `18dp` (horizontal)
- Section spacing: `24dp`
- Card spacing: `12dp`

### Elevation & Shadows
- Cards: Subtle shadow using drawable shapes
- No material elevation (dark theme optimized)

### Icon Sizes
- Feature icons: `28sp` (emoji size)
- Icon containers: `56dp x 56dp`
- Input icons: `20dp x 20dp`
- Arrow indicators: `24sp`

### Button Specifications
- Height: `56dp` (standard touch target)
- Corner radius: `12dp`
- Text: 16sp, Bold
- Full-width on forms
- Centered text

### Input Field Specifications
- Minimum height: `56dp`
- Corner radius: `12dp`
- Icon size: `20dp`
- Icon margin: `14dp`
- Border width: `1dp`
- Focused border: `2dp`

---

## 6. Design Principles

### 1. Dark-First Design
The app uses a dark theme as the primary color scheme, optimized for:
- Reduced eye strain during extended use
- Better battery life on OLED screens
- Modern, professional aesthetic
- Focus on content with high contrast

### 2. Gradient Accents
Strategic use of gradients for:
- Visual hierarchy (headers)
- Feature differentiation
- Brand identity
- Depth and dimension

### 3. Color-Coded Features
Each major feature has its own accent color:
- Teal for Savings (growth, prosperity)
- Blue for Income/Expenses (stability, trust)
- Purple for Career (ambition, wisdom)

### 4. Minimalist Interface
- Clean layouts with ample white space
- Clear visual hierarchy
- Focused user flows
- No unnecessary decorative elements

### 5. Accessibility
- High contrast text (white on dark)
- Minimum 56dp touch targets
- Clear labels and descriptions
- Descriptive content descriptions for icons

### 6. Consistency
- Uniform card styles across screens
- Consistent spacing system
- Repeated interaction patterns
- Predictable navigation

### 7. Financial Focus
- Clear numerical displays
- Easy data entry
- Quick-glance summaries
- Positive reinforcement for savings

---

## 7. Component Library

### 7.1 Cards

**Feature Card**
```xml
- Layout: Horizontal LinearLayout
- Background: feature_card_bg.xml
- Padding: 20dp
- Corner radius: 16dp
- Contains: Icon container, Text content, Arrow
- Foreground: Ripple effect
```

**Welcome Card**
```xml
- Layout: Vertical LinearLayout
- Background: welcome_card_bg.xml
- Padding: 24dp
- Corner radius: 20dp
- Contains: Greeting text, user name, description
```

**Header Card**
```xml
- Layout: Vertical LinearLayout
- Background: Teal gradient
- Padding: 24dp
- Corner radius: 20dp (top)
- Contains: App icon, title, subtitle
```

### 7.2 Buttons

**Primary Button**
```xml
- Background: button_dark.xml (white)
- Height: 56dp
- Text: 16sp, Bold, Black
- Corner radius: 12dp
- Full width
```

**Logout Button**
```xml
- Background: logout_button_bg.xml
- Padding: 24dp (horizontal), 12dp (vertical)
- Text: 15sp, Regular, Muted
- Icon: Arrow (↗)
- Corner radius: 12dp
```

### 7.3 Input Fields

**Standard Input**
```xml
- Container: LinearLayout (horizontal)
- Background: input_rounded.xml
- Min height: 56dp
- Padding: 18dp (horizontal), 16dp (vertical)
- Contains: Icon (20dp), EditText, Optional toggle icon
- Corner radius: 12dp
- Border: 1dp (#333333), 2dp (#FFFFFF when focused)
```

### 7.4 Icon Containers

**Feature Icon Container**
```xml
- Size: 56dp x 56dp
- Background: Circular gradient
- Gravity: Center
- Contains: Emoji icon (28sp)
```

### 7.5 Text Components

**Section Header**
```xml
- Font: Poppins Bold
- Size: 18sp
- Color: White
- Prefix: Small colored dot (8dp)
```

**Feature Title**
```xml
- Font: Poppins Bold
- Size: 16sp
- Color: White
```

**Feature Description**
```xml
- Font: Poppins Regular
- Size: 13sp
- Color: #7E8B9A
- Margin top: 2dp
```

### 7.6 Gradients

**Teal Header Gradient**
```xml
- Angle: 135°
- Start: #26A69A
- Center: #00897B
- End: #00796B
- Type: Linear
```

**Purple Gradient**
```xml
- Angle: 135°
- Start: #667EEA
- End: #764BA2
- Type: Linear
```

### 7.7 List Items

**Savings Entry Item**
```xml
- Layout: Card layout
- Contains: Amount, Description, Date, Delete button
- Background: Surface color
- Padding: 16dp
- Margin: 8dp (vertical)
```

**Career Tip Item**
```xml
- Layout: Card layout
- Contains: Category badge, Tip icon, Title, Description
- Background: Surface color
- Padding: 20dp
```

---

## 8. Implementation Notes

### 8.1 Technology Stack
- **Language**: Kotlin
- **Framework**: Android SDK
- **Backend**: Firebase (Authentication, Firestore)
- **UI Components**: Material Design Components (customized)
- **Font Loading**: Google Fonts (Poppins)

### 8.2 Key Dependencies
```gradle
- Firebase Authentication
- Firebase Firestore
- Material Design Components
- AndroidX Libraries
- Google Fonts Provider
```

### 8.3 Data Models

**User Model**
```kotlin
data class User(
    val fullName: String,
    val email: String
)
```

**Savings Entry Model**
```kotlin
data class SavingsEntry(
    val amount: Double,
    val description: String,
    val timestamp: Long
)
```

**Finance Data Model**
```kotlin
data class FinanceData(
    val monthlyIncome: Double,
    val monthlyExpenses: Double,
    val remainingBalance: Double
)
```

**Career Tip Model**
```kotlin
data class CareerTip(
    val title: String,
    val description: String,
    val category: String
)
```

### 8.4 Navigation Flow
```
MainActivity (Login)
    ├─→ RegisterActivity
    └─→ HomeActivity
            ├─→ SavingsTrackerActivity
            ├─→ IncomeExpensesActivity
            ├─→ CareerTipsActivity
            └─→ Logout → MainActivity
```

### 8.5 Firebase Structure

**Firestore Collections**:
- `users/{userId}` - User profile data
- `users/{userId}/savings` - Savings entries
- `users/{userId}/finances` - Income/expense data

### 8.6 Responsive Design
- ScrollView containers for all main screens
- Edge-to-edge display with system bar insets
- Keyboard handling for input screens
- Dynamic content sizing

### 8.7 State Management
- Firebase real-time listeners
- Local data caching
- RecyclerView adapters for lists
- LiveData/ViewModel pattern (if implemented)

### 8.8 Accessibility Features
- Content descriptions for all icons
- Minimum touch target sizes (56dp)
- High contrast ratios
- Scalable text sizes
- Screen reader compatible

### 8.9 Performance Optimizations
- Lazy loading of list items
- Image and icon optimization
- Efficient Firebase queries
- Proper activity lifecycle management
- Memory leak prevention

### 8.10 Code Organization
```
com.example.loginformpractice/
├── Activities
│   ├── MainActivity.kt (Login)
│   ├── RegisterActivity.kt
│   ├── HomeActivity.kt
│   ├── SavingsTrackerActivity.kt
│   ├── IncomeExpensesActivity.kt
│   └── CareerTipsActivity.kt
├── Adapters
│   ├── SavingsAdapter.kt
│   └── CareerTipsAdapter.kt
└── Models
    ├── User.kt
    ├── SavingsEntry.kt
    ├── FinanceData.kt
    └── CareerTip.kt
```

### 8.11 Drawable Resources
- Gradient backgrounds (XML shapes)
- Button styles (XML shapes)
- Input field backgrounds (XML shapes)
- Icon backgrounds (XML shapes)
- Ripple effects (XML ripples)

### 8.12 Future Enhancements
- Data visualization (charts/graphs)
- Budget planning features
- Savings goals with progress tracking
- Export financial reports
- Notifications and reminders
- Dark/Light theme toggle
- Multi-language support
- Offline mode with sync

---

## Design Credits

**Design System**: Custom dark theme with teal accents
**Font**: Poppins by Google Fonts
**Icons**: Material Design Icons + Custom emoji icons
**Color Philosophy**: Dark UI optimized for financial applications
**Alignment**: UN Sustainable Development Goals (SDG 8)

---

**Document Version**: 1.0
**Last Updated**: December 2025
**Maintained By**: Development Team
