# Book Now - Karnataka Tourism Booking Platform

A comprehensive multi-tenant booking platform for Karnataka tourism, offering hotel bookings, vehicle rentals, and tourism place reservations.

## Project Structure

```
book-now/
└── prajwal shetty/
    ├── home.html              # Landing page with 3D carousel
    ├── login.html             # Authentication (Login/Signup)
    ├── logo.html              # Logo/branding page
    ├── qr-payment.png         # QR code for payments
    │
    ├── [a]Admin Pages/        # Admin role dashboards
    │   ├── ahotel.html        # Hotel admin dashboard
    │   ├── acar.html          # Vehicle admin dashboard
    │   └── atourism.html      # Tourism admin dashboard
    │
    ├── [b]Business Pages/      # Business owner dashboards
    │   ├── bhotel.html        # Hotel registration portal
    │   ├── bcar.html          # Vehicle registration portal
    │   └── btourism.html      # Tourism registration portal
    │
    └── [u]User Pages/         # End-user booking pages
        ├── uhotel.html         # Hotel booking & payment
        ├── ucar.html          # Vehicle booking
        └── utourism.html      # Tourism places booking
```

## Features

### User Features
- Browse hotels, vehicles, and tourism places
- Multi-step booking flow
- Payment via QR code (UPI)
- Multiple payment methods (UPI, Card, Net Banking)
- Booking confirmation

### Admin Features
- Dashboard with statistics
- Filter by city (Bengaluru, Mysuru, Coorg, Hampi, Gokarna)
- View pending/verified items
- Confirm/cancel bookings
- Export data to JSON

### Business Features
- Multi-step registration forms
- Document upload capability
- Property listing submission

## Technology Stack

| Component | Technology |
|-----------|------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Backend/Database | Firebase (Google) |
| Authentication | Firebase Authentication |
| Database | Firebase Firestore |
| Hosting | Firebase Hosting |

## Admin Credentials

**IMPORTANT**: Admin access is RESTRICTED to authorized personnel only.

### Admin Login Details

| Role | Email | Password |
|------|-------|----------|
| Admin | prajwal@gmail.com | prajwal12 |

### How to Access Admin Dashboard

1. Navigate to the login page
2. Select "Admin" role
3. A notice will appear showing the authorized admin credentials
4. Enter credentials:
   - Email: `prajwal@gmail.com`
   - Password: `prajwal12`
5. Click "Enter" to access the admin dashboard

### Security Restrictions

- **Only one admin account**: Admin access is restricted to a single authorized account
- **No admin registration**: Users cannot sign up as admin - registration as admin is disabled
- **Email verification**: Admin login requires the exact email `prajwal@gmail.com`
- **Password verification**: Admin login requires the exact password `prajwal12`
- **Google Sign-In restriction**: Only the authorized admin email can login as admin via Google

### Admin Dashboard URLs

- Hotel Admin: `ahotel.html`
- Vehicle Admin: `acar.html`
- Tourism Admin: `atourism.html`

## User Roles

| Role | Login URL | Description |
|------|-----------|-------------|
| Admin | ahotel.html | Full dashboard access, can approve/reject bookings |
| Business | bhotel.html | Can register hotels/vehicles/tourism services |
| User | uhotel.html | End customers who browse and book |

## Firebase Configuration

The application uses the following Firebase project:

```javascript
{
  apiKey: "AIzaSyBzlUz79MvbV98osbMniaddt3nltmtQyaM",
  authDomain: "book-now-935f2.firebaseapp.com",
  projectId: "book-now-935f2",
  storageBucket: "book-now-935f2.firebasestorage.app",
  messagingSenderId: "61818097207",
  appId: "1:61818097207:web:aade934f0fb93b975c79b2"
}
```

## Database Collections

| Collection | Purpose |
|------------|---------|
| `users` | User accounts with roles (admin/user/business) |
| `bookings` | All booking records (hotels, vehicles, tourism) |
| `businessRegistrations` | Business listings submitted by business users |

## Supported Cities

- Bengaluru
- Mysuru
- Coorg
- Hampi
- Gokarna
- Chikmagalur
- Mangalore
- Hubli
- And more...

## Getting Started

### Prerequisites
- A Firebase account
- Web browser with JavaScript enabled
- Internet connection

### Installation

1. Clone or download the repository
2. Configure Firebase credentials in each HTML file (if using a different Firebase project)
3. Open `home.html` in a web browser
4. Register a new account or login with existing credentials

### Setting Up Admin Access

To add a new admin user:

1. Create a Firebase Authentication user account
2. Manually add a document to Firestore `users` collection:
   ```json
   {
     "uid": "<user-uid>",
     "email": "admin@example.com",
     "role": "admin",
     "createdAt": "<timestamp>"
   }
   ```

## Design Theme

- Primary Color: Gold (#d4af37)
- Background: Black (#0a0a0a)
- Accent: Bronze (#b8941f)
- Typography: Playfair Display, Cormorant Garamond (Google Fonts)

## Security Notes

1. Firebase API keys are exposed in client-side JavaScript (standard for Firebase)
2. **Admin credentials are hardcoded** - Only `prajwal@gmail.com` with password `prajwal12` can access admin
3. **No admin self-registration** - Users cannot register as admin
4. Role-based access control is implemented at application level
5. QR payment system requires manual verification
6. For production, implement Firebase Security Rules for server-side validation

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## License

This project is for educational purposes.

## Contact

For questions or support, please contact the development team.
