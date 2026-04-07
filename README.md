# ⚽ Football Daily - Sports Web App

A modern, single-page web application for football enthusiasts to view daily matches, team lineups, match statistics, and AI-powered match predictions.

## 🌟 Features

### 📋 Today's Matches
- **Real-time Match Display**: View all football matches happening today across major leagues
- **League Filter**: Filter matches by Premier League, La Liga, Serie A, Bundesliga, or Ligue 1
- **Date Selector**: Browse matches for different dates
- **Live Status**: See match status (Not Started, In Progress, Finished)
- **Quick Info**: Team names, scores, time, and stadium information

### 👥 Team Lineups
- **Starting 11**: View the complete starting lineup with player names, numbers, and positions
- **Substitutes**: See reserve players ready to enter the game
- **Coach Info**: Team coach/manager information
- **Formation**: Team's tactical formation
- **Player Search**: Quick search through all players in the match

### 📊 Match Statistics
- **Detailed Comparison**: Home vs Away statistics including:
  - Shots on Target & Total Shots
  - Possession Percentage
  - Passes Accuracy
  - Corner Kicks
  - Fouls Committed
  - Yellow/Red Cards
  - Offsides
  - Goals
- **Half-Time Scores**: Track scores at different stages
- **Visual Comparisons**: Easy-to-read stat bars

### 🎯 AI-Powered Predictions
- **Win Probability**: Calculated probability for Home Win, Draw, or Away Win
- **Goal Markets**:
  - Over/Under 1.5 Goals
  - Over/Under 2.5 Goals
  - Over/Under 3.5 Goals
- **Both Teams to Score (BTS)**: Probability both teams will score
- **Asian Handicap**: Handicap betting predictions
- **Visual Indicators**: Progress bars showing prediction confidence

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for API calls)

### Installation

1. **Download the file**
   - Save `index.html` to your desired location

2. **Open in Browser**
   - Double-click `index.html` or
   - Open with your preferred web browser
   - Or serve via a local server: `python -m http.server 8000`

3. **Access the App**
   - Navigate to `http://localhost:8000` (if using server)
   - Or just open the file directly in your browser

## 📱 Usage

### Viewing Today's Matches
1. Click the "Today's Matches" tab
2. The app automatically loads matches for today
3. Use the **League Filter** dropdown to filter by specific league
4. Use the **Date Picker** to select a different date
5. Click on any match card to see detailed information

### Viewing Lineups
1. Click on a match card to open the match details modal
2. Navigate to the "Lineups" section
3. View starting players and substitutes for both teams
4. See formation and coach information
5. Use player search to find specific players

### Viewing Statistics
1. Open a match details modal
2. Go to the "Statistics" tab
3. Compare home vs away stats visually
4. Scroll through different statistical categories

### Making Predictions
1. Click the "Predictions" tab
2. Select a match from the list
3. View the AI-calculated probabilities for:
   - Match outcome (Home/Draw/Away)
   - Goal markets (Over/Under various thresholds)
   - Both teams to score
   - Asian handicap options
4. Use predictions to inform your analysis

## 🔌 API Integration

### Data Source
- **API**: apifootball.com (Free Tier)
- **Authentication**: No API key required for free tier
- **Rate Limits**: Generous limits suitable for daily browsing

### API Endpoints Used
- `/v1/events/` - Match events and statistics
- `/v1/fixtures/` - Match fixtures and schedules
- Lineup data - Embedded in match events

### Data Points
- Match scores and status
- Player lineups (starting XI and substitutes)
- Team statistics
- Match details (venue, referee, etc.)

## 🛠️ Technical Stack

### Frontend
- **HTML5**: Semantic markup
- **CSS3**: Modern styling with gradients and animations
- **JavaScript (Vanilla)**: No framework dependencies
  - Fetch API for HTTP requests
  - DOM manipulation
  - Event listeners
  - LocalStorage for caching

### Libraries/CDN
- **Tailwind CSS via Browser** (optional enhancement)
- Pure CSS for styling
- No external JavaScript libraries

### Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📊 Prediction Algorithm

The AI predictions use a statistical model based on:
- **Historical Data**: Past match outcomes between teams
- **Team Form**: Recent performance metrics
- **Head-to-Head**: Direct matchup history
- **Home/Away Factor**: Advantage of playing at home
- **League Position**: Current standings and strength

The predictions are probabilistic and should not be considered as guaranteed outcomes.

## 🎨 UI/UX Features

- **Responsive Design**: Works on desktop, tablet, and mobile
- **Dark Theme**: Easy on the eyes with gradient backgrounds
- **Smooth Animations**: Transitions and hover effects
- **Intuitive Navigation**: Clear tabs and sections
- **Modal Windows**: Detailed view without page navigation
- **Color Coding**: Easy visual identification of match status

## ⚙️ Configuration

### Customization Options

To modify the default leagues:
```javascript
// Edit the leagueIds array in the JavaScript section
const leagueIds = [39, 140, 135, 78, 61]; // Premier League, La Liga, Serie A, Bundesliga, Ligue 1
```

To change the default date:
```javascript
// Modify the initial date loading in the load event
const today = new Date();
```

## 🐛 Troubleshooting

### Issue: No matches displaying
- **Solution**: Check internet connection and API status
- The app requires live data from the API
- Wait a few seconds for data to load
- Try selecting a different date

### Issue: Lineups not showing
- **Solution**: Not all matches have available lineup data
- Wait for match day (lineups are finalized closer to match time)
- Try a different match

### Issue: Statistics showing zeros
- **Solution**: Statistics are populated during and after the match
- Before kickoff, stats will be empty
- Wait for the match to start

### Issue: CORS errors
- **Solution**: The API supports cross-origin requests
- Try clearing browser cache
- Use a different browser
- Check if browser privacy settings allow API requests

## 📈 Future Enhancements

- Live score updates with WebSocket
- Historical match data and archives
- Player performance analytics
- Season-long statistics tracking
- Betting odds integration
- User preferences and saved matches
- Mobile app version
- Push notifications for match events
- Multi-language support
- Dark/Light theme toggle

## 📜 License

This project uses data from apifootball.com and is provided for educational and personal use.

## 🤝 Contributing

To suggest improvements or report issues:
1. Test the feature/bug thoroughly
2. Document what you found
3. Suggest clear improvements

## 📞 Support

For issues with the API, visit: https://apifootball.com/

For browser compatibility issues, ensure you're using a modern browser version.

## ⚠️ Disclaimer

The predictions provided by this application are for informational purposes only and should not be used for gambling or financial decisions. The accuracy of predictions is not guaranteed and depends on multiple factors. Always exercise caution and responsible decision-making.

## 🎓 Learning Resources

- **JavaScript Fetch API**: https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API
- **HTML5 Semantics**: https://developer.mozilla.org/en-US/docs/Glossary/Semantics
- **CSS3 Animations**: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations
- **Football Statistics**: https://en.wikipedia.org/wiki/Category:Association_football_statistics

## 📝 Version History

### v1.0.0 (Current)
- Initial release
- Match display and filtering
- Lineup viewer
- Statistics comparison
- AI-powered predictions
- Multi-league support

---

**Made with ⚽ for football lovers**

*Last Updated: 2024*
