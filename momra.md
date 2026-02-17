# Dashboard Project Agent Guide

## Project Overview
Saudi Arabia One Health Platform - Dengue Fever Surveillance Dashboards

## File Structure & Purpose

### Primary Files
- **dashboard-v2.html** - ORIGIN/MASTER dashboard (Ministry of Health)
- **dashboard-momra.html** - DERIVATIVE dashboard (Ministry of Municipal & Housing)

### Relationship
```
dashboard-v2.html (ORIGIN)
    ↓ customized for specific ministry
dashboard-momra.html (REPLICA with modifications)
```

## Dashboard Specifications

### dashboard-v2.html (Full Health Dashboard)
- **Target Ministry**: وزارة الصحة (Ministry of Health)
- **Title**: لوحة معلومات الضنك - وقاية
- **Scope**: Complete epidemiological surveillance
- **Features**: ALL components included
  - Full statistics panel
  - Clinical outcomes tracking
  - Laboratory status monitoring
  - Field investigation data
  - Hospital reporting
  - Risk factor analysis
  - Viral hemorrhagic fever TreeMap
  - Complete demographic breakdowns

### dashboard-momra.html (Municipal Focus Dashboard)
- **Target Ministry**: وزارة البلديات والإسكان (Ministry of Municipal & Housing)
- **Title**: لوحة معلومات الضنك - وزارة البلديات والإسكان
- **Scope**: Municipal/housing-focused surveillance
- **Features**: SIMPLIFIED subset
  - Basic statistics
  - Geographic distribution (map)
  - Demographics (age, gender)
  - Municipal-relevant metrics only
  - NO clinical outcomes
  - NO detailed lab status
  - NO field investigations

## Technical Architecture

### Shared Components
- Map visualization with GeoJSON
- Basic chart functions (pie, bar, line)
- Filter system
- Data generation logic
- UI styling and animations

### Dashboard-Specific Components
| Component | dashboard-v2 | dashboard-momra |
|-----------|--------------|-----------------|
| Clinical Outcomes | ✅ | ❌ |
| Lab Status | ✅ | ❌ |
| TreeMap | ✅ | ❌ |
| Field Investigations | ✅ | ❌ |
| Risk Factors | ✅ | ❌ |
| Hospital Reporting | ✅ | ❌ |

## Data Strategy
- **Static mock data** for demonstration
- **Filter-based multiplication** for realistic variations
- **Ministry-specific data subsets**
- **Geographic focus**: Saudi Arabia cities and regions

## Maintenance Guidelines

### When to Modify dashboard-v2.html
- Core functionality changes
- Map improvements
- Filter system updates
- UI/UX enhancements
- Bug fixes in shared components

### When to Modify dashboard-momra.html
- Municipal-specific requirements
- Simplified workflow changes
- MOMRA branding updates
- Municipal data focus adjustments

### Code Organization Rules
1. **Keep intentional separation** - don't force convergence
2. **Extract shared utilities** only when beneficial
3. **Document differences** clearly
4. **Optimize each for its specific use case**

## Current Status
- Both dashboards are functional
- Arabic RTL layout implemented
- Glass morphism UI design
- Chart.js integration complete
- Mock data generation working

## Improvement Priorities
1. **Code cleanup** in MOMRA version (remove unused functions)
2. **Shared utilities extraction** for common functions
3. **Performance optimization** for each dashboard's scope
4. **Documentation enhancement** in code comments
5. **Accessibility improvements**
6. **Mobile responsiveness** verification

## Development Rules
- **dashboard-v2.html** = Full-featured master template
- **dashboard-momra.html** = Intentionally simplified derivative
- **No forced unification** - respect different requirements
- **Maintain clear separation** of concerns
- **Document all changes** affecting both files

## Key Stakeholders
- **Ministry of Health** (وزارة الصحة) - Full surveillance needs
- **Ministry of Municipal & Housing** (وزارة البلديات والإسكان) - Municipal focus needs

---
*Last Updated: November 2, 2025*
*Agent Purpose: Guide development decisions and maintain project clarity*