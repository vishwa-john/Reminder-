# Voice Reminder & Alarm Web Application

A modern, full-stack web application that allows users to set voice reminders and alarms with an animated, responsive UI.

## Features

### Core Functionality
- **Voice Recording**: Record voice notes using the Web Speech API
- **Alarm System**: Set alarms with custom date/time
- **Real-time Monitoring**: Automatic alarm triggering at scheduled times
- **Text-to-Speech**: Playback of voice notes when alarms trigger
- **CRUD Operations**: Create, read, update, and delete reminders

### UI/UX Features
- **Animated RGB Background**: Smooth gradient animations using CSS keyframes
- **Responsive Design**: Optimized for desktop and mobile devices
- **Smooth Transitions**: Fluid animations on buttons, cards, and modals
- **Glass Morphism**: Modern backdrop-blur effects
- **Interactive Feedback**: Visual and audio cues for user actions

### Technical Features
- **Next.js App Router**: Modern React framework with server-side rendering
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first styling with custom animations
- **RESTful API**: Backend API routes for data management
- **In-memory Storage**: Simple data persistence (easily replaceable with database)

## Getting Started

### Prerequisites
- Node.js 18+ 
- Modern web browser with Web Speech API support

### Installation

1. Clone or download the project files
2. Install dependencies:
   \`\`\`bash
   npm install
   \`\`\`

3. Run the development server:
   \`\`\`bash
   npm run dev
   \`\`\`

4. Open [http://localhost:3000](http://localhost:3000) in your browser

### Browser Compatibility

**Speech Recognition Support:**
- Chrome/Chromium browsers (recommended)
- Edge
- Safari (limited support)
- Firefox (requires flag enabled)

**Note**: For the best experience, use Chrome or other Chromium-based browsers.

## Usage

### Creating a Reminder

1. **Enter Title**: Add a descriptive title for your reminder
2. **Record Voice Note** (Optional): 
   - Click "Start Recording" 
   - Speak your reminder message
   - Click "Stop Recording" when finished
3. **Set Time**: Choose when you want to be reminded
4. **Create**: Click "Create Reminder" to save

### Managing Reminders

- **View All**: See all your reminders in the main dashboard
- **Status**: Active reminders show as "Active", completed ones as "Completed"
- **Delete**: Click the trash icon to remove a reminder

### Alarm Experience

When an alarm triggers:
- **Visual Alert**: Flashing modal with reminder details
- **Audio Alert**: Alarm sound plays
- **Voice Playback**: Your recorded voice note is spoken aloud
- **Dismiss**: Click "Dismiss Alarm" to stop

## API Endpoints

### GET /api/reminders
Retrieve all reminders

### POST /api/reminders
Create a new reminder
\`\`\`json
{
  "title": "Meeting with client",
  "voiceNote": "Don't forget the presentation slides",
  "scheduledTime": "2024-01-15T14:30:00"
}
\`\`\`

### DELETE /api/reminders/[id]
Delete a specific reminder

### PUT /api/reminders/[id]
Update a reminder (used to mark as completed)

## Customization

### Styling
- Modify \`app/globals.css\` for custom animations and themes
- Update Tailwind classes in components for different color schemes
- Adjust animation durations and effects

### Storage
Replace the in-memory storage with:
- **SQLite**: For local file-based storage
- **PostgreSQL/MySQL**: For production databases
- **Supabase/Firebase**: For cloud-based solutions

### Audio
- Replace the placeholder alarm sound with custom audio files
- Add different alarm tones for different reminder types

## Deployment

### Vercel (Recommended)
1. Push code to GitHub
2. Connect repository to Vercel
3. Deploy automatically

### Other Platforms
- **Netlify**: Works with static export
- **Railway**: Full-stack deployment
- **Docker**: Use provided Dockerfile for containerization

## Browser Permissions

The app requires:
- **Microphone Access**: For voice recording
- **Audio Playback**: For alarm sounds
- **Notifications** (Optional): For browser notifications

## Troubleshooting

### Speech Recognition Issues
- Ensure microphone permissions are granted
- Try using Chrome/Chromium browsers
- Check if microphone is working in other applications

### Alarm Not Triggering
- Keep the browser tab active
- Check if audio is not muted
- Verify the scheduled time is in the future

### Performance
- Clear browser cache if experiencing issues
- Restart the development server
- Check browser console for error messages

## Future Enhancements

- **User Authentication**: Multi-user support
- **Cloud Sync**: Cross-device synchronization
- **Push Notifications**: Background notifications
- **Recurring Reminders**: Daily/weekly/monthly repeats
- **Categories**: Organize reminders by type
- **Export/Import**: Backup and restore functionality

## License

This project is open source and available under the MIT License.
