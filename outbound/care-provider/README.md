# Care Provider Profile Documentation

This directory contains the data structure specifications for care provider profiles shared with external partners.

## Overview

The care provider profile is a comprehensive data structure containing care provider information suitable for sharing with external partners. All sensitive personal data has been filtered for privacy compliance.

**Schema Location:** [`schema.json`](schema.json)
**Example Data:** [`example.json`](example.json)

---

## Profile Structure

Each care provider profile contains the following sections:

### 1. Personal Information
Basic demographic details including:
- Name (given name and family name)
- Country of origin (EU/EFTA countries)
- Gender
- Date of birth

### 2. Work Experience
Professional qualifications and experience:
- German language proficiency (e.g., BASIC, INTERMEDIATE, ...)
- Years of experience in Germany
- Total years of care experience
- Driver's license status
- Care activities performed (e.g., DRESSING, FEEDING, ...)
- Health conditions managed (e.g., DIABETES, INCONTINENCE, ...)

### 3. Preferences
Care provider's requirements and preferences for assignments:
- Salary expectations (monthly, in EUR)
- Days needed between assignments
- Availability date
- Environmental preferences (smoking household, pets, urban/rural, etc.)
- Care recipient characteristics (mobility level, dementia severity, gender preference)
- Preferred care activities and conditions
- Lifting capability requirements (e.g., LIGHT, MEDIUM, ...)

### 4. Assessment
Platform-generated profile information:
- Hobbies and interests (e.g., COOKING, READING_BOOKS, ...)
- Smoking status
- AI-generated introduction text

### 5. Communication
- Platform language preference (e.g., DE, EN, ...)

### 6. Documents
- Profile picture URL (optional)

---

## Key Data Types

The schema includes comprehensive enumerations for various attributes. For complete and up-to-date values, please refer to the [`schema.json`](schema.json) file.

**Examples of enumerated types:**
- **Care Activities:** DRESSING, FEEDING, ...
- **Health Conditions:** DIABETES, INCONTINENCE, ...
- **Mobility Levels:** ROLLATOR, WHEELCHAIR, ...
- **Dementia Severity:** NONE, MILD, ...
- **Hobbies:** COOKING, READING_BOOKS, ...
- **Language Proficiency:** BASIC, INTERMEDIATE, ...
- **Lifting Capability:** LIGHT, MEDIUM, ...

---

## Technical Details

### Schema Format
- **Standard:** JSON Schema Draft 07
- **Validation:** All profiles must conform to the schema specification
- **Versioning:** Each profile includes a version UUID for change tracking

### Version Tracking
Each care provider profile includes:
- `id`: Unique profile identifier (UUID)
- `version`: Version identifier (UUID) that changes with each profile update
