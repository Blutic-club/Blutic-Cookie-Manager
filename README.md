# Blutic Cookie Manager - GTM Community Template

A Google Tag Manager community template for implementing cookie consent management with region-specific consent settings and Google Consent Mode v2 support.

## Overview

The Blutic Cookie Manager template integrates your website with the Blutic Cookie Management platform, providing DPDP/privacy-compliant cookie consent banners with customizable designs and advanced consent management features.

## Features

- **Easy Integration**: Simply enter your Domain ID to connect with your Blutic Cookie Manager configuration
- **Google Consent Mode v2**: Full support for consent mode with granular controls:
  - Ad Storage
  - Analytics Storage
  - Ad Personalization
  - Ad User Data
  - Functionality Storage
  - Security Storage
- **Region-Specific Settings**: Configure different default consent states for different countries/regions
- **Auto-Block Tracking**: Optional automatic blocking of tracking scripts until user consent is given
- **DataLayer Events**: Automatic consent events pushed to GTM dataLayer for enhanced tracking

## Installation

1. Go to **Templates** in your Google Tag Manager container
2. Click **Search Gallery** in the Tag Templates section
3. Search for "Blutic Cookie Manager"
4. Click **Add to Workspace**
5. Accept the permissions

## Configuration

### Required Settings

**Domain ID** (Required)

- Enter your unique Domain ID from the Blutic Cookie Manager platform
- Find this ID after creating your consent banner at https://cookie-management.blutic.club

### Optional Settings

**Auto Block Tracking**

- When enabled, blocks all tracking and analytics scripts by default
- Scripts only run after users explicitly give consent via your banner

**Region-Specific Consent Settings**

- Configure default consent values for different countries or regions
- Add one row per region group with different requirements
- Use `all` for global fallback settings

For each region, configure:

- **Region**: Comma-separated ISO country codes (e.g., `US,CA`) or `all`
- **Ad Storage**: Default consent for advertising cookies
- **Analytics Storage**: Default consent for analytics (e.g., Google Analytics)
- **Ad Personalization**: Default consent for personalized ads
- **Ad User Data**: Default consent for sharing user data with Google
- **Functional Storage**: Default consent for functionality cookies
- **Wait for Update**: Delay in milliseconds for consent update (default: 500ms)

## Usage

1. Create a new tag using the Blutic Cookie Manager template
2. Enter your Domain ID
3. Configure your consent settings (optional)
4. Set the tag to fire on **All Pages** with trigger type **Consent Initialization**
5. Save and publish your container

## DataLayer Events

The template pushes the following events to dataLayer:

- `consent_default_global`: Global consent defaults applied
- `consent_default_region`: Region-specific consent applied
- `banner_sdk_loaded`: Banner SDK loaded successfully
- `banner_sdk_load_failed`: Banner SDK failed to load

## Documentation

For detailed setup instructions and banner customization, visit:
https://www.blutic.club/guides/google-tag-manager-user-guide

## Support

For issues or questions:

- Visit: https://www.blutic.club
- Documentation: https://www.blutic.club/guides/google-tag-manager-user-guide

## License

See LICENSE file for details.

## Privacy & Compliance

This template is designed to help websites comply with DPDP, GDPR, and other privacy regulations by implementing proper cookie consent management. The template integrates with Google's Consent Mode v2 for enhanced privacy controls.
