<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# 主日學教師支援工具 (Sunday School Teacher Support Tool)

A comprehensive AI-powered Church administration and teaching support application with MongoDB Atlas integration for data persistence.

View your app in AI Studio: https://ai.studio/apps/drive/12XnGnPpRVxh_r20K-dnTd97dF-0bq4S7

## Features

✨ **Class Arrangement Management**
- Create, edit, and delete class arrangements
- Store data in MongoDB Atlas for persistence
- Export arrangements as JSON backup files
- Import arrangements from JSON files
- Password-protected management interface

🤖 **AI-Powered Teaching Support**
- Generate lesson plans with Google Gemini AI
- Customizable AI personas for different teaching styles
- Creative activity and discussion question generation
- Tailored content for different age groups

📱 **Modern UI**
- Responsive design built with Tailwind CSS v4
- Clean, intuitive interface
- Real-time loading states and error handling

## Run Locally

**Prerequisites:**  Node.js 18+

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Set up environment variables:**

   Create a `.env.local` file based on `.env.example`:
   ```env
   VITE_API_KEY=your_gemini_api_key_here
   MONGODB_URI=your_mongodb_connection_string_here
   ```

   - Get your Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
   - See [MONGODB_SETUP.md](./MONGODB_SETUP.md) for MongoDB Atlas setup instructions

3. **Run the development server:**
   ```bash
   npm run dev
   ```

4. **Open your browser:**
   Navigate to `http://localhost:3000` (or the port shown in terminal)

## Deploy to Vercel

### Quick Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

### Manual Deployment

1. **Push your code to GitHub**

2. **Import to Vercel:**
   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "Add New Project"
   - Import your GitHub repository

3. **Configure Environment Variables:**

   Add these in Vercel → Settings → Environment Variables:

   | Name | Value | Description |
   |------|-------|-------------|
   | `VITE_API_KEY` | Your Gemini API key | For AI features |
   | `MONGODB_URI` | Your MongoDB connection string | For data persistence |

4. **Deploy:**
   Click "Deploy" and wait for the build to complete

## MongoDB Atlas Setup

For detailed instructions on setting up MongoDB Atlas, see [MONGODB_SETUP.md](./MONGODB_SETUP.md).

Quick steps:
1. Create a free MongoDB Atlas account
2. Create a cluster (free tier available)
3. Create a database user
4. Whitelist your IP (or allow from anywhere for Vercel)
5. Get your connection string
6. Add to environment variables

## Project Structure

```
├── api/                    # API routes for serverless functions
│   ├── arrangements.ts     # CRUD operations for arrangements
│   └── index.ts           # Main API handler
├── components/            # React components
│   ├── common/           # Reusable UI components
│   └── ...               # Feature-specific components
├── hooks/                # Custom React hooks
│   ├── useArrangements.ts # Hook for MongoDB integration
│   └── useLocalStorage.ts # Local storage hook
├── lib/                  # Utilities
│   └── mongodb.ts       # MongoDB connection
├── services/            # Service layer
│   ├── arrangementService.ts # Client-side API calls
│   └── geminiService.ts     # AI integration
├── App.tsx             # Main application component
├── index.css          # Global styles with Tailwind
├── types.ts          # TypeScript type definitions
└── constants.ts     # App constants

```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally

## Data Management

### Export Data
1. Go to "課程" (Classes) section
2. Click "管理課程" (Manage Classes) - Password: `cklbckoho`
3. Click "匯出" (Export) button
4. JSON file will be downloaded with timestamp

### Import Data
1. Go to "課程" (Classes) section
2. Click "管理課程" (Manage Classes) - Password: `cklbckoho`
3. Click "匯入" (Import) button
4. Select your JSON backup file

## Technologies Used

- **Frontend:** React 19, TypeScript
- **Styling:** Tailwind CSS v4
- **Build Tool:** Vite
- **Database:** MongoDB Atlas
- **AI:** Google Gemini API
- **Deployment:** Vercel
- **API:** Vercel Serverless Functions

## Troubleshooting

### Build Errors
- Make sure you have Node.js 18+ installed
- Delete `node_modules` and run `npm install` again
- Check that all environment variables are set

### MongoDB Connection Issues
- Verify your connection string is correct
- Check that your IP is whitelisted in MongoDB Atlas
- Ensure the database user has read/write permissions

### API Errors
- Check browser console for detailed errors
- Verify environment variables are set in Vercel
- Check Vercel deployment logs

## Support

For issues and questions:
- Check [MONGODB_SETUP.md](./MONGODB_SETUP.md) for database setup
- Review browser console for error messages
- Check Vercel deployment logs

## License

Copyright © 2025. All rights reserved.
