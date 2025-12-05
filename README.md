# Tesla (Teslamate) Plugin

A TRMNL plugin that displays your Tesla vehicle data from your self-hosted Teslamate installation.

## Overview

This plugin integrates with Teslamate, a self-hosted data logger for Tesla vehicles, to display your vehicle's information on your TRMNL device. It requires a local Teslamate deployment and a companion reporter service to send data to TRMNL.

## Features

- **Vehicle data display** - Shows information from your Tesla via Teslamate
- **Webhook-based updates** - Real-time data pushed from your Teslamate instance
- **Self-hosted privacy** - Your Tesla data stays on your own infrastructure

## Requirements

⚠️ **IMPORTANT:** This plugin requires additional setup beyond the standard TRMNL plugin installation.

### Prerequisites

1. **Teslamate Installation** - You must have Teslamate running locally
2. **Teslamate Reporter** - A companion service that sends data from Teslamate to TRMNL
3. **Network Access** - Your Teslamate instance needs to reach TRMNL's webhook endpoint

## Setup Instructions

### Step 1: Deploy Teslamate Reporter

This plugin depends on data reporting from your local Teslamate deployment. You need to deploy the Teslamate Reporter alongside your Teslamate installation.

**Reporter Repository:**
```
https://github.com/eden881/trmnl-teslamate-reporter
```

Visit the repository above for detailed installation and configuration instructions.

### Step 2: Configure the Plugin

Once the reporter is deployed and configured:

1. Add this plugin to your TRMNL device
2. The plugin will provide you with a webhook URL
3. Configure the Teslamate Reporter to send data to this webhook URL
4. Data will begin flowing to your TRMNL display

## Technical Details

- **Strategy:** Webhook
- **Refresh Interval:** 30 minutes
- **Screen Padding:** Yes
- **Dark Mode Support:** No

## How It Works

1. Teslamate collects data from your Tesla vehicle
2. The Teslamate Reporter service reads this data from Teslamate's database
3. The Reporter sends formatted data to TRMNL via webhook
4. Your TRMNL device displays the information

This webhook-based approach ensures your Tesla data remains on your own infrastructure while still enabling display on TRMNL.

## Settings

### Attention!
- **Type:** Copyable URL
- **Value:** `https://github.com/eden881/trmnl-teslamate-reporter`
- **Description:** This plugin depends on data reporting from your local Teslamate deployment. Head over to this URL to deploy the reporter alongside Teslamate!

## Layout Support

This plugin supports all TRMNL layout sizes:
- Full screen
- Half horizontal
- Half vertical
- Quadrant

## Privacy & Security

This plugin is designed with privacy in mind:
- Your Tesla data is logged by Teslamate on your own server
- Data is only sent to TRMNL when you configure the reporter
- No third-party services access your vehicle data
- You maintain full control over what data is shared

## Troubleshooting

**No data appearing?**
- Verify Teslamate is running and collecting data
- Check that the Teslamate Reporter is properly configured
- Ensure the webhook URL is correctly set in the Reporter
- Verify network connectivity between your server and TRMNL

**Data not updating?**
- Check the Reporter's logs for errors
- Verify the refresh interval settings
- Ensure your Teslamate database is being updated

## Resources

- **Teslamate:** [https://github.com/adriankumpf/teslamate](https://github.com/adriankumpf/teslamate)
- **Teslamate Reporter:** [https://github.com/eden881/trmnl-teslamate-reporter](https://github.com/eden881/trmnl-teslamate-reporter)
