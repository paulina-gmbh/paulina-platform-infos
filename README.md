# Paulina24 Platform Information

This repository provides technical documentation and data structure specifications for partners integrating with the Paulina24 platform.

## About Paulina24

Paulina24 GmbH operates a digital platform that connects independent care providers with families seeking 24-hour live-in care for elderly individuals in Germany. The platform handles the complete administrative burden including care provider onboarding, regulatory compliance, insurance coordination, and payment processing, enabling transparent and fair compensation for care professionals.

**Key Services:**
- Matching care providers with families needing elderly care
- Administrative support (business registration, tax filing, insurance)
- Payment processing and salary disbursement
- Communication support during care assignments

**Website:** [www.paulina24.de](https://www.paulina24.de)

---

## Repository Structure

```
paulina-platform-infos/
├── README.md
└── outbound/
    └── care-provider/
        ├── README.md      # Care provider profile documentation
        ├── schema.json    # JSON Schema for care provider profiles
        └── example.json   # Example care provider profile data
```

### Outbound Directory

The `outbound/` directory contains data structures and schemas for information shared with external partners and systems. These represent privacy-filtered, partner-safe representations of internal platform data.

---

## Available Data Structures

### Care Provider Profiles

Comprehensive care provider profile data including personal information, work experience, preferences, and qualifications.

**📁 Documentation:** [outbound/care-provider/README.md](outbound/care-provider/README.md)

The care provider profile contains:
- Personal information (name, country, gender, date of birth)
- Work experience and qualifications
- Assignment preferences and requirements
- Platform assessment and generated content
- Communication preferences
- Document references

All profiles conform to JSON Schema Draft 07 and include version tracking for change management.
