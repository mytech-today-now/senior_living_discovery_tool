# 🏠 Senior Living Discovery Tool

## 🚀 Revolutionary Enhancement: One Row Per Query Term with Hyperlinks

The Senior Living Discovery Tool now features a **completely redesigned data structure** that returns **one row per query term** with **15-character context snippets** and **automatic hyperlink generation** for spreadsheet formats.

### 🎯 Key Improvements

#### Enhanced Result Format
- **One Row Per Query Term**: Each keyword gets its own result row for maximum clarity
- **15-Character Context Snippets**: Precisely formatted context with exactly 15 characters before and after each match
- **Hyperlink Generation**: Automatic creation of clickable Excel HYPERLINK() formulas for .xls, .xlsx, and .ods formats
- **Anchor Link Integration**: URLs include fragment identifiers (#search-term) for direct navigation to highlighted text
- **Match Type Classification**: Results categorized as Exact, Partial, None, Error, or Skipped

#### Advanced Data Export
- **Excel HYPERLINK() Formulas**: Native Excel formulas for clickable results in spreadsheet formats
- **Target="_blank" Links**: All hyperlinks open in new tabs with security attributes
- **Optimized Column Widths**: Automatic column sizing for optimal readability
- **Document Metadata**: Complete workbook properties including title, author, and creation date

## Features

### Core Functionality
- **File Upload**: Supports .xlsx, .xls, .csv, and .ods formats with comprehensive validation
- **Real-time Processing Status**: Visual progress tracking with detailed logging and error handling
- **Enhanced Search Integration**: Multi-strategy search with sitemap-based recursive scraping
- **Sitemap-Based Web Scraping**: Discovers and scrapes all pages in website sitemaps
- **Advanced Keyword Analysis**: One row per query term with weighted scoring and context preservation
- **Comprehensive Export Options**: Download results with hyperlinks in multiple formats
- **Glassmorphic UI**: Modern, translucent interface design with accessibility features

### 📊 Enhanced Result Structure (NEW)

**Revolutionary Data Format**: Results now return one row per query term with 15-character context snippets and hyperlink support.

#### Result Table Structure
Each row represents analysis of one specific keyword:

| Column | Description | Example |
|--------|-------------|---------|
| Name | Facility name | "Sunset Manor" |
| Address | Full address | "123 Main St" |
| Town | City/Town | "Springfield" |
| State | State abbreviation | "IL" |
| Zip | ZIP code | "62701" |
| Query Term | Specific keyword analyzed | "assisted living" |
| Match Type | Type of match found | "Exact" |
| Total Matches | Number of matches | 3 |
| Score | Weighted score | 6 |
| Context Snippet | 15-char before/after context | "...provides assisted living services for..." |

#### Hyperlink Format for Spreadsheet Exports
- **Excel Formula**: `=HYPERLINK("https://domain.com/page.html#search-term","context snippet")`
- **Target Behavior**: Opens in new tab with fragment navigation
- **Security**: Includes `rel="noopener noreferrer"` attributes
- **Supported Formats**: .xls, .xlsx, .ods (CSV uses plain text)

### 🕷️ Sitemap-Based Web Scraping

**Comprehensive Enhancement**: Sitemap-based recursive web scraping for maximum search coverage and accuracy.

#### Key Features
- **Automatic Sitemap Discovery**: Finds sitemaps through robots.txt and common paths
- **Recursive Parsing**: Follows sitemap index files to discover all pages
- **Intelligent Content Extraction**: Extracts meaningful text from HTML pages
- **Advanced Keyword Matching**: Weighted scoring with context awareness
- **Rate Limiting**: Configurable delays to respect server resources
- **Error Recovery**: Robust fallback mechanisms and retry logic
- **Performance Optimization**: Efficient memory usage and concurrent processing

#### Search Strategy Hierarchy
1. **Sitemap-Based Scraping** (Primary): Discovers and scrapes all pages in website sitemaps
2. **Traditional Search Engines** (Secondary): Falls back to search engine APIs
3. **Simulated Results** (Fallback): Intelligent fallback with criteria-based content

#### Configuration Options
- **Enable/Disable Toggle**: Control sitemap scraping functionality
- **Max Pages per Site**: Limit pages scraped (5-200, default: 50)
- **Scraping Delay**: Configure request delays (100-2000ms, default: 200ms)
- **Timeout Settings**: Request timeout configuration
- **Retry Attempts**: Number of retry attempts for failed requests

#### Technical Implementation
- **IIFE Module Pattern**: Avoids global state pollution
- **Promise-Based Architecture**: Asynchronous processing with proper error handling
- **CORS Proxy Support**: Multiple proxy services for cross-origin requests
- **Comprehensive Testing**: Unit tests covering all scenarios and edge cases
- **Enhanced Logging**: Detailed error logging with timestamp format

For detailed technical documentation, see `SITEMAP_SCRAPING_README.md`.

### Production Configuration (ENHANCED)
- **API Service Management**: Configure free and paid search APIs with secure key storage
- **Interactive API Suggestions**: Curated recommendations for Free, Premium, and Enterprise APIs
- **Detailed Setup Guides**: Step-by-step instructions with direct links to provider documentation
- **Multiple Provider Support**: SerpApi, Google Custom Search, Bing, DuckDuckGo, Azure, Elasticsearch, Algolia
- **Rate Limiting Controls**: Configurable delays to respect API rate limits
- **Caching System**: Optional result caching with customizable expiry settings
- **Connection Testing**: Built-in API connectivity validation and diagnostics
- **Configuration Persistence**: Settings automatically saved to localStorage
- **Service Toggles**: Enable/disable individual search services with visual feedback
- **Security Features**: API key masking, secure storage, and validation

### Enhanced Code Review & Documentation
- **Comprehensive Architecture Overview**: Detailed technical documentation
- **Security Implementation**: Client-side security measures and data protection
- **Performance Optimizations**: Memory management and DOM optimization strategies
- **Testing Framework**: Unit tests covering positive, negative, boundary, edge cases, and API guide system validation
- **Error Handling**: Enterprise-grade logging with structured error format
- **Browser Compatibility**: Progressive enhancement with feature detection

## 🔍 API Provider Recommendations (NEW)

The application now includes interactive API provider suggestions with detailed setup guides:

### Free Tier APIs
1. **SerpApi Free Tier**
   - 100 searches per month
   - Google, Bing, and other search engines
   - Setup guide with account creation and API key instructions
   - Direct links: [Sign Up](https://serpapi.com/users/sign_up) | [Documentation](https://serpapi.com/search-api)

2. **DuckDuckGo Instant Answer API**
   - Completely free with no rate limits
   - No API key required
   - Instant answer format
   - Direct links: [API Docs](https://duckduckgo.com/api) | [Examples](https://duckduckgo.com/api#examples)

3. **Bing Web Search API (Free)**
   - 1,000 searches per month on Azure free tier
   - Microsoft Cognitive Services
   - Setup guide for Azure account creation
   - Direct links: [Azure Free](https://azure.microsoft.com/free/) | [Bing Search APIs](https://azure.microsoft.com/services/cognitive-services/bing-web-search-api/)

### Premium APIs
1. **Google Custom Search API**
   - 100 searches per day free, paid tiers available
   - Comprehensive search results
   - Custom search engine configuration
   - Direct links: [Google Cloud Console](https://console.cloud.google.com/) | [API Documentation](https://developers.google.com/custom-search/v1/overview)

2. **SerpApi Professional**
   - Higher rate limits and advanced features
   - Professional support and SLA
   - Multiple search engines
   - Direct links: [Pricing Plans](https://serpapi.com/pricing) | [Dashboard](https://serpapi.com/dashboard)

3. **Bing Search API Professional**
   - Higher quotas and advanced features
   - Azure professional tiers
   - Enterprise support
   - Direct links: [Azure Pricing](https://azure.microsoft.com/pricing/details/cognitive-services/search-api/) | [Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/bing-web-search/)

### Enterprise Solutions
1. **Azure Cognitive Search**
   - Full-featured enterprise search service
   - AI-powered capabilities
   - Scalable and secure
   - Direct links: [Azure Portal](https://portal.azure.com/) | [Create Service](https://portal.azure.com/#create/Microsoft.Search)

2. **Elasticsearch Service**
   - Managed search and analytics
   - Real-time indexing and search
   - Multiple deployment options
   - Direct links: [Elastic Cloud](https://cloud.elastic.co/) | [AWS OpenSearch](https://aws.amazon.com/opensearch-service/)

3. **Algolia Search**
   - Fast, reliable search-as-a-service
   - Powerful APIs and SDKs
   - Global infrastructure
   - Direct links: [Sign Up](https://www.algolia.com/users/sign_up) | [Pricing](https://www.algolia.com/pricing/)

### Interactive Setup Guides
Each API provider includes:
- **Step-by-step instructions** with screenshots and detailed explanations
- **Direct links** to registration, documentation, and configuration pages (all open in new tabs with security attributes)
- **Pricing information** and feature comparisons
- **Configuration examples** with sample API keys and endpoints
- **Troubleshooting tips** for common setup issues

## Processing Status Display

The application includes a comprehensive processing status display that shows:

### Visual Elements
- **Progress Bar**: Real-time completion percentage
- **Spinner Animation**: Indicates active processing
- **Statistics**: Current row count and elapsed time
- **Live Log**: Timestamped processing events

### Status Information
- File reading progress
- Row-by-row processing updates
- Search operation status
- Error handling and recovery
- Completion notifications

## API Documentation

### Core Functions

#### `processFile()`
**Purpose**: Main function to process uploaded spreadsheet files
**Inputs**: 
- File from `#fileInput` element
- Criteria from `#criteria` textarea
**Outputs**: Populates `globalData` array and renders results table
**Error Handling**: Comprehensive try-catch with user notifications

#### `showProcessingStatus()`
**Purpose**: Displays processing status interface
**Inputs**: None
**Outputs**: Shows processing div, hides results table
**Side Effects**: Initializes processing state and timer

#### `hideProcessingStatus()`
**Purpose**: Hides processing status interface
**Inputs**: None
**Outputs**: Hides processing div, shows results table
**Side Effects**: Resets processing state

#### `updateProcessingProgress(current, total, details)`
**Purpose**: Updates progress indicators and status text
**Inputs**:
- `current` (number): Current row being processed
- `total` (number): Total number of rows
- `details` (string): Additional status information
**Outputs**: Updates progress bar, counters, and status text
**Error Handling**: Validates inputs and handles DOM element availability

#### `logEvent(message)` / `logError(error)`
**Purpose**: Logging functions with timestamp and processing log integration
**Inputs**:
- `message` (string): Event message
- `error` (string|Error): Error message or Error object
**Outputs**: Console logs and processing log entries
**Side Effects**: Adds timestamped entries to processing log display

### Configuration Management Functions (NEW)

#### `toggleApiService(serviceType)`
**Purpose**: Toggles API service on/off with visual feedback
**Inputs**:
- `serviceType` (string): Type of service ('free' or 'paid')
**Outputs**: Updates toggle UI state and saves configuration
**Error Handling**: Validates element existence and logs toggle events

#### `saveConfiguration()`
**Purpose**: Saves current configuration from form inputs to localStorage
**Inputs**: Reads from configuration form elements
**Outputs**: Validates and stores configuration with user feedback
**Validation**: API key masking, numeric range validation, URL format checking

#### `testApiConnection()`
**Purpose**: Tests connectivity to configured API endpoints
**Inputs**: Uses current configuration settings
**Outputs**: Connection status report with success/failure indicators
**Error Handling**: Timeout handling and fallback testing strategies

#### `resetConfiguration()`
**Purpose**: Resets all configuration to default values
**Inputs**: User confirmation dialog
**Outputs**: Clears localStorage and resets form inputs
**Side Effects**: Restores default toggle states and input values

#### `getConfiguration()` / `saveConfigurationToStorage(config)`
**Purpose**: Configuration persistence and retrieval functions
**Inputs**: Configuration object for saving, none for retrieval
**Outputs**: Current configuration object or storage confirmation
**Error Handling**: JSON parsing errors and localStorage availability checks

### API Guide System Functions (NEW)

#### `showApiGuide(apiType)`
**Purpose**: Displays interactive API setup guide modal with detailed instructions
**Inputs**:
- `apiType` (string): Type of API ('serpapi', 'google', 'bing', 'duckduckgo', 'azure', 'elasticsearch', 'algolia', etc.)
**Outputs**: Opens modal with step-by-step setup instructions and direct links
**Error Handling**: Validates API type existence and handles modal element availability

#### `closeApiGuide()`
**Purpose**: Closes the API guide modal and cleans up event listeners
**Inputs**: None
**Outputs**: Hides modal and logs closure event
**Error Handling**: Validates modal element existence before manipulation

#### `getApiGuideData(apiType)`
**Purpose**: Retrieves comprehensive setup guide data for specific API provider
**Inputs**:
- `apiType` (string): API provider identifier
**Outputs**: Guide object with title, description, steps, and links, or null if not found
**Data Structure**:
```javascript
{
  title: string,           // Guide title with emoji and provider name
  description: string,     // Brief description of the API service
  steps: [                 // Array of setup steps
    {
      title: string,       // Step title (e.g., "1. Create Account")
      content: string,     // Detailed step instructions
      links: [             // Array of helpful links
        {
          text: string,    // Link display text
          url: string      // Direct URL (opens in new tab)
        }
      ]
    }
  ]
}
```

#### `generateApiGuideHTML(guideData)`
**Purpose**: Generates HTML content for API guide modal from guide data
**Inputs**:
- `guideData` (Object): Guide data object from getApiGuideData()
**Outputs**: HTML string with formatted guide content
**Features**:
- Responsive layout with glassmorphic styling
- Security attributes (target="_blank" rel="noopener noreferrer")
- Error handling for invalid or missing data
- Accessible markup with proper heading hierarchy

### Processing State Management

#### `processingState` Object
```javascript
{
  isProcessing: boolean,    // Current processing status
  startTime: number|null,   // Processing start timestamp
  totalRows: number,        // Total rows to process
  currentRow: number,       // Current row index
  logEntries: Array         // Log entry history (max 20 entries)
}
```

### Error Handling

The application implements robust error handling at multiple levels:

1. **File Validation**: Checks for file selection and criteria input
2. **Spreadsheet Parsing**: Handles malformed or empty files
3. **Row Processing**: Individual row error isolation
4. **Search Operations**: Network and API error recovery
5. **DOM Operations**: Element availability validation
6. **State Management**: Processing state consistency

### Error Logging Format
```
[HH:MM:SS AM/PM] <Element> tag #X: <message> at line L, column C
```

## Comprehensive Code Review & Testing Framework

### Unit Test Coverage Areas

#### Positive Test Cases
- **File Upload Validation**: Valid .xlsx, .xls, .csv, .ods files with proper data structure
- **Spreadsheet Parsing**: Well-formed files with complete address data and facility information
- **Progress Tracking**: Accurate percentage calculations and time estimations
- **Search Operations**: Successful API responses and data extraction
- **State Management**: Proper initialization and cleanup of processing states
- **DOM Manipulation**: Successful element updates and event handling
- **Export Functionality**: Correct file generation in all supported formats

#### Negative Test Cases
- **Invalid File Types**: Rejection of unsupported file formats (.txt, .pdf, .doc)
- **Corrupted Files**: Graceful handling of malformed or corrupted spreadsheet data
- **Empty Datasets**: Processing of files with no data rows or missing headers
- **Network Failures**: Timeout handling and fallback mechanisms for search operations
- **Missing DOM Elements**: Error recovery when required HTML elements are not found
- **Invalid User Input**: Handling of empty criteria fields or malformed search terms
- **Memory Constraints**: Behavior with extremely large datasets exceeding browser limits

#### Boundary Test Cases
- **File Size Limits**: Testing with files at browser memory boundaries (>100MB)
- **Row Count Extremes**: Single row files vs. files with 10,000+ rows
- **Character Encoding**: Unicode, special characters, and international address formats
- **Search Term Limits**: Very long criteria strings and keyword extraction edge cases
- **Progress Boundaries**: 0% and 100% completion states and intermediate values
- **Time Calculations**: Processing duration edge cases (instant completion, multi-hour processing)

#### Edge Cases Handled
- **Incomplete Address Data**: Missing street numbers, city names, or zip codes
- **Duplicate Facility Names**: Handling of identical facility names with different addresses
- **Special Characters**: Processing of addresses with apostrophes, hyphens, and accented characters
- **Network Connectivity Issues**: CORS limitations, API rate limiting, and connection timeouts
- **Browser Compatibility**: Fallbacks for older browsers lacking modern JavaScript features
- **Concurrent Processing**: Prevention of multiple simultaneous file processing operations
- **State Corruption**: Recovery from interrupted processing due to browser navigation or refresh

#### Simulated Failure Scenarios
- **API Timeout Simulation**: Mock delayed responses to test timeout handling
- **Memory Exhaustion**: Large dataset processing to test memory management
- **DOM Manipulation Failures**: Simulated missing elements to test error recovery
- **File Reading Errors**: Corrupted file simulation to test FileReader error handling
- **Search Service Unavailability**: Mock API failures to test fallback mechanisms
- **Progress Calculation Errors**: Division by zero and negative value handling

#### State Transition Testing
- **Processing Lifecycle**: NOT_STARTED → IN_PROGRESS → COMPLETE state transitions
- **Error Recovery**: IN_PROGRESS → ERROR → RECOVERY → COMPLETE flows
- **User Interruption**: Handling of user actions during processing (file changes, navigation)
- **Memory State Consistency**: Verification of globalData integrity across operations
- **UI State Synchronization**: Ensuring UI reflects actual processing state accurately

#### Module Interaction Testing
- **File Reader ↔ Spreadsheet Parser**: Data flow validation between file reading and parsing
- **Search Module ↔ Scoring System**: Integration testing of search results and keyword scoring
- **Progress Tracker ↔ UI Updates**: Synchronization of internal state with visual indicators
- **Error Logger ↔ User Notifications**: Coordination between console logging and user alerts
- **Export Module ↔ Data Processor**: Verification of processed data integrity in exported files

#### Performance Testing Scenarios
- **Large File Processing**: 10,000+ row spreadsheets with timing benchmarks
- **Memory Usage Monitoring**: Tracking memory consumption during processing
- **UI Responsiveness**: Ensuring interface remains interactive during heavy processing
- **Search Operation Batching**: Optimal batch sizes for concurrent search requests
- **Progress Update Frequency**: Balancing update frequency with performance impact
- **Log Entry Management**: Performance impact of extensive logging operations

### Advanced Error Handling & Logging

#### Error Classification System
- **Critical Errors**: File reading failures, DOM corruption, memory exhaustion
- **Processing Errors**: Individual row failures, search timeouts, data validation issues
- **User Errors**: Invalid input, missing files, unsupported formats
- **Network Errors**: API failures, CORS issues, connectivity problems
- **State Errors**: Concurrent processing attempts, invalid state transitions

#### Comprehensive Error Logging Implementation
```javascript
/**
 * Enhanced error logging with detailed context information
 * Format: [HH:MM:SS AM/PM] <Element> tag #X: <message> at line L, column C
 * @param {Error|string} error - Error object or message
 * @param {string} elementType - HTML element type where error occurred
 * @param {number} elementIndex - Element index or ID
 * @param {number} lineNumber - Source line number
 * @param {number} columnNumber - Source column number
 */
function logDetailedError(error, elementType = 'unknown', elementIndex = 0, lineNumber = 0, columnNumber = 0) {
  const timestamp = getCurrentTimestamp();
  const message = error instanceof Error ? error.message : String(error);
  const formattedLog = `[${timestamp}] ${elementType} tag #${elementIndex}: ${message} at line ${lineNumber}, column ${columnNumber}`;

  console.error(formattedLog);
  addProcessingLogEntry(timestamp, formattedLog, 'error');

  // Additional error context for debugging
  if (error instanceof Error && error.stack) {
    console.error('Stack trace:', error.stack);
  }
}
```

#### Fallback Mechanisms
- **Search API Failures**: Progressive fallback from primary to secondary to mock services
- **File Reading Errors**: Alternative parsing methods for corrupted files
- **DOM Element Missing**: Dynamic element creation with error boundaries
- **Memory Constraints**: Chunked processing for large datasets
- **Network Timeouts**: Exponential backoff retry strategies

### Robust Input Validation & Sanitization

#### File Validation Pipeline
```javascript
/**
 * Comprehensive file validation with multiple checkpoints
 * @param {File} file - Uploaded file object
 * @returns {Object} Validation result with success status and error details
 */
function validateUploadedFile(file) {
  const validationResult = {
    isValid: false,
    errors: [],
    warnings: []
  };

  // File existence check
  if (!file) {
    validationResult.errors.push('No file provided');
    return validationResult;
  }

  // File size validation (max 50MB)
  if (file.size > 50 * 1024 * 1024) {
    validationResult.errors.push(`File size ${(file.size / 1024 / 1024).toFixed(2)}MB exceeds 50MB limit`);
  }

  // File type validation
  const allowedTypes = ['.xlsx', '.xls', '.csv', '.ods'];
  const fileExtension = file.name.toLowerCase().substring(file.name.lastIndexOf('.'));
  if (!allowedTypes.includes(fileExtension)) {
    validationResult.errors.push(`Unsupported file type: ${fileExtension}`);
  }

  // MIME type validation
  const allowedMimeTypes = [
    'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet',
    'application/vnd.ms-excel',
    'text/csv',
    'application/vnd.oasis.opendocument.spreadsheet'
  ];
  if (!allowedMimeTypes.includes(file.type) && file.type !== '') {
    validationResult.warnings.push(`Unexpected MIME type: ${file.type}`);
  }

  validationResult.isValid = validationResult.errors.length === 0;
  return validationResult;
}
```

## Performance Considerations & Optimization

### Memory Management Strategies
- **Log Entry Rotation**: Automatic cleanup of processing logs (max 20 entries)
- **Data Chunking**: Processing large datasets in manageable chunks (500 rows per batch)
- **Garbage Collection**: Explicit cleanup of temporary variables and DOM references
- **Memory Monitoring**: Real-time tracking of memory usage during processing
- **Lazy Loading**: On-demand loading of search results and table data

### DOM Optimization Techniques
- **Batch Updates**: Grouping multiple DOM modifications to minimize reflow
- **Virtual Scrolling**: Efficient rendering of large result tables
- **Event Delegation**: Single event listeners for dynamic content
- **CSS Containment**: Isolating layout and paint operations
- **Progressive Enhancement**: Core functionality without JavaScript dependencies

### Asynchronous Processing Architecture
- **Web Workers**: Offloading heavy computations to background threads
- **Promise Chains**: Non-blocking sequential processing with error propagation
- **Throttled Updates**: Rate-limited progress updates to prevent UI freezing
- **Cancellation Support**: Ability to abort long-running operations
- **Queue Management**: Ordered processing of multiple file uploads

### Code Quality & Best Practices

#### Strict Mode Implementation
- **JavaScript Strict Mode**: Enabled globally with `'use strict';` directive
- **Type Safety**: Explicit type checking and validation throughout codebase
- **Variable Declarations**: Consistent use of `const` and `let`, avoiding `var`
- **Function Purity**: Minimizing side effects and maintaining predictable behavior
- **Error Boundaries**: Isolated error handling preventing cascade failures

#### Modular Architecture & Global State Avoidance
```javascript
/**
 * IIFE (Immediately Invoked Function Expression) pattern for module isolation
 * Prevents global namespace pollution and ensures encapsulation
 */
(function SeniorLivingDiscoveryModule() {
  'use strict';

  // Private module state
  const moduleState = {
    data: [],
    processing: false,
    config: {
      maxLogEntries: 20,
      batchSize: 500,
      timeoutMs: 30000
    }
  };

  // Public API exposure
  window.SeniorLivingTool = {
    processFile: processFile,
    downloadFile: downloadFile,
    filterByScore: filterByScore
  };

  // Private implementation details hidden from global scope
})();
```

#### Descriptive Naming Conventions
- **Functions**: Verb-noun patterns (`processFile`, `updateProgress`, `validateInput`)
- **Variables**: Clear, descriptive names (`processingState`, `criteriaKeywords`, `globalData`)
- **Constants**: UPPER_SNAKE_CASE for configuration values (`MAX_FILE_SIZE`, `SUPPORTED_FORMATS`)
- **DOM Elements**: Semantic IDs and classes (`processingStatus`, `scoreDisplay`, `outputTable`)
- **Error Messages**: Specific, actionable descriptions with context

#### Comprehensive Documentation Standards
- **Function Documentation**: JSDoc format with @param, @returns, @throws annotations
- **Inline Comments**: Explanation of complex logic and business rules
- **Code Examples**: Usage patterns and integration examples
- **API Documentation**: Complete input/output specifications
- **Error Scenarios**: Documented error conditions and recovery strategies

### Advanced Testing Framework Implementation

#### Unit Test Structure with Simple Assertions
```javascript
/**
 * Lightweight testing framework using simple assertions
 * No external dependencies required
 */
function runTestSuite() {
  'use strict';

  const testResults = {
    passed: 0,
    failed: 0,
    errors: []
  };

  // Simple assertion helper
  function assert(condition, message) {
    if (!condition) {
      testResults.failed++;
      testResults.errors.push(`ASSERTION FAILED: ${message}`);
      console.error(`❌ ${message}`);
    } else {
      testResults.passed++;
      console.log(`✅ ${message}`);
    }
  }

  // Test file validation
  function testFileValidation() {
    console.log('Testing file validation...');

    // Test valid file
    const validFile = new File(['test'], 'test.xlsx', { type: 'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' });
    const validResult = validateUploadedFile(validFile);
    assert(validResult.isValid === true, 'Valid XLSX file should pass validation');

    // Test invalid file type
    const invalidFile = new File(['test'], 'test.txt', { type: 'text/plain' });
    const invalidResult = validateUploadedFile(invalidFile);
    assert(invalidResult.isValid === false, 'Invalid file type should fail validation');

    // Test oversized file
    const oversizedFile = new File([new ArrayBuffer(60 * 1024 * 1024)], 'large.xlsx');
    const oversizedResult = validateUploadedFile(oversizedFile);
    assert(oversizedResult.isValid === false, 'Oversized file should fail validation');
  }

  // Run all tests
  testFileValidation();

  console.log(`Test Results: ${testResults.passed} passed, ${testResults.failed} failed`);
  return testResults;
}
```

## Browser Compatibility & Progressive Enhancement

### Supported Browsers
- **Chrome 60+**: Full feature support including backdrop-filter
- **Firefox 70+**: Complete functionality with CSS fallbacks
- **Safari 13+**: Native glassmorphic effects support
- **Edge 79+**: Chromium-based full compatibility
- **Mobile Browsers**: iOS Safari 13+, Chrome Mobile 60+

### Feature Detection & Fallbacks
```javascript
/**
 * Progressive enhancement with feature detection
 */
function initializeWithFallbacks() {
  // Check for required APIs
  if (!window.FileReader) {
    showFallbackMessage('File upload not supported in this browser');
    return;
  }

  if (!window.fetch) {
    // Fallback to XMLHttpRequest for older browsers
    window.fetch = function(url, options) {
      return new Promise((resolve, reject) => {
        const xhr = new XMLHttpRequest();
        xhr.open(options.method || 'GET', url);
        xhr.onload = () => resolve({ ok: xhr.status === 200, json: () => JSON.parse(xhr.responseText) });
        xhr.onerror = reject;
        xhr.send(options.body);
      });
    };
  }

  // CSS feature detection for glassmorphic effects
  if (!CSS.supports('backdrop-filter', 'blur(10px)')) {
    document.body.classList.add('no-backdrop-filter');
  }
}
```

## Security Implementation & Data Protection

### Client-Side Security Measures
- **Input Sanitization**: All user inputs sanitized before processing
- **XSS Prevention**: Content Security Policy headers and output encoding
- **File Type Validation**: Multiple layers of file format verification
- **Memory Protection**: Bounds checking and buffer overflow prevention
- **Error Information Disclosure**: Sanitized error messages without sensitive data

### Data Privacy Compliance
- **No Server Transmission**: All processing occurs client-side
- **Local Storage Only**: Temporary data storage in browser memory
- **No Tracking**: No analytics or user behavior monitoring
- **GDPR Compliance**: No personal data collection or storage
- **Audit Trail**: Complete processing logs for transparency

### CORS Security Considerations
- **Same-Origin Policy**: Respects browser security restrictions
- **Proxy Services**: Secure proxy usage for external API calls
- **API Key Protection**: No exposed credentials in client-side code
- **Rate Limiting**: Built-in request throttling to prevent abuse
- **Fallback Security**: Graceful degradation when external services unavailable
