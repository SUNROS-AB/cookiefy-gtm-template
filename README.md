# Cookiefy - Consent Mode Template

A Google Tag Manager template for [Cookiefy](https://cookiefy.app) cookie consent banner with full Google Consent Mode v2 support.

## Features

- ✅ **Google Consent Mode v2** - Supports all required consent types:
  - `ad_storage`
  - `ad_user_data` (new in v2)
  - `ad_personalization` (new in v2)
  - `analytics_storage`
  - `functionality_storage`
  - `personalization_storage`
  - `security_storage`

- ✅ **Automatic Consent Restoration** - Reads existing consent from cookie on page load
- ✅ **Real-time Updates** - Instantly updates consent state when user interacts with banner
- ✅ **Region-Specific Defaults** - Configure different consent defaults per region (ISO codes)
- ✅ **URL Passthrough** - Pass ad click information through URL parameters
- ✅ **Ads Data Redaction** - Further redact ad data when consent is denied

## Installation

### Option 1: Import from Community Template Gallery
1. In GTM, go to **Templates** > **Tag Templates** > **Search Gallery**
2. Search for "Cookiefy"
3. Click **Add to workspace**

### Option 2: Manual Import
1. Download the `.tpl` file from this repository
2. In GTM, go to **Templates** > **Tag Templates** > **New**
3. Click the three-dot menu > **Import**
4. Select the downloaded file

## Configuration

### Required Settings
| Parameter | Description |
|-----------|-------------|
| **Domain ID** | Your Cookiefy Domain ID (found in your dashboard) |

### Default Consent Settings
Configure the default consent state for each consent type. For GDPR compliance, these should typically be set to "Denied".

### Region-Specific Settings (Optional)
Override consent defaults for specific regions using ISO country codes (e.g., "US", "SE", "DE").

### Advanced Settings
| Parameter | Description | Default |
|-----------|-------------|---------|
| URL Passthrough | Pass ad click info in URL parameters | Disabled |
| Ads Data Redaction | Further redact ad data when denied | Disabled |
| Wait for Update | Time to wait for consent before firing tags | 500ms |

## Usage

1. **Create a new Tag** using the Cookiefy template
2. **Set the trigger** to "Consent Initialization - All Pages"
3. **Enter your Domain ID** from Cookiefy dashboard
4. **Configure defaults** (typically all "Denied" for GDPR)
5. **Publish** your container

## How It Works

1. **On page load**: The template sets default consent state to "Denied" (or your configured defaults)
2. **Cookie check**: If a Cookiefy consent cookie exists, consent state is immediately updated
3. **Banner interaction**: When user accepts/denies, the banner calls a callback that updates consent
4. **Tag firing**: Tags fire according to their consent requirements

## Support

- **Documentation**: https://cookiefy.app/docs/gtm-integration
- **Email**: support@cookiefy.app
- **Website**: https://cookiefy.app

## License

This template is provided by Cookiefy under the [Google Tag Manager Community Template Gallery Developer Terms of Service](https://developers.google.com/tag-manager/gallery-tos).
