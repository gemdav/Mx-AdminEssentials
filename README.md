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
2.  **Assign Module Roles:** Navigate to `App Security` -> `User Roles` and assign the appropriate module roles (e.g., `Administrator`, `AdminUser`) from this module to your project's user roles that require administrative access.
3.  **Integrate Admin UI (Snippet):**
    *   This module provides a comprehensive administrative UI within a single snippet: `SNPT_AdminEssentials_Configuration`.
    *   Create a dedicated administration page in your application (e.g., `MyAdministration_Overview`).
    *   **Drag and drop the `SNPT_AdminEssentials_Configuration` snippet** from the module's `USE_ME` folder onto your admin page. This snippet contains all the necessary tabs and interfaces for managing alerts, maintenance mode, user messaging, and user access reviews.

## Configuration

This module requires minimal explicit configuration beyond the setup of its own entities and pages.

*   **Initial Data:** Ensure initial configuration objects (e.g., for maintenance mode, default email templates) are created, either manually or via a startup process.
*   **Email Connector:** For the User Messaging feature to send actual emails (instead of just generating `.eml` files), you will need to integrate with an external email sending module or service (e.g., the Mendix Email Connector or a custom Java action). The module primarily focuses on `.eml` file generation for review.

## Usage

After installation and configuration, you can utilize the module's functionalities by integrating the provided elements from the `USE_ME` folder.

*   **Alerts:** Create and manage system-wide alerts using the integrated `SNPT_AdminEssentials_Configuration` snippet, and integrate their display into your application layouts.
*   **Maintenance Mode:** Configure and activate maintenance mode through the integrated `SNPT_AdminEssentials_Configuration` snippet.
*   **User Messaging:** Compose and generate emails via the integrated `SNPT_AdminEssentials_Configuration` snippet; the `.eml` file will automatically download upon generation.
*   **UAR Management:** Access the UAR overview and decision pages via the integrated `SNPT_AdminEssentials_Configuration` snippet to manage pending user access reviews.
    This module is designed to manage the local users of your app. Please be aware that MendixSSO users are provisioned by the MendixSSO module and should be managed from the App User Management screen (Developer Portal > General Settings > Manage App Users).

## Help Improving This Module

This module is designed to be a comprehensive administrative toolkit. If you have suggestions for new features, improvements to existing ones, or encounter any issues, please don't hesitate to provide feedback. Your contributions help make this module even more valuable for the Mendix community!