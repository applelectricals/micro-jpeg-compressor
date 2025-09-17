# MicroJPEG - Professional Image Compression Application

A comprehensive web application for JPEG image compression with premium subscription features.

## Features

### Core Compression
- Customizable quality settings
- Resize options
- Multiple output formats (JPEG, PNG, WEBP, AVIF)
- Special format conversions (RAW, SVG, TIFF)

### User Tiers
- **Anonymous**: 500 operations/month, 25/day, 5/hour
- **Free**: 500 operations/month, 25/day, 5/hour
- **Premium**: 10,000 operations/month, unlimited daily/hourly
- **Enterprise**: 50,000 operations/month, unlimited daily/hourly

### Technology Stack
- **Frontend**: React 18 (TypeScript), Vite, Tailwind CSS, shadcn/ui
- **Backend**: Express.js (TypeScript), Sharp for image processing
- **Database**: PostgreSQL with Drizzle ORM
- **Payment**: Stripe integration
- **Email**: SendGrid
- **Authentication**: Replit Auth

## Getting Started

### Prerequisites
- Node.js 18+
- PostgreSQL database
- Required environment variables:
  - `DATABASE_URL`
  - `STRIPE_SECRET_KEY`
  - `SENDGRID_API_KEY`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/applelectricals/micro-jpeg-compressor.git
   cd micro-jpeg-compressor
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables in `.env`

4. Run database migrations:
   ```bash
   npm run db:push
   ```

5. Start the development server:
   ```bash
   npm run dev
   ```

The application will be available at `http://localhost:5000`

## Project Structure

```
├── client/           # React frontend
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Application pages
│   │   ├── lib/          # Utilities and helpers
│   │   └── hooks/        # Custom React hooks
├── server/           # Express.js backend
│   ├── routes.ts     # API routes
│   ├── storage.ts    # Data storage interface
│   └── index.ts      # Server entry point
├── shared/           # Shared types and schemas
│   └── schema.ts     # Database schema and types
└── package.json      # Dependencies and scripts
```

## API Endpoints

- `POST /api/compress` - Image compression
- `POST /api/convert-special` - Special format conversion
- `GET /api/usage-stats` - User usage statistics
- `POST /api/auth/login` - User authentication
- `POST /api/stripe/webhook` - Stripe payment webhook

## Deployment

The application can be deployed to various platforms:

### Vercel
1. Connect your GitHub repository to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy with automatic builds

### Railway/Render
1. Connect repository to platform
2. Configure build and start commands:
   - Build: `npm run build`
   - Start: `npm start`

## Environment Variables

```bash
# Database
DATABASE_URL=postgresql://...

# Stripe Payments  
STRIPE_SECRET_KEY=sk_...
VITE_STRIPE_PUBLIC_KEY=pk_...

# Email Service
SENDGRID_API_KEY=SG...

# Optional
REDIS_URL=redis://...
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.

## Support

For support, please contact [your-email@example.com] or open an issue on GitHub.

---

Built with ❤️ using React, TypeScript, and Express.js
