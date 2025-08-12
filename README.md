# EV/EBITDA Calculator

A professional, lightweight web application for calculating and analyzing Enterprise Value to EBITDA ratios for investment decisions. Built with vanilla HTML, CSS, and JavaScript with no sign-in required.

## 🚀 Features

### Core Functionality
- **EV/EBITDA Calculation**: Calculate the ratio from Enterprise Value and EBITDA inputs
- **Investment Scoring**: Get a 0-100 score based on industry-standard valuation bands
- **Investment Recommendations**: Receive Buy/Hold/Sell recommendations with explanations
- **In-Depth Analysis**: Expandable panels with due diligence checklists and limitations

### Calculation Methods
- **Enterprise Value (EV) Calculator**: 
  - Formula: EV = Market Cap + Total Debt - Cash & Cash Equivalents
  - Auto-fills main calculation form
- **EBITDA Calculator**:
  - Formula: EBITDA = Net Income + Interest + Taxes + Depreciation + Amortization
  - Auto-fills main calculation form

### Batch Processing
- **CSV Upload**: Drag & drop or click to upload CSV files
- **Multiple Companies**: Process 10+ companies simultaneously
- **Results Table**: Sortable results by company name, ratio, or score
- **Export Functionality**: Download results as CSV

### User Experience
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Modern UI**: Clean, professional interface with gradient backgrounds
- **Real-time Validation**: Error handling for invalid inputs
- **Auto-population**: Calculated values automatically fill main form

## 📊 Investment Logic

### EV/EBITDA Interpretation Bands
- **< 8**: Undervalued (Strong Buy) - Score: 90
- **6-8**: Undervalued (Buy) - Score: 78
- **8-12**: Fairly Valued (Hold) - Score: 55
- **12-18**: Overvalued (Sell) - Score: 25
- **> 18**: Highly Overvalued (Strong Sell) - Score: 10

### Special Cases
- **EBITDA = 0**: N/A - Suggests alternative valuation methods
- **EBITDA < 0**: N/A - Not meaningful for EV/EBITDA analysis

## 🛠️ Technical Details

### Technologies Used
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **CSV Processing**: PapaParse library for robust file handling
- **Styling**: Custom CSS with responsive grid layouts
- **No Backend**: 100% client-side processing

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### File Structure
```
Fianance/
├── index.html              # Main application file
├── sample_companies.csv    # Sample data for testing
└── README.md              # This documentation
```

## 📁 CSV Format Requirements

### Required Columns
- `company_name`: Company name or identifier
- `ev`: Enterprise Value (numeric)
- `ebitda`: EBITDA value (numeric, must be > 0)

### Optional Columns
- `currency`: Currency code (defaults to USD)
- `unit`: Unit of measurement (defaults to millions)

### Sample CSV Structure
```csv
company_name,ev,ebitda,currency,unit
Apple Inc,2500000,350000,USD,billions
Microsoft Corp,2200000,280000,USD,billions
```

## 🚀 Getting Started

### 1. Download Files
- Download `index.html` and `sample_companies.csv`
- Place them in the same directory

### 2. Open Application
- Double-click `index.html` or open in any modern web browser
- No installation or server setup required

### 3. Start Calculating
- Use individual EV/EBITDA calculators for single companies
- Upload CSV files for batch analysis
- Export results for further analysis

## 💡 Usage Examples

### Single Company Analysis
1. **Calculate EV**: Enter market cap, debt, and cash → Get EV
2. **Calculate EBITDA**: Enter income components → Get EBITDA
3. **Main Calculation**: EV/EBITDA ratio, score, and recommendation
4. **View Details**: Expand in-depth analysis panel

### Batch Analysis
1. **Prepare CSV**: Create file with company data
2. **Upload**: Drag & drop or click to upload
3. **Review Results**: Sort by different criteria
4. **Export**: Download results for portfolio analysis

## 🔧 Customization

### Adding New Currencies
Edit the currency dropdown in `index.html`:
```html
<option value="NEW">NEW (Symbol)</option>
```

### Modifying Score Bands
Update the `calculateScore()` function in the JavaScript:
```javascript
function calculateScore(ratio) {
    if (ratio <= 6) return 90;
    if (ratio <= 8) return 78;
    // Add your custom bands here
}
```

### Styling Changes
Modify the CSS variables and classes in the `<style>` section of `index.html`.

## 📈 Business Applications

### Investment Analysis
- **Screening**: Quickly identify undervalued companies
- **Comparison**: Compare multiple companies in a sector
- **Due Diligence**: Use checklist for thorough analysis

### Portfolio Management
- **Risk Assessment**: Identify overvalued positions
- **Opportunity Detection**: Find potential new investments
- **Performance Tracking**: Monitor valuation changes over time

### Financial Planning
- **Valuation Models**: Input for DCF and other models
- **M&A Analysis**: Evaluate acquisition targets
- **Credit Analysis**: Assess company financial health

## 🚨 Limitations & Disclaimers

### Technical Limitations
- **Client-side Only**: No data persistence between sessions
- **File Size**: Large CSV files may impact performance
- **Browser Memory**: Very large datasets may cause issues

### Financial Limitations
- **Single Metric**: EV/EBITDA is one of many valuation tools
- **Industry Variation**: Benchmarks vary by sector
- **Market Conditions**: Economic factors affect interpretation
- **Growth Rates**: Doesn't account for future growth prospects

### Professional Use
- **Not Financial Advice**: Use for educational and analytical purposes only
- **Due Diligence**: Always conduct thorough research before investing
- **Professional Consultation**: Consult financial advisors for investment decisions

## 🔮 Future Enhancements

### Planned Features
- **Sector Benchmarks**: Industry-specific comparison data
- **Historical Trends**: Track ratio changes over time
- **Portfolio Saving**: Save and compare multiple analyses
- **API Integration**: Connect to financial data providers

### Technical Improvements
- **React Version**: Modern component-based architecture
- **Database Backend**: Persistent data storage
- **User Accounts**: Personalized analysis history
- **Mobile App**: Native mobile application

## 🤝 Contributing

### Development Setup
1. Clone or download the project files
2. Open `index.html` in a code editor
3. Make changes and test in browser
4. Submit improvements or bug reports

### Code Standards
- **HTML**: Semantic markup with accessibility
- **CSS**: Responsive design with modern features
- **JavaScript**: ES6+ syntax with clear function names
- **Comments**: Inline documentation for complex logic

## 📞 Support & Contact

### Issues & Questions
- **Technical Issues**: Check browser console for errors
- **Feature Requests**: Document specific use cases
- **Bug Reports**: Include steps to reproduce

### Documentation
- **User Guide**: This README file
- **Code Comments**: Inline documentation in HTML/JS
- **Sample Data**: `sample_companies.csv` for testing

## 📄 License

This project is provided as-is for educational and professional use. No warranty is expressed or implied. Use at your own risk for financial analysis and investment decisions.

---

**Built with ❤️ for financial professionals and investors**

*Last updated: December 2024*
