# Xcel Energy TOU Calculator

A web application that helps Colorado Xcel Energy customers determine whether Time of Use (TOU) pricing will save them money compared to traditional flat rate pricing.

## 🌐 Live Demo

[https://xcel-tou-calculator.vercel.app/](https://xcel-tou-calculator.vercel.app/)

## 📋 Overview

Xcel Energy is transitioning Colorado customers to choose between two pricing plans:
- **Time of Use (TOU)**: Different rates for on-peak (5pm-9pm weekdays) and off-peak hours
- **Flat Rate**: Single rate applied to all usage

This calculator analyzes your historical hourly usage data to show which plan would save you money.

## ✨ Features

- **📊 Upload Your Data**: Import your Xcel Energy hourly usage CSV file
- **💰 Cost Comparison**: See side-by-side annual costs for TOU vs Flat Rate pricing
- **📈 Visual Analytics**: 
  - Monthly usage patterns (on-peak vs off-peak)
  - Cost comparisons by month
  - Savings/loss breakdown
  - On-peak usage percentage trends
- **✅ Data Validation**: Automatic checks for data completeness and quality
- **🧪 Demo Mode**: Try the calculator with sample data
- **🎯 What-If Scenarios**: Interactive slider to see how shifting usage patterns affects savings
- **📄 Save as PDF**: Export your results via browser print dialog
- **📱 Responsive Design**: Works on desktop, tablet, and mobile devices

## 🚀 Getting Started

### For Users

1. Visit [xcel-tou-calculator.vercel.app](https://xcel-tou-calculator.vercel.app/)
2. Download your hourly usage data from Xcel Energy:
   - Log in to your [Xcel account](https://myenergy.xcelenergy.com/myenergy/usage-history)
   - Select "by Hour" from the dropdown
   - Click "By Interval"
   - Set interval range to one year
   - Click "Download Data"
3. Upload your CSV file to the calculator
4. Review your personalized cost comparison

### For Developers

#### Prerequisites

- Node.js 16+ and npm

#### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/xcel-tou-calculator.git

# Navigate to project directory
cd xcel-tou-calculator

# Install dependencies
npm install

# Start development server
npm run dev
```

#### Build for Production

```bash
npm run build
```

The built files will be in the `dist/` directory.

## 📊 How It Works

### Pricing Structure

**Summer Rates (June - September):**
- TOU On-Peak: $0.21277/kWh
- TOU Off-Peak: $0.07884/kWh
- Flat Rate: $0.10380/kWh

**Winter Rates (October - May):**
- TOU On-Peak: $0.18331/kWh
- TOU Off-Peak: $0.06792/kWh
- Flat Rate: $0.08570/kWh

### Peak Hours

- **On-Peak**: 5pm - 9pm, Monday - Friday
- **Off-Peak**: All other hours and weekends

### Calculation Method

1. Parses your hourly usage CSV data
2. Categorizes each hour as on-peak or off-peak
3. Applies seasonal rates (summer vs winter)
4. Calculates total annual costs for both TOU and Flat Rate plans
5. Shows monthly breakdowns and visualizations

## 🎮 What-If Scenarios

The interactive slider lets you explore how shifting your usage patterns affects your savings:

- Adjust from **-20% to +20%** on-peak usage
- See real-time impact on annual savings
- Understand how behavioral changes (running appliances at night, EV charging off-peak, etc.) affect costs

## 🛠️ Technology Stack

- **React**: UI framework
- **Vite**: Build tool and dev server
- **Tailwind CSS**: Styling
- **Recharts**: Data visualization
- **PapaParse**: CSV parsing
- **Lucide React**: Icons

## 📁 Project Structure

```
xcel-tou-calculator/
├── dist/                      # Production build files
│   ├── index.html
│   └── assets/
│       └── index-[hash].js
├── xcel-tou-calculator.jsx    # Main React component
├── index.jsx                  # React entry point
├── index.html                 # HTML template
├── vite.config.js             # Vite configuration
├── package.json               # Dependencies and scripts
└── README.md                  # This file
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License.

## ⚠️ Disclaimer

This calculator is for informational purposes only. While we strive for accuracy, please verify all calculations with Xcel Energy. Rates and pricing structures are subject to change. Always consult your official Xcel Energy bills and rate schedules for the most current information.

## 🙏 Acknowledgments

- Rate information from [Xcel Energy Colorado](https://co.my.xcelenergy.com/s/billing-payment/residential-rates/time-of-use-pricing)
- Built to help Colorado residents make informed energy pricing decisions

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

**Made with ⚡ for Colorado Xcel Energy customers**
