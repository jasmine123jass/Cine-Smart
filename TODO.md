# CineSmart Completion Plan

## Task Summary
Complete CineSmart with:
1. All Bollywood + Tollywood movies from archive datasets
2. Movie posters (from Wikipedia URLs in CSV + Google image fallback)
3. Netflix-like appearance

## Implementation Steps

### Step 1: Create Comprehensive Movie Service with Dataset Loading
- [ ] Update MovieService.java to load ALL movies from CSV files (Bollywood 1950-2019)
- [ ] Include poster URLs from Wikipedia in the CSV data
- [ ] Add Google image search URL as fallback for missing posters

### Step 2: Update Frontend Poster Handling
- [ ] Update script.js to use Wikipedia poster URLs when available
- [ ] Add fallback to Google image search for missing posters
- [ ] Improve Netflix-style card display

### Step 3: Enhance UI/UX
- [ ] Add more movie categories (Bollywood, Tollywood, etc.)
- [ ] Ensure proper poster display
- [ ] Add hero section with movie details

## Files to Modify:
1. backend/src/main/java/com/cinesmart/backend/service/MovieService.java
2. Frontend/script.js
3. Frontend/style.css (if needed)

## Dataset Sources:
- backend/src/main/resources/archive/1950-1989/
- backend/src/main/resources/archive/1990-2009/
- backend/src/main/resources/archive/2010-2019/
