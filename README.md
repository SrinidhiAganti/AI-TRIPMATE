# TripMate - AI Travel Planner

## Overview
Brief description of what the application does.

## Features
- Feature 1
- Feature 2

## Tech Stack
- Backend: Python, FastAPI
- Frontend: React, CSS

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="AI-powered travel planner for personalized itineraries">
    <meta name="keywords" content="travel, ai, planner, itinerary, vacation">
    <meta name="author" content="TripMate Team">
    
    <!-- Open Graph Meta Tags -->
    <meta property="og:title" content="TripMate - AI Travel Planner">
    <meta property="og:description" content="Create personalized travel itineraries with AI">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://tripmate.app">
    <meta property="og:image" content="https://tripmate.app/og-image.jpg">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="TripMate - AI Travel Planner">
    <meta name="twitter:description" content="Create personalized travel itineraries with AI">
    <meta name="twitter:image" content="https://tripmate.app/twitter-image.jpg">
    
    <title>TripMate Pro - AI Travel Planner | Personalized Itineraries</title>
    
    <!-- Preconnect to external domains -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="preconnect" href="https://api.openai.com">
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="/favicon.ico">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Critical CSS inlined here for performance -->
    <style>
        /* Critical CSS for above-the-fold content */
        :root {
            --primary-500: #3b82f6;
            --primary-600: #2563eb;
            --gray-800: #1f2937;
            --gray-900: #111827;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: var(--gray-800);
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }
        
        .hidden {
            display: none !important;
        }
    </style>
</head>
<body>
    <!-- Skip to main content for accessibility -->
    <a href="#main-content" class="skip-link">Skip to main content</a>
    
    <!-- Header with semantic navigation -->
    <header class="site-header" role="banner">
        <div class="container">
            <nav class="main-nav" role="navigation" aria-label="Main navigation">
                <a href="/" class="logo" aria-label="TripMate homepage">
                    <span class="logo-icon" role="img" aria-label="airplane">✈️</span>
                    <span>TripMate Pro</span>
                </a>
                
                <ul class="nav-list">
                    <li><a href="#planner" class="nav-link" aria-current="page">Plan Trip</a></li>
                    <li><a href="#features" class="nav-link">Features</a></li>
                    <li><a href="#pricing" class="nav-link">Pricing</a></li>
                    <li><a href="#contact" class="nav-link">Contact</a></li>
                    <li><span class="premium-badge">Pro</span></li>
                </ul>
                
                <!-- Mobile menu button -->
                <button class="mobile-menu-btn" aria-label="Toggle mobile menu" aria-expanded="false">
                    <span></span>
                    <span></span>
                    <span></span>
                </button>
            </nav>
        </div>
    </header>

    <!-- Main content area -->
    <main id="main-content" class="main-content">
        <!-- Hero Section -->
        <section class="hero-section" aria-labelledby="hero-title">
            <div class="container">
                <h1 id="hero-title" class="hero-title">
                    Create Amazing Travel Experiences with AI
                </h1>
                <p class="hero-subtitle">
                    Get personalized itineraries, budget estimates, and local insights 
                    powered by artificial intelligence. Plan smarter, travel better.
                </p>
                
                <!-- Feature highlights -->
                <div class="feature-highlights" role="list">
                    <div class="feature-card" role="listitem">
                        <span class="feature-icon" role="img" aria-label="AI brain">🧠</span>
                        <h3 class="feature-title">AI-Powered Planning</h3>
                        <p class="feature-description">
                            Smart recommendations based on your preferences and travel style
                        </p>
                    </div>
                    
                    <div class="feature-card" role="listitem">
                        <span class="feature-icon" role="img" aria-label="money">💰</span>
                        <h3 class="feature-title">Budget Optimization</h3>
                        <p class="feature-description">
                            Get accurate cost estimates and money-saving tips
                        </p>
                    </div>
                    
                    <div class="feature-card" role="listitem">
                        <span class="feature-icon" role="img" aria-label="clock">⚡</span>
                        <h3 class="feature-title">Instant Results</h3>
                        <p class="feature-description">
                            Generate complete itineraries in seconds, not hours
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Main Planning Form Section -->
        <section class="planner-section" id="planner" aria-labelledby="planner-heading">
            <div class="container">
                <h2 id="planner-heading" class="section-title">Plan Your Perfect Trip</h2>
                <p class="section-subtitle">Tell us about your dream destination and preferences</p>
                
                <div class="form-container">
                    <!-- Progress indicator -->
                    <div class="form-progress" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">
                        <div class="form-progress-bar" id="formProgressBar"></div>
                    </div>
                    
                    <form class="trip-form" id="tripForm" novalidate>
                        <!-- Step 1: Destination & Duration -->
                        <div class="form-section" data-step="1">
                            <div class="section-header">
                                <span class="section-number">1</span>
                                <h3 class="section-title-text">Where & When</h3>
                            </div>
                            
                            <div class="field-group">
                                <div class="field-row">
                                    <div class="field-wrapper">
                                        <label for="destination" class="field-label">
                                            <span>Destination</span>
                                            <span class="required-indicator" aria-label="required">*</span>
                                        </label>
                                        <div class="destination-input-wrapper">
                                            <input 
                                                type="text" 
                                                id="destination" 
                                                name="destination"
                                                class="field-input"
                                                placeholder="e.g., Paris, Tokyo, New York..."
                                                aria-describedby="destination-help destination-error"
                                                autocomplete="off"
                                                required
                                            >
                                            <div class="destination-suggestions" id="destinationSuggestions" role="listbox">
                                                <!-- Dynamic suggestions populated by JavaScript -->
                                            </div>
                                        </div>
                                        <div id="destination-help" class="field-help">
                                            <span>🔍</span>
                                            <span>Start typing for destination suggestions</span>
                                        </div>
                                        <div id="destination-error" class="field-error" role="alert"></div>
                                        <div id="destination-success" class="field-success">
                                            <span>✓</span>
                                            <span>Great choice!</span>
                                        </div>
                                    </div>
                                    
                                    <div class="field-wrapper">
                                        <label for="days" class="field-label">
                                            <span>Trip Duration</span>
                                            <span class="required-indicator" aria-label="required">*</span>
                                        </label>
                                        <input 
                                            type="number" 
                                            id="days" 
                                            name="days"
                                            class="field-input"
                                            min="1" 
                                            max="30" 
                                            value="7"
                                            aria-describedby="days-help days-error"
                                            required
                                        >
                                        <div id="days-help" class="field-help">
                                            <span>📅</span>
                                            <span>Between 1 and 30 days</span>
                                        </div>
                                        <div id="days-error" class="field-error" role="alert"></div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Step 2: Travel Style & Budget -->
                        <div class="form-section" data-step="2">
                            <div class="section-header">
                                <span class="section-number">2</span>
                                <h3 class="section-title-text">Style & Budget</h3>
                            </div>
                            
                            <div class="field-group">
                                <fieldset class="travel-style-fieldset">
                                    <legend class="field-label">Travel Style</legend>
                                    <div class="travel-style-grid" role="radiogroup" aria-labelledby="travel-style-legend">
                                        <label class="travel-style-card">
                                            <input type="radio" name="travelStyle" value="adventure" class="sr-only">
                                            <div class="travel-style-content">
                                                <span class="travel-style-icon" role="img" aria-label="mountain">🏔️</span>
                                                <h4 class="travel-style-title">Adventure</h4>
                                                <p class="travel-style-description">Outdoor activities, hiking, extreme sports</p>
                                                <div class="travel-style-price">$80-150/day</div>
                                            </div>
                                        </label>
                                        
                                        <label class="travel-style-card">
                                            <input type="radio" name="travelStyle" value="culture" class="sr-only" checked>
                                            <div class="travel-style-content">
                                                <span class="travel-style-icon" role="img" aria-label="museum">🏛️</span>
                                                <h4 class="travel-style-title">Culture</h4>
                                                <p class="travel-style-description">Museums, history, local experiences</p>
                                                <div class="travel-style-price">$100-200/day</div>
                                            </div>
                                        </label>
                                        
                                        <label class="travel-style-card">
                                            <input type="radio" name="travelStyle" value="luxury" class="sr-only">
                                            <div class="travel-style-content">
                                                <span class="travel-style-icon" role="img" aria-label="champagne">🥂</span>
                                                <h4 class="travel-style-title">Luxury</h4>
                                                <p class="travel-style-description">Fine dining, premium hotels, spa</p>
                                                <div class="travel-style-price">$300-500/day</div>
                                            </div>
                                        </label>
                                        
                                        <label class="travel-style-card">
                                            <input type="radio" name="travelStyle" value="backpacker" class="sr-only">
                                            <div class="travel-style-content">
                                                <span class="travel-style-icon" role="img" aria-label="backpack">🎒</span>
                                                <h4 class="travel-style-title">Budget</h4>
                                                <p class="travel-style-description">Hostels, local food, free activities</p>
                                                <div class="travel-style-price">$30-80/day</div>
                                            </div>
                                        </label>
                                    </div>
                                </fieldset>
                                
                                <div class="field-wrapper">
                                    <label for="budgetSlider" class="field-label">
                                        <span>Daily Budget Range</span>
                                    </label>
                                    <div class="budget-slider-container">
                                        <input 
                                            type="range" 
                                            id="budgetSlider" 
                                            name="budget"
                                            class="budget-slider"
                                            min="30" 
                                            max="500" 
                                            value="150"
                                            step="10"
                                            aria-describedby="budget-display"
                                        >
                                        <div class="budget-display" id="budget-display">
                                            <span>Budget per day:</span>
                                            <span class="budget-value" id="budgetValue">$150</span>
                                        </div>
                                        <div class="budget-labels">
                                            <span>$30</span>
                                            <span>$500+</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Step 3: Interests & Preferences -->
                        <div class="form-section" data-step="3">
                            <div class="section-header">
                                <span class="section-number">3</span>
                                <h3 class="section-title-text">Your Interests</h3>
                            </div>
                            
                            <div class="field-group">
                                <fieldset class="interests-fieldset">
                                    <legend class="field-label">What are you interested in?</legend>
                                    <p class="field-help">Select all that apply (minimum 1)</p>
                                    
                                    <div class="interests-section">
                                        <div class="interests-grid" role="group" aria-labelledby="interests-legend">
                                            <div class="interest-tag" data-interest="food" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🍕</span>
                                                <span>Food & Dining</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="art" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🎨</span>
                                                <span>Art & Museums</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="nature" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🌲</span>
                                                <span>Nature & Parks</span>
                                            </div>
                                            
                                            <div class="interest-tag selected" data-interest="photography" tabindex="0" role="button" aria-pressed="true">
                                                <span class="interest-emoji">📸</span>
                                                <span>Photography</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="nightlife" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🌙</span>
                                                <span>Nightlife</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="shopping" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🛍️</span>
                                                <span>Shopping</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="history" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🏛️</span>
                                                <span>History</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="sports" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">⚽</span>
                                                <span>Sports</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="wellness" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🧘</span>
                                                <span>Wellness & Spa</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="music" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🎵</span>
                                                <span>Music & Shows</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="architecture" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🏗️</span>
                                                <span>Architecture</span>
                                            </div>
                                            
                                            <div class="interest-tag" data-interest="beaches" tabindex="0" role="button" aria-pressed="false">
                                                <span class="interest-emoji">🏖️</span>
                                                <span>Beaches</span>
                                            </div>
                                        </div>
                                        <div class="field-error" id="interests-error" role="alert"></div>
                                    </div>
                                </fieldset>
                            </div>
                        </div>

                        <!-- Submit Section -->
                        <div class="submit-section">
                            <button type="submit" class="submit-button" id="submitButton" aria-describedby="submit-status">
                                <div class="button-content">
                                    <span class="button-text">✨ Generate My Perfect Itinerary</span>
                                    <span class="button-spinner hidden" aria-hidden="true"></span>
                                </div>
                            </button>
                            
                            <div id="submit-status" class="submit-status" role="status" aria-live="polite"></div>
                            
                            <p class="submit-disclaimer">
                                🔒 Your data is secure and never shared with third parties
                            </p>
                        </div>
                    </form>
                </div>
            </div>
        </section>

        <!-- Results Section -->
        <section class="results-section hidden" id="resultsSection" aria-labelledby="results-heading">
            <div class="container">
                <div class="state-container">
                    <!-- Loading State -->
                    <div class="loading-state" id="loadingState">
                        <div class="loading-animation">
                            <div class="loading-spinner"></div>
                        </div>
                        <h3>Creating Your Perfect Itinerary</h3>
                        <p class="loading-messages" id="loadingMessages">Analyzing your preferences...</p>
                        <div class="loading-progress">
                            <div class="loading-progress-bar" id="loadingProgressBar"></div>
                        </div>
                    </div>

                    <!-- Error State -->
                    <div class="error-state hidden" id="errorState">
                        <div class="error-icon">⚠️</div>
                        <h3>Oops! Something went wrong</h3>
                        <p class="error-message" id="apiErrorMessage">
                            We encountered an issue generating your itinerary. Please try again.
                        </p>
                        <div class="error-actions">
                            <button type="button" class="btn btn-primary" id="retryButton">
                                <span>🔄</span>
                                <span>Try Again</span>
                            </button>
                            <button type="button" class="btn btn-secondary" id="contactSupportButton">
                                <span>💬</span>
                                <span>Contact Support</span>
                            </button>
                        </div>
                    </div>

                    <!-- Success State -->
                    <div class="success-state hidden" id="successState">
                        <div class="itinerary-header">
                            <h2 id="results-heading">Your Personalized Itinerary</h2>
                            <div class="itinerary-meta">
                                <span class="destination-name" id="resultDestination">Paris, France</span>
                                <span class="trip-duration" id="resultDuration">7 days</span>
                            </div>
                        </div>
                        
                        <div class="itinerary-content">
                            <!-- Budget Summary -->
                            <div class="budget-summary">
                                <h3>💰 Budget Overview</h3>
                                <div class="budget-grid">
                                    <div class="budget-item">
                                        <div class="budget-label">Daily Average</div>
                                        <div class="budget-value" id="dailyBudget">$120</div>
                                    </div>
                                    <div class="budget-item">
                                        <div class="budget-label">Total Estimate</div>
                                        <div class="budget-value primary" id="totalBudget">$840</div>
                                    </div>
                                    <div class="budget-item">
                                        <div class="budget-label">Style</div>
                                        <div class="budget-style" id="budgetStyle">Culture</div>
                                    </div>
                                </div>
                                <div class="budget-breakdown">
                                    <details>
                                        <summary>View detailed breakdown</summary>
                                        <div class="breakdown-content" id="budgetBreakdown">
                                            <!-- Populated by JavaScript -->
                                        </div>
                                    </details>
                                </div>
                            </div>
                            
                            <!-- Itinerary Content -->
                            <div class="itinerary-body">
                                <h3>📅 Your Day-by-Day Plan</h3>
                                <div class="itinerary-text" id="itineraryText">
                                    <!-- Generated itinerary content will be inserted here -->
                                </div>
                            </div>
                            
                            <!-- Action Buttons -->
                            <div class="action-section">
                                <h4>Save & Share Your Itinerary</h4>
                                <div class="action-buttons">
                                    <button type="button" class="btn btn-primary" id="downloadButton">
                                        <span>📄</span>
                                        <span>Download PDF</span>
                                    </button>
                                    
                                    <button type="button" class="btn btn-primary" id="downloadTxtButton">
                                        <span>📝</span>
                                        <span>Download TXT</span>
                                    </button>
                                    
                                    <button type="button" class="btn btn-secondary" id="shareButton">
                                        <span>🔗</span>
                                        <span>Share Link</span>
                                    </button>
                                    
                                    <button type="button" class="btn btn-secondary" id="emailButton">
                                        <span>📧</span>
                                        <span>Email to Me</span>
                                    </button>
                                </div>
                                
                                <div class="secondary-actions">
                                    <button type="button" class="btn btn-outline" id="newTripButton">
                                        <span>✨</span>
                                        <span>Plan Another Trip</span>
                                    </button>
                                    
                                    <button type="button" class="btn btn-outline" id="modifyTripButton">
                                        <span>✏️</span>
                                        <span>Modify This Trip</span>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="site-footer" role="contentinfo">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>TripMate Pro</h4>
                    <p>AI-powered travel planning for the modern explorer</p>
                    <div class="social-links">
                        <a href="#" aria-label="Follow us on Twitter">🐦</a>
                        <a href="#" aria-label="Follow us on Instagram">📸</a>
                        <a href="#" aria-label="Follow us on Facebook">👥</a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h4>Features</h4>
                    <ul>
                        <li><a href="#ai-planning">AI Planning</a></li>
                        <li><a href="#budget-optimization">Budget Tools</a></li>
                        <li><a href="#local-insights">Local Insights</a></li>
                        <li><a href="#mobile-app">Mobile App</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h4>Support</h4>
                    <ul>
                        <li><a href="#help">Help Center</a></li>
                        <li><a href="#contact">Contact Us</a></li>
                        <li><a href="#faq">FAQ</a></li>
                        <li><a href="#api">API Access</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h4>Company</h4>
                    <ul>
                        <li><a href="#about">About</a></li>
                        <li><a href="#careers">Careers</a></li>
                        <li><a href="#privacy">Privacy</a></li>
                        <li><a href="#terms">Terms</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2024 TripMate Pro. Made with ❤️ for travelers everywhere.</p>
                <p class="footer-tech">
                    Built with HTML5, CSS3, JavaScript & AI • 
                    <a href="#accessibility">Accessibility Statement</a>
                </p>
            </div>
        </div>
    </footer>

    <!-- Toast Notifications Container -->
    <div id="toastContainer" class="toast-container" role="region" aria-label="Notifications"></div>

    <!-- Loading Overlay for Full-Screen Operations -->
    <div class="loading-overlay hidden" id="loadingOverlay">
        <div class="overlay-spinner"></div>
        <div class="overlay-message">Processing your request...</div>
    </div>

    <!-- Scripts -->
    <script src="./js/constants.js"></script>
    <script src="./js/utils.js"></script>
    <script src="./js/api.js"></script>
    <script src="./js/components.js"></script>
    <script src="./js/form-validation.js"></script>
    <script src="./js/form-handler.js"></script>
    <script src="./js/app.js"></script>
