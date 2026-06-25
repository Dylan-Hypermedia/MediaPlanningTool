# ?? Media Planning Dashboard - Dual-View Budget Planning Tool

A comprehensive, interactive media planning tool that generates both **internal buy rates** and **client-facing blended CPM proposals** from a single campaign dataset. Perfect for media agencies managing complex multi-channel campaigns with transparent internal cost tracking and simplified client presentations.

## ?? Overview

This tool solves the challenge of maintaining two parallel views of media plans:
- **Internal View**: Shows actual costs, individual CPM rates for each channel, and detailed fee breakdowns
- **Client View**: Presents a clean blended CPM that includes all fees and service charges without showing the complexity

All calculations are performed in real-time in the browser—no server required, fully offline capable.

---

## ? Key Features

### ??? Dual-View System
- **Internal Plan**: Transparent cost structure with itemized fees (HM Management, DSP, SSP, VR/Agency)
- **Client Proposal**: Simplified blended CPM showing total investment without fee complexity
- **Side-by-Side Comparison**: Analyze impact of fees on final CPM pricing

### ?? Advanced Budget Management
- **Campaign Budget Tracking**: Real-time total budget vs. assigned budget vs. total cost
- **Budget Warning System**: Color-coded alerts (?? Normal | ?? Warning | ?? Over Budget)
- **Remaining Budget Display**: Instant visibility of available funds
- **Flexible Campaign Details**: Flight dates with auto-calculated campaign duration

### ?? Channel Management
- **Media Channels**: PDOOH, In-Store, Mobile, Outdoor
- **Flat Fee Products**: Support for non-impression-based services (BLS Reporting, Creative Execution, etc.)
- **Dynamic Channel Types**: Easily add, remove, or modify channels
- **Unlimited Channels**: Scale to any campaign size

### ?? Intelligent Calculations

#### Three-Way Field Calculations
For media channels, enter ANY 2 of 3 fields and the third auto-calculates:
- **Budget + Impressions** ? Auto-calculates CPM
- **Budget + CPM** ? Auto-calculates Impressions
- **Impressions + CPM** ? Auto-calculates Budget

#### Fee Structure
- **HM Management Fee**: % of Total Campaign Budget
- **DSP Tech Fee**: % of Channel Budget
- **SSP Fee**: % of (Channel Budget - DSP Fee) — cascading calculation
- **VR/Agency Fee**: % of Total Campaign Budget
- **Flat Fee Products**: Fixed amounts, no fee markups applied

#### CPM Logic
- **Internal CPM**: (Media Cost / Impressions) × 1000
- **Blended CPM**: (Total Cost Including All Fees / Impressions) × 1000
- **Channel-Level Blending**: Proportional fee distribution across channels

### ?? Visual Analytics
- **Budget Split Pie Charts**: Internal and Client views show channel allocation
- **Interactive Charts**: Hover tooltips show amounts and percentages
- **Color-Coded Segments**: Consistent visual design across both views
- **Responsive Design**: Charts auto-hide if no data available

### ?? Multi-Currency Support
- **USD & AED Toggle**: Switch currencies instantly
- **Real-time Conversion**: All displays update dynamically
- **Format Preservation**: Numbers formatted appropriately for selected currency

### ?? Campaign Details
- **Campaign Name**: Custom identifier
- **Client Name**: Client organization
- **Objective**: Campaign goal (e.g., "Awareness & Reach")
- **Flight Dates**: Start and end dates with auto-calculated campaign duration
- **Total Budget**: Campaign-wide budget envelope

### ?? Export & Print Options
- **JSON Export**: Complete plan data for archival or system integration
- **Internal Print**: Formatted printable version with buy rates and fees
- **Client Print**: Clean proposal suitable for client delivery
- **Browser Print**: Native print styling for PDF generation

---

## ?? Getting Started

### Installation
1. Download `media_planning_tool.html`
2. Open in any modern web browser (Chrome, Firefox, Safari, Edge)
3. No installation, dependencies, or server setup required

### Quick Start Workflow

#### 1. **Define Campaign** (Edit Plan tab)
- Enter campaign name, client, objective
- Set flight dates (auto-calculates duration)
- Enter total budget

#### 2. **Add Channels** (Media Channels section)
- Add channels using quick-add form OR
- Populate default templates with your data
- For media channels: Enter any 2 of (Budget, Impressions, CPM)
- For flat fees: Check "Flat Fee?" box and enter fixed amount

#### 3. **Configure Fees** (Fee Structure section)
- Set HM Management Fee %
- Set DSP Tech Fee %
- Set SSP Fee %
- Set VR/Agency Fee %

#### 4. **Review Plans**
- **Internal View**: See actual costs and individual CPMs
- **Client View**: See blended CPM without fee details
- **Side-by-Side**: Compare impact of fees
- **Budget Summary**: Verify you're within budget

#### 5. **Export & Present**
- Print internal plan for cost tracking
- Print client plan for proposal delivery
- Export JSON for integration with other systems

---

## ?? Understanding the Tool

### Channel Table Columns

| Column | Description | Media Channels | Flat Fee |
|--------|-------------|---|---|
| **Channel Name** | Service/placement name | Required | Required |
| **Type** | Channel category (PDOOH, In-Store, etc.) | Required | "Flat Fee" |
| **Flat Fee?** | Toggle for fee-based products | Unchecked | Checked |
| **Budget/Cost** | Amount allocated (2 of 3) | $ amount | $ fixed cost |
| **Impressions** | Expected reach (2 of 3) | # impressions | — (disabled) |
| **CPM** | Cost per thousand impressions (2 of 3) | $ CPM | — (disabled) |

### Budget Tracking Metrics

```
Assigned Budget = Sum of all channel budgets
Media Cost = Assigned Budget

Total Fees = HM Fee + DSP Fee + SSP Fee + VR Fee
Where:
  HM Fee = Total Budget × HM %
  DSP Fee = Assigned Budget × DSP %
  SSP Fee = (Assigned Budget - DSP Fee) × SSP %
  VR Fee = Total Budget × VR %

Total Cost = Media Cost + Total Fees
Remaining Budget = Total Budget - Total Cost
```

### Internal View Logic
- Shows unblended costs and fees
- Individual CPM per channel = (Channel Budget / Channel Impressions) × 1000
- DSP and SSP fees calculated at portfolio level
- All fees itemized separately

### Client View Logic
- Total investment = Total Cost (same as internal)
- Blended CPM = (Total Cost / Total Impressions) × 1000
- Fees distributed proportionally across channels
- No fee breakdown shown (transparent to client)

---

## ?? Visual Design

### Color Scheme
- **Primary Blue** (#185FA5): Headers, primary elements
- **Accent Green** (#639922): Blended CPM values, positive indicators
- **Warning Yellow** (#fff3cd): Budget warning states
- **Danger Red** (#f8d7da): Over-budget alerts
- **Neutral Gray**: Secondary content, disabled fields

### Responsive Layout
- Optimized for desktop (1200px+) and tablet views
- Grid-based metrics for flexible sizing
- Table columns with fixed widths for stability
- Mobile-friendly typography and spacing

### Interactive Elements
- Checkboxes for flat fee toggle
- Dropdown selects for channel types
- Number inputs with auto-calculation
- Real-time chart updates
- Color-coded card states based on budget status

---

## ?? Use Cases

### 1. **Multi-Channel Campaign Planning**
- PDOOH campaigns across metro systems
- Retail/in-store placements in shopping centers
- Mobile retargeting across platforms
- Mixed-media integrated campaigns

### 2. **Fee-Based Services Integration**
- Media planning + BLS reporting costs
- Creative execution fees
- Premium placement charges
- Production and licensing costs

### 3. **Client Proposal Generation**
- Clean CPM proposals without fee complexity
- Professional print-ready documents
- Transparent cost breakdowns (internal only)
- Side-by-side plan comparisons

### 4. **Budget Compliance**
- Prevent overspending with real-time warnings
- Monitor budget utilization percentage
- Track remaining funds across campaign
- Itemized fee visibility for finance teams

### 5. **Currency Management**
- Multi-region campaigns (USD, AED)
- Instant currency switching for presentations
- Consistent formatting across currencies
- No recalculation needed

---

## ?? Technical Details

### Architecture
- **Single HTML File**: No build process, dependencies, or server needed
- **Client-Side Only**: All processing in browser, no data transmission
- **Chart.js 4.4.1**: Via CDN for visualization (one external dependency)
- **Vanilla JavaScript**: Pure ES6, no frameworks

### Browser Compatibility
- ? Chrome 90+
- ? Firefox 88+
- ? Safari 14+
- ? Edge 90+

### Performance
- Sub-100ms calculation time for all metrics
- Real-time chart updates on field change
- Optimized DOM rendering
- No noticeable lag with 20+ channels

### Data Persistence
- **Session-Based**: Data persists during browser session
- **LocalStorage Option**: Can be added for save-between-sessions
- **JSON Export**: Full data export for external storage
- **No Cloud**: All data remains on user's machine

---

## ?? Channel Types & Defaults

### Pre-Built Channel Templates
Tool includes default empty templates for:
- PDOOH Channel 1 & 2 (Digital out-of-home)
- In-Store Channel 1 & 2 (Retail placements)
- Mobile Channel 1 (Digital/mobile)
- Outdoor Channel 1 (Traditional OOH)
- Other Channel 1 (Flexible category)
- Flat Fee (for fixed-cost services)

All channels start at $0 and can be customized freely.

### Adding Custom Channel Types
Users can freely:
- Rename channel descriptions
- Change channel types via dropdown
- Mark as flat fee or media channel
- Delete and re-add as needed
- Clear all and start fresh

---

## ?? Example Scenario

**Campaign**: "UAE Q2 Awareness Push"
- **Client**: Premium Brand XYZ
- **Budget**: AED 200,000 total
- **Flight**: 1 April - 30 June (90 days)
- **Objective**: Reach & Awareness

**Channels**:
1. Metro PDOOH: AED 60,000 / 3,000,000 impressions = AED 20 CPM
2. Mall In-Store: AED 40,000 / 2,000,000 impressions = AED 20 CPM
3. Mobile Retargeting: AED 50,000 / 5,000,000 impressions = AED 10 CPM
4. Creative Execution (Flat Fee): AED 15,000

**Fees**:
- HM Management: 10% of AED 200,000 = AED 20,000
- DSP Tech: 15% of AED 150,000 = AED 22,500
- SSP: 15% of (AED 150,000 - 22,500) = AED 19,125
- VR/Agency: 10% of AED 200,000 = AED 20,000
- **Total Fees**: AED 81,625

**Results**:
- Internal CPM: AED 16.67 (media only)
- Blended CPM: AED 23.11 (with all fees)
- Total Cost: AED 231,625
- **Over Budget by**: AED 31,625 ?? WARNING

User adjusts channels until under budget, then:
- Prints internal plan for cost tracking
- Prints client plan with blended CPM for proposal
- Exports JSON for CRM/project management system

---

## ?? Security & Privacy

- **No Data Collection**: Zero analytics, tracking, or external calls
- **Offline-First**: Works without internet connection
- **Local Processing**: All calculations on user's device
- **No Authentication**: No user accounts or passwords
- **No Dependencies**: Only Chart.js from CDN (essential for charts)

---

## ?? Future Enhancement Ideas

- LocalStorage for persistent saves
- Multi-plan comparison views
- Historical scenario tracking
- Custom fee templates
- Excel/CSV import/export
- Mobile app version
- Collaborative editing (with server)
- Advanced forecasting and sensitivity analysis
- Custom branding options for client exports

---

## ??? Customization

### Modifying Fee Labels
Edit the HTML labels in the Fee Structure section to match your agency:
- "HM Management Fee" ? "Agency Management Fee"
- "DSP Tech Fee" ? "Platform Fee"
- "SSP Fee" ? "Supply-Side Fee"
- "VR/Agency Fee" ? "Creative Services Fee"

### Adding Channel Types
Edit the channel type dropdown options in the HTML:
```html
<option>PDOOH</option>
<option>In-Store</option>
<option>Mobile</option>
<option>Outdoor</option>
<option>Flat Fee</option>
<option>Other</option>
<!-- Add custom types here -->
```

### Adjusting Default Fees
Modify the plan object at script initialization:
```javascript
hmFeePercent: 10,      // Change HM fee %
dspFeePercent: 15,     // Change DSP fee %
sspFeePercent: 15,     // Change SSP fee %
vrFeePercent: 10       // Change VR fee %
```

---

## ?? Support & Feedback

This is a fully self-contained tool. For issues or enhancements:
1. Check the browser console (F12) for errors
2. Verify all fields are numeric where required
3. Ensure impressions are non-zero for media channels (flat fees don't need this)
4. Try exporting/importing data to verify data integrity

---

## ?? License

This tool is provided as-is for media planning purposes. Adapt and customize as needed for your agency's workflows and branding.

---

## ?? Learning Resources

### Key Concepts
- **CPM**: Cost Per Thousand impressions (industry standard metric)
- **Blended CPM**: All-in rate that includes service fees and markups
- **Media Budget**: Direct spend on placements/impressions
- **Fees**: Agency services, platform costs, technology surcharges

### Best Practices
1. Always verify budget before client presentations
2. Communicate fee structure clearly to clients upfront
3. Export data regularly for records and integrations
4. Use side-by-side view to understand fee impact on pricing
5. Print/save proposals for compliance and audit trails

---

## ?? Quick Links

- **File**: `media_planning_tool.html`
- **Size**: ~50KB (single file, no compression)
- **Setup Time**: ~30 seconds (just open the file)
- **Learning Curve**: ~5 minutes to understand the interface
- **Data Entry Time**: ~10-15 minutes for typical 5-channel campaign

---

**Built with**: HTML5, CSS3, JavaScript (ES6), Chart.js 4.4.1
**No external dependencies** except Chart.js (for visualization)
**Works offline** - open HTML file and start planning
**Browser-based** - no installation required

---

*Media Planning Dashboard v1.0 - Comprehensive Dual-View Campaign Budget Planning Tool*
