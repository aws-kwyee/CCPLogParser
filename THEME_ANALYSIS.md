# CCP Log Parser - Theme Analysis

## Current Styling Structure

### Main Components and Their Styling:
1. **App.jsx** - Main container with Material-UI withStyles
   - Root background: `#f5f5f5` (light gray)
   - AppBar background: `#26303b` (dark blue-gray)
   - Tab background: `#2e3a48` (darker blue-gray)

2. **LogView.jsx** - Log display component
   - Header background: `#f7f7f7` (light gray)
   - Content background: `transparent`
   - Text color: `#222222` (dark gray)

3. **LogLineView.jsx** - Individual log lines
   - Hover background: `rgba(0,0,0,0.1)`
   - Selected background: `rgba(255,255,0,0.3)` (yellow highlight)
   - More info background: `#f5f5f588` (light gray with transparency)

4. **EmptyView.jsx** - Drag & drop area
   - Icon color: `rgba(0,0,0,0.25)` (light gray)
   - Text color: `rgba(0,0,0,0.5)` (medium gray)

5. **SnapshotListView.jsx** - Sidebar snapshots
   - Header background: `#f7f7f7` (light gray)
   - List background: `theme.palette.background.paper` (Material-UI default)
   - Selected background: `rgba(255,255,0,0.3)` (yellow highlight)

## Theme Implementation Plan

### 1. Create Theme Context
- Light theme (current colors)
- Dark theme (new dark colors)
- Theme toggle functionality

### 2. Color Scheme for Dark Mode
- **Background**: `#1a1a1a` (very dark gray)
- **Surface**: `#2d2d2d` (dark gray)
- **Primary**: `#3f51b5` (blue - keep existing primary)
- **Text Primary**: `#ffffff` (white)
- **Text Secondary**: `#b0b0b0` (light gray)
- **Border**: `#404040` (medium dark gray)

### 3. Components to Update
- App.jsx (root, appbar, tabs)
- LogView.jsx (header, content)
- LogLineView.jsx (lines, hover states)
- EmptyView.jsx (icon, text colors)
- SnapshotListView.jsx (header, list items)
- All other view components

### 4. Implementation Strategy
- Create ThemeContext with light/dark themes
- Add theme dropdown to AppBar
- Update all withStyles functions to use theme variables
- Ensure proper contrast ratios for accessibility