# Admin Essentials Module

## Overview

This module provides a centralized suite of tools for Mendix application administrators and developers. It consolidates essential administrative functionalities, including system-wide alerts, application maintenance management, user messaging, and user access review. Designed for ease of integration via the Mendix Marketplace, it aims to enhance application governance, operational efficiency, and user experience by offering plug-and-play solutions for common administrative tasks.

## Typical Usage Scenario

For Mendix developers and administrators seeking to streamline operational tasks and improve application governance, this module offers a ready-to-use solution. It allows for effective communication through system-wide alerts, controlled activation of maintenance modes, targeted user messaging, and efficient management of user access reviews, all from within the Mendix application.

## Features

*   **Dynamic Alert System:** Create and manage various types of alerts (banners, toasts) with customizable severity, content, and display options for effective system-wide communication.
*   **Maintenance Mode Control:** Easily activate and deactivate application-wide maintenance mode, providing clear communication to users while allowing technical staff continued access.
*   **User Messaging & Email Generation:** Compose and send targeted emails to users or user roles using customizable templates, with the ability to automatically generate and download `.eml` files for review.
*   **User Access Review (UAR) Management:** Streamline the process of reviewing and managing user access, allowing administrators to renew, revoke, or modify user roles with auditability.

## Installation

1.  **Download from Marketplace:** Install the "Admin Essentials Module" from the Mendix Marketplace into your app.
2.  **Assign Module Roles:** Navigate to `App Security` -> `User Roles` and assign the `Administrator` module role to the application level admin role and the `User` module role to all other app roles.
3.  **Make the admin UI snippet accessible:**
    *   This module provides a comprehensive administrative UI within a single snippet: `SNPT_AdminEssentials_Configuration`.
    *   Create a dedicated administration page in your application (e.g., `AdminEssentials_Config`) which can be reached by administrators.
    *   Drag and drop the `SNPT_AdminEssentials_Configuration` snippet from the module's `USE_ME` folder onto your admin page. This snippet contains all the necessary tabs and interfaces for managing alerts, maintenance mode, user messaging, and user access reviews.
4. **Integrate the functionality snippet:** For some of the functionalities to take effect (e.g. for alerts to be shown and the maintenance mode to be fired), the snippet `SNPT_AdminEssentials` has to be integrated into the app. It is recommended to add the snippet to the top of every non-popup layout that is used in the application.
5. **Customize alerts and maintenance page:** The different alert types and the maintenance page are fully customizable:
    *   To customize the alerts, replace the snippet call in `SNPT_CUSTOM_BannerAlert` or `SNPT_CUSTOM_ToastAlert` in the `USE_ME` folder with the desired content. 
    *   To customize the maintenance page, replace the snippet call in `SNPT_CUSTOM_MaintenancePage` in the `USE_ME` folder with the desired content.

    Note that it is recommended to keep the custom content in a non-marketplace module (e.g. you Main module) to prevent it from being overwritten when the marketplace module is updated.

## Usage

After installation and configuration, you can utilize the module's functionalities by integrating the provided elements from the `USE_ME` folder.

*   **Alerts:** Create and manage system-wide alerts using the integrated `SNPT_AdminEssentials_Configuration` snippet, and integrate their display into your application layouts.
*   **Maintenance Mode:** Configure and activate maintenance mode through the integrated `SNPT_AdminEssentials_Configuration` snippet.
*   **User Messaging:** Compose and generate emails via the integrated `SNPT_AdminEssentials_Configuration` snippet; the `.eml` file will automatically download upon generation.
*   **UAR Management:** Access the UAR overview and decision pages via the integrated `SNPT_AdminEssentials_Configuration` snippet to manage pending user access reviews.
    This module is designed to manage the local users of your app. Please be aware that MendixSSO users are provisioned by the MendixSSO module and should be managed from the App User Management screen (Developer Portal > General Settings > Manage App Users).

## Help Improving This Module

This module is designed to be a comprehensive administrative toolkit. If you have suggestions for new features, improvements to existing ones, or encounter any issues, please don't hesitate to provide feedback. Your contributions help make this module even more valuable for the Mendix community!