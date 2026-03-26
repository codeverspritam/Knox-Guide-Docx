# Knox Manage Guide: Dashboard

The **Dashboard** is the first screen you see after logging in. It serves as your "Control Tower," providing a real-time visual summary of your entire device fleet's health, security, and license status.

---

### 1. What it is

The Dashboard is an interactive graphical interface that aggregates data from all enrolled devices. It uses charts (pie charts, bar graphs, and lists) to show which devices are online, which are violating security policies, and how many licenses are remaining.

### 2. Why we use it

- **Instant Visibility:** Instead of checking 100 devices one by one, you see a summary in 5 seconds.
- **Security Monitoring:** Quickly identify "Compromised" (rooted) devices or those with "Policy Violations."
- **License Management:** Track your 90-day trial or commercial license expiration to prevent service interruption.
- **Connectivity Tracking:** See which devices have not connected to the internet (synced) recently.

### 3. Step-by-Step: How to Use it

1.  **Log in** to the [Knox Manage Console](https://www.samsungknox.com).
2.  On the left-hand sidebar, click **Dashboard**.
3.  **Filter Data:** Use the "Organization" or "Group" dropdown at the top to see data for specific teams.
4.  **Interactive Click:** Click on any colored segment of a pie chart (e.g., the red "Non-Compliant" slice).
5.  **View Details:** The console will automatically jump to the **Device List**, filtered to show only those specific devices for immediate action.

### 4. What happens on the Device

The Dashboard itself is a **read-only** tool for the Admin.

- **No immediate change:** Simply viewing the Dashboard does not change anything on the user's phone.
- **Reporting:** The phone periodically sends "Heartbeat" data (battery level, OS version, location) back to the console to populate these charts.

### 5. How to "Stop" or Reset

Since the Dashboard is a reporting tool, you don't "stop" it, but you can customize what it shows:

- **Reset Filters:** Click the **Reset** button or the "Home" icon at the top to return to the default view.
- **Refresh Data:** Click the **Refresh** icon to pull the most recent data from the servers.
- **Fix Red Status:** To "clear" a red error on the Dashboard, you must go to the **Device List**, find the failing device, and fix the issue (e.g., update the OS or re-sync the policy).

---

<!-- **Which option from your list is next?** (e.g., Device, Profile, Application, etc.) -->

# Knox Manage Guide: Device

The **Device** menu is your primary control center. This is where you see every individual phone or tablet enrolled in your system and where you send "Remote Commands" (like locking or wiping) to specific users.

---

### 1. What it is

The **Device** section (specifically **All Devices**) is a real-time list of every piece of hardware under your management. It shows the device name, model, phone number, battery level, and most importantly, its **Connection Status** (online or offline).

### 2. Why we use it

- **Individual Control:** Unlike "Profiles" which affect groups, the Device menu lets you target **one specific phone**.
- **Troubleshooting:** See exactly when a device last "checked in" to the server.
- **Emergency Action:** If a phone is lost or stolen, this is where you go to **Lock** or **Wipe** it immediately.
- **Device Info:** Check technical details like IMEI, Serial Number, OS version, and Storage space.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Device** > **All Devices**.
2.  **Search:** Use the search bar at the top to find a device by **User Name**, **Serial Number**, or **Phone Number**.
3.  **Select:** Click the checkbox next to the device name.
4.  **Execute Command:** Click the **Device Management** button (top bar) to see the action menu:
    - **Lock:** Freezes the phone screen.
    - **Wipe:** Factory resets the device (deletes everything).
    - **Sync:** Forces the phone to download the latest settings.
    - **Change License:** Move the device from a Trial to a Commercial license.

### 4. What happens on the Device

- **Real-time Response:** If the device is connected to Wi-Fi or Data, it will react to your command in **seconds**.
- **Lock Command:** The user’s screen will turn off and show a "Device Locked by Admin" message. They cannot bypass this.
- **Wipe Command:** The phone will immediately reboot and begin erasing all photos, apps, and settings.
- **Sync Command:** A small "Knox Manage" icon may appear briefly in the notification bar while it updates.

### 5. How to Stop

- **Unlocking:** If you locked a device, select it again in the list and click **Unlock**. You may need to provide the "Unlock PIN" shown in the console.
- **Stopping a Wipe:** **WARNING:** Once a "Wipe" command is sent and the device receives it, it **cannot be stopped**. It will be factory reset.
- **Removing Management:** To stop managing a device entirely, select it and click **Unenroll** or **Delete**. This removes the Knox agent and all corporate restrictions.

---

<!-- **Next option on your list?** (e.g., User, Organization, Profile, or Application?) -->

# Knox Manage Guide: User

The **User** menu is where you manage the "People" behind the devices. While the **Device** menu focuses on hardware (IMEI, Serial Number), the **User** menu focuses on identity (Name, Email, Department).

---

### 1. What it is

The **User** section is a database of all employees or technicians who are authorized to use managed devices. It links a specific person to a specific phone. This is where you store login credentials and contact information.

### 2. Why we use it

- **Accountability:** You can see exactly which person is holding which device.
- **Group Management:** You can assign users to "Organizations" (e.g., Sales, HR, IT) to apply different rules to different departments automatically.
- **Authentication:** This is where you set the username and password that the employee must enter when they first set up their phone.
- **Bulk Enrollment:** If you have 500 employees, you use this menu to "Import" them all from an Excel file instead of typing names one by one.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **User** > **All Users**.
2.  **Add a User:** Click the **Add** button at the top.
    - **User ID:** Usually their work email (this is what they use to log in).
    - **Password:** Set a temporary password for them to use during setup.
    - **Organization:** Assign them to a department (e.g., "Marketing").
3.  **Invite User:** Select a user and click **Send Invitation**. They will receive an email or SMS with instructions on how to enroll their device.
4.  **Modify User:** Click on a user's name to change their password or update their phone number.

### 4. What happens on the Device

- **Setup Screen:** When the user turns on a new phone, they will see a Knox login screen. They must enter the **User ID** and **Password** you created here.
- **Automatic Profile:** Once they log in, Knox Manage looks at which "Organization" the user belongs to and automatically downloads the correct Apps, Wallpaper, and Restrictions for them.
- **Personalization:** If you configured it, the device might display the user's name on the lock screen.

### 5. How to Stop

- **Deactivate User:** If an employee leaves the company, select the user and click **Modify** > **Status** > **Inactivate**. This stops them from enrolling any new devices.
- **Delete User:** If you delete a user, any device currently linked to them will lose its "Owner" status.
  - _Note:_ Deleting a user **does not** automatically wipe the device; you must send a **Wipe** command from the **Device** menu first if you want the data gone.
- **Unlink Device:** If a user gets a new phone, you can "Unassign" their old device in their user profile so the old phone can be given to someone else.

---

<!-- **Ready for the next one?** (e.g., Organization, Profile, or Application?) -->

# Knox Manage Guide: Deactivate User

The **Deactivate User** function is a security measure used to temporarily suspend a person's access to the management system without deleting their data or history from your records.

---

### 1. What it is

Deactivating a user changes their status from **Active** to **Inactive**. This acts as a "Pause" button for that person's account within the Knox Manage console. It prevents that specific identity from enrolling new devices or logging into the Knox self-service portal.

### 2. Why we use it

- **Employee Leave:** If an employee is on a long leave (medical, maternity, or sabbatical), you deactivate them so their account cannot be used while they are away.
- **Suspicion of Breach:** If you suspect a user's credentials have been stolen, deactivating the user immediately stops any further enrollment attempts.
- **Offboarding Process:** When an employee leaves the company, you deactivate them first to ensure they can no longer access corporate resources before you eventually delete the account.
- **Device Recovery:** If a device is lost, deactivating the user ensures they can't try to "re-enroll" a different device using those same stolen credentials.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **User** > **All Users**.
2.  Find the specific user in the list (you can use the **Search** bar).
3.  Click on the **User ID** (the blue link) to open their profile.
4.  Look for the **Status** field. Click the dropdown menu and change it from **Active** to **Inactive**.
5.  Click **Save** at the bottom of the page.
6.  _Alternative:_ Select the checkbox next to the user in the "All Users" list and look for a **Modify Status** button in the top action bar (if available in your version).

### 4. What happens on the Device

- **Enrollment Blocked:** If the user tries to set up a new phone using their User ID and Password, the device will show an error: _"Unauthorized User"_ or _"Account Disabled."_
- **Existing Devices:** Deactivating a user **does not** automatically wipe a device they already have. The phone will remain managed under the last applied policy, but the user cannot perform "Self-Service" actions (like remote locating their own phone).
- **Syncing:** The device will still show as "Managed" in your console, but it is now linked to an "Inactive" identity.

### 5. How to Stop (Reactivate)

- **Reverse the Process:** To allow the user back into the system, go back to **User** > **All Users**.
- **Filter for Inactive:** If you can't find them, click the **Filter** icon and ensure "Inactive" users are being shown.
- **Change Status:** Click the user's name, change the **Status** back to **Active**, and click **Save**.
- **Immediate Effect:** The user can now immediately begin enrolling devices or logging into the corporate portal again.

---

<!-- **Which specific option name is next on your list?** (e.g., Organization, Profile, or Group?) -->

# Knox Manage Guide: Group

The **Group** menu is your primary tool for **mass management**. While a "User" is one person, a "Group" is a collection of users or devices that all need the exact same apps, restrictions, and settings.

---

### 1. What it is

A **Group** is a logical container used to categorize users or devices. Think of it like a folder. Instead of sending an app to 100 individual users, you put those 100 users into a "Sales Group" and send the app to the group once.

### 2. Why we use it

- **Efficiency:** It saves hours of work. One click updates every device in the group.
- **Role-Based Access:** You can create different groups for different job roles (e.g., "Drivers" get GPS apps, "Office Staff" get Outlook).
- **Automation:** When you add a new user to a group, they **automatically** receive all the apps and policies already assigned to that group.
- **Filtering:** It helps you organize your **Device List** so you can quickly see only the "Warehouse Tablets" or "Manager Phones."

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **User** > **Group**.
2.  **Create a Group:** Click the **Add** button at the top.
    - **Group Name:** Enter a clear name (e.g., _Delivery_Team_Alpha_).
    - **Description:** (Optional) Add a note about who is in this group.
    - **Parent Group:** Choose if this is a sub-group of another department.
3.  **Add Members:**
    - Go to **User** > **All Users**.
    - Select the checkboxes for the users you want.
    - Click **Change Group** at the top and select your new group.
4.  **Assign Policies:** Go to **Profile** or **Application**, select your item, and click **Assign**. Choose your **Group** from the list.

### 4. What happens on the Device

- **Instant Update:** As soon as a device is moved into a group, Knox Manage checks what that group is supposed to have.
- **App Pushes:** The device will immediately start downloading any apps assigned to that group.
- **Policy Changes:** If the group has a "No Camera" policy, the camera icon will disappear from the phone within seconds of the device joining the group.
- **Wallpaper Change:** If the group has a specific branded wallpaper, the device screen will update automatically.

### 5. How to Stop (Remove from Group)

- **Move User:** Go to **User** > **All Users**, select the person, click **Change Group**, and move them to a "Default" or "Null" group.
- **Delete Group:** If you delete a group, all users inside it become "Unassigned."
  - _Warning:_ When you remove a user from a group, any apps or policies that were **only** assigned to that group may be **automatically uninstalled** from the phone.
- **Check Assignments:** To stop a group from having a specific app, go to **Application** > **App Library**, select the app, and **Unassign** it from that specific group.

---

<!-- **What is the next option name on your list?** (e.g., Organization, Profile, or Application?) -->

# Knox Manage Guide: Organization

The **Organization** menu is the highest level of your structural hierarchy. While a **Group** is for smaller teams (like "Sales" or "Drivers"), the **Organization** represents your entire company or its major branches.

---

### 1. What it is

The **Organization** (often called "Org Unit") is the "Tree Structure" of your Knox Manage console. It is a hierarchical folder system used to partition your company. For example, your top-level Organization might be "Global Corp," with sub-levels like "India Office" and "UK Office."

### 2. Why we use it

- **Top-Down Management:** It allows you to set a "Global Policy" at the top level that every single device in the company must follow.
- **Admin Permissions:** You can assign "Sub-Admins" who can only see and manage devices in the "India Office" organization, but not the "UK Office."
- **Separation of Data:** If you manage multiple clients or completely different business units, an Organization keeps their users, devices, and apps totally separate.
- **Branding:** You can set different company logos or contact information for different branches of your business.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **User** > **Organization**.
2.  **Create an Organization:** Click the **Add** button at the top.
    - **Organization Name:** Enter your company or branch name (e.g., _Mumbai_Branch_).
    - **Parent Organization:** Select where this fits in the tree (e.g., under _Global_HQ_).
3.  **Assign Users:**
    - Go to **User** > **All Users**.
    - Select a user and click **Modify**.
    - Change their **Organization** field to your new branch.
4.  **Set Policy:** Go to **Profile**, select a profile, and click **Assign**. Choose the **Organization** tab to apply that policy to everyone in that branch at once.

### 4. What happens on the Device

- **Profile Application:** The device will look at its assigned Organization to decide which "Profile" (restrictions/wallpaper) to download.
- **Contact Info:** If you have set "Support Information" (phone/email) for that Organization, it will appear in the Knox Manage app on the user's phone.
- **Inheritance:** If you change a setting at the "Global HQ" level, it "trickles down" to the "Mumbai Branch" automatically unless you have set a specific local rule.

### 5. How to Stop (Modify or Delete)

- **Move Users/Groups:** Before deleting an Organization, you must move all users and groups inside it to a different branch.
- **Delete Organization:** Select the branch in the **Organization** menu and click **Delete**.
  - _Note:_ You cannot delete the "Root" (top-level) organization you created when you first set up the account.
- **Change Parent:** You can click **Modify** to move a branch (e.g., move "Sales" from "New York" to "New Jersey"). The devices will instantly update to the new location's rules.

---

<!-- **What is the next option name on your list?** (e.g., Profile, Application, or Settings?) -->

# Knox Manage Guide: Difference Between Group and Organization

While both **Groups** and **Organizations** are used to categorize your assets, they serve different purposes in your hierarchy. Understanding the difference is key to avoiding "Policy Conflicts."

---

### 1. What they are

- **Organization (The "Tree"):** This is your company's structural skeleton. It is a hierarchical folder system (Top-level > Sub-level) used to partition the entire company by branch, region, or department.
- **Group (The "Tags"):** A group is a collection of users or devices. Unlike Organizations, which are built like a tree, Groups are more like "labels" you put on people or hardware to give them specific things.

### 2. Key Differences at a Glance

| Feature         | Organization                                         | Group                                                  |
| :-------------- | :--------------------------------------------------- | :----------------------------------------------------- |
| **Structure**   | Hierarchical (Sub-orgs inherit from parents).        | Static or Dynamic list (Flat structure).               |
| **Primary Use** | Administrative delegation and company structure.     | Assigning specific Apps and Profiles.                  |
| **Inheritance** | Sub-orgs inherit policies from the "Super Org".      | No inheritance; settings are specific to the group.    |
| **Membership**  | A user/device usually belongs to **one** Org branch. | A user/device can belong to **many** different groups. |

### 3. Use Cases (Why we use which)

- **Use Organization when:** You want to divide your console so a "Manager in Mumbai" can only see devices in the "Mumbai Branch" but not the "Delhi Branch".
- **Use Group when:** You have 10 people across _different_ departments who all need a specific "Video Editing App." You put them in a "Video Team" Group to push the app to them.

### 4. What happens on the Device (Priority)

This is the most important part of the guide: **Group policies always beat Organization policies**.

- **Example:** If your **Organization** policy _allows_ the camera, but your **Group** policy _disables_ the camera, the phone will **disable** the camera.
- **Result:** The device follows the most "specific" rule (the Group) over the "general" rule (the Organization).

### 5. How to Stop Conflict

If a device is acting weird because of these two settings:

1.  Check the **Device Details** in the console to see which Profiles are assigned to it.
2.  If you want the Organization rule to win, you must **Unassign** the conflicting profile from the **Group**.
3.  Click **Sync** on the device to refresh the settings.

---

<!-- **Which specific option name is next on your list?** (e.g., Profile, Application, or Settings?) -->

# Knox Manage Guide: Application

The **Application** menu is where you manage the lifecycle of software on your devices. This is where you decide which apps are allowed, how they are installed, and how they are configured for your users.

---

### 1. What it is

The **Application** section (specifically the **App Library**) is a centralized repository of all software you intend to deploy. It supports multiple sources, including the **Managed Google Play Store**, private **In-house APKs**, and even web links. It is the "Warehouse" from which you distribute tools to your fleet.

### 2. Why we use it

- **Controlled Distribution:** Ensures employees only use company-approved apps.
- **Silent Installation:** You can install apps in the background so the user doesn't have to click anything.
- **Remote Configuration (AppConfig):** You can pre-set settings inside an app (like a server URL or email domain) so the user doesn't have to type them manually.
- **Security:** You can "Whitelist" only safe apps and "Blacklist" dangerous ones to prevent data leaks.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Application** > **App Library**.
2.  **Add an App:** Click the **Add** button.
    - **Public (Play Store):** Search the Play Store and select the app.
    - **Internal (In-house):** Upload your own `.apk` or `.ipa` file.
3.  **Set Configuration:** Once added, click on the app name and look for **Managed Configuration** (if supported by the developer). Enter your custom settings here.
4.  **Assign to Users:**
    - Select the app and click **Assign**.
    - Choose your **Target** (Organization or Group).
    - **Crucial Step:** Select the **Installation Type**:
      - _Auto-installed (can't be removed):_ Forces the app onto the phone silently.
      - _Installed by User:_ Places the app in a "Work Play Store" for the user to download if they want it.

### 4. What happens on the Device

- **Automatic Pop-up:** If set to "Auto-installed," the app icon will suddenly appear on the phone's home screen or in the "Work Profile" folder.
- **No Setup Required:** If you used **Managed Configuration**, the user opens the app and finds it is already logged in or configured with the correct company settings.
- **Blocked Apps:** If a user tries to download a "Blacklisted" app from their personal store, the phone will block the installation or the Knox agent will immediately uninstall it.

### 5. How to Stop

- **Unassigning:** To remove an app from a group, select the app in the **App Library**, click on the **Assigned Group**, and select **Unassign**.
- **Uninstallation Policy:** When unassigning, you will be asked if you want to **"Uninstall the app from the device."** Select **Yes** to remotely delete the app from all phones in that group.
- **Deleting from Library:** If you delete an app from the **App Library** entirely, it will be removed from your console, but it may stay on devices unless you explicitly chose the "Uninstall" option during the deletion process.

---

<!-- **What is the next option name on your list?** (e.g., Profile, Content, or Kiosk?) -->

# Knox Manage Guide: Profile

The **Profile** menu is the "Brain" of your management system. While the **User** or **Group** identifies _who_ gets the settings, the **Profile** defines exactly _what_ those settings and restrictions are.

---

### 1. What it is

A **Profile** is a collection of security policies, device restrictions, and connectivity settings bundled into a single file. Think of it as a "Rule Book." You create different rule books for different needs (e.g., a "Strict Profile" for factory workers and a "Flexible Profile" for office managers).

### 2. Why we use it

- **Security Enforcement:** This is where you disable the **Camera**, **Bluetooth**, or **Factory Reset** to protect company data.
- **Automation:** Instead of manually setting 50 options on every phone, you apply one Profile, and all 50 settings activate instantly.
- **Standardization:** Ensures every device in a specific department looks and behaves exactly the same way.
- **Compliance:** You use Profiles to force users to set a **Strong Password** (PIN/Pattern) so the phone cannot be easily broken into if lost.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Profile**.
2.  **Create a Profile:** Click the **Add** button.
    - **Profile Name:** Give it a clear name (e.g., _Warehouse_Security_Policy_).
    - **Platform:** Select **Android** (or iOS/Windows).
    - **Management Type:** Usually **Android Enterprise** (for modern devices).
3.  **Modify Policy:** Click the **Modify Policy** button inside your new profile.
    - Navigate the tree on the left (e.g., **Device Restriction** > **Allow Camera**).
    - Change the setting to **Disallow**.
4.  **Save & Apply:** Click **Save** at the bottom.
5.  **Assign:** Select the profile from the list and click **Assign**. Choose the **Organization** or **Group** that should follow these rules.

### 4. What happens on the Device

- **Instant Lockdown:** Within seconds of assigning the profile, the phone will vibrate or show a "Security policy updated" notification.
- **Feature Disappearance:** If you disabled the **Camera**, the Camera icon will literally vanish from the home screen.
- **Settings Greyed Out:** If the user tries to go into the phone's manual settings to change something you've restricted (like Wi-Fi), the option will be **greyed out** and say: _"Disabled by your Administrator."_

### 5. How to Stop (Modify or Remove)

- **Change a Rule:** To "Undo" a restriction, go back to **Profile** > **Modify Policy**, change the setting (e.g., set Camera back to **Allow**), and click **Save & Assign**. The phone will update instantly.
- **Unassign Profile:** If you want to remove all rules from a group, select the profile and click **Unassign**.
  - _Note:_ The device will usually revert to its "Default" state (Camera returns, restrictions lift) unless another profile is still active.
- **Delete Profile:** You can only delete a profile if it is **not assigned** to any devices or groups. You must unassign it first.

---

<!-- **What is the next option name on your list?** (e.g., Kiosk, Content, or Event?) -->

# Knox Manage: Profile Policy Categories Guide

When you click **Modify Policy** within a Profile, you will see several categories on the left. Here is a breakdown of the most important options, why they are used, and their impact on the device.

---

## 1. Device Restriction

Controls the hardware and core system features of the device.

- **Why we use it:** To prevent unauthorized use of the camera, screenshots, or hardware buttons for security or focus.
- **Key Settings:**
  - **Allow Camera:** Enable/Disable the camera.
  - **Allow Screen Capture:** Prevent users from taking screenshots.
  - **Allow Factory Reset:** Blocks the user from wiping the device to remove management.
- **On the Device:** Restricted icons (like Camera) disappear. Blocked settings in the phone's menu will be greyed out.
- **To Stop:** Change the setting back to **Allow** and click **Save & Assign**.

---

## 2. Connectivity

Manages how the device connects to the internet and other hardware.

- **Why we use it:** To save data costs, prevent data leaks via USB, or force devices to stay on a secure corporate Wi-Fi.
- **Key Settings:**
  - **Wi-Fi SSID Allowlist:** Only allow the phone to connect to specific office Wi-Fi names.
  - **USB Data Transfer:** Set to **Disallow** so files cannot be copied to a PC.
  - **Bluetooth Control:** Restrict which Bluetooth devices (like only headsets) can connect.
- **On the Device:** Users will be unable to toggle Wi-Fi/Bluetooth off or connect to unauthorized networks.
- **To Stop:** Set the restriction to **Not Apply** or **Allow**.

---

## 3. Security

Enforces protection for the device's data and OS integrity.

- **Why we use it:** To ensure the device is encrypted and has a strong lock screen.
- **Key Settings:**
  - **Take Action if OS is Compromised:** Automatically **Lock** or **Wipe** the device if it is rooted.
  - **Factory Reset Protection (FRP):** Ensures only your admin email can unlock the phone after a reset.
  - **Storage Encryption:** Forces the phone to encrypt its internal memory.
- **On the Device:** If the OS is tampered with, the phone immediately bricks or erases itself to protect data.
- **To Stop:** Revert the compliance action to **Admin Alert** (Only notifies you instead of locking).

---

## 4. Kiosk Mode

Locks the device into a dedicated purpose (e.g., a digital sign or a warehouse scanner).

- **Why we use it:** To turn a standard phone into a "single-purpose" tool.
- **Key Settings:**
  - **Kiosk App Settings:** Choose **Single App Mode** (locks into one app) or **Multi-App Mode** (locks into a custom home screen).
  - **System Bar:** Choose to hide the top notification bar and bottom navigation buttons.
- **On the Device:** The phone becomes a "Kiosk." The user cannot exit the app or see the standard home screen.
- **To Stop:** Set the Kiosk mode to **Disallow** or **Unassign** the profile from the device.

---

## 5. System Update (E-FOTA)

Controls when and how the Android Operating System updates.

- **Why we use it:** To prevent devices from updating during critical work hours or to ensure all phones stay on a stable OS version.
- **Key Settings:**
  - **Update Policy:** Choose **Automatic**, **Postpone** (up to 30 days), or **Windowed** (e.g., only 2 AM - 4 AM).
  - **Freeze Period:** Set a period of up to 90 days where no updates occur.
- **On the Device:** The user will not see "Update Available" prompts; the phone will simply update silently during the window you set.
- **To Stop:** Set the policy to **Automatic** to allow standard Google updates.

---

## 6. Wallpaper & Display

Customizes the look of the device for corporate branding.

- **Why we use it:** To make company-owned devices easily identifiable and professional.
- **Key Settings:**
  - **Wallpaper:** Upload a custom image for the Home and/or Lock screen.
  - **Brightness:** Set a fixed brightness level to save battery.
- **On the Device:** The background image changes automatically. The user is usually blocked from changing it back to a personal photo.
- **To Stop:** Set the Wallpaper policy to **Disallow** (this removes the restriction) or upload a different image.

# Knox Manage Guide: Advanced Profile Policy Sections

This guide covers the remaining specialized categories within **Profile** > **Modify Policy**. These sections allow for deep customization of network traffic, runtime behavior, and automated triggers.

---

## 1. KSP (Knox Service Plugin)

The "Power User" section. KSP allows you to use the latest Samsung-specific features before they are officially added to the standard Android Enterprise menus.

- **Why we use it:** To access "Zero-Day" features like advanced camera blocking, specialized hardware button remapping (XCover key), and deep UI customization.
- **Step-by-Step:**
  1. Inside Profile, find **Samsung Knox** > **Knox Service Plugin**.
  2. Enable the **KSP policy**.
  3. Configure advanced settings like "Force Wi-Fi On" or "Disable Power Off button."
- **On the Device:** Enables features that standard Android profiles cannot touch, such as disabling the physical volume buttons or the power button.
- **To Stop:** Set the KSP configuration to **Not Apply**.

---

## 2. Browser (Web Content Filtering)

Controls what websites the user can visit specifically within the managed browser.

- **Why we use it:** To prevent users from visiting dangerous, non-work related, or high-data-usage websites (like YouTube or social media).
- **Key Settings:**
  - **Allowlist:** The user can _only_ visit the sites you list.
  - **Blocklist:** The user can visit anything _except_ the sites you list.
- **On the Device:** If a user tries to go to a blocked site, the browser shows a message: _"Access to this site is restricted by your administrator."_
- **To Stop:** Change the filtering mode to **Not Apply** or remove the URLs from the list.

---

## 3. Firewall (Network Filter)

A powerful tool to control which apps can talk to the internet and which IP addresses they can reach.

- **Why we use it:** To stop "background data" leaks or to ensure a specific app only communicates with your company's private server.
- **Key Settings:**
  - **App-based Rules:** Block "App A" from using Mobile Data but allow it on Wi-Fi.
  - **IP/Port Rules:** Block all traffic except to your specific office IP address.
- **On the Device:** The user sees no change, but apps will simply fail to load content if they aren't on the "Allowed" list.
- **To Stop:** Delete the Firewall rules or set the policy to **Not Apply**.

---

## 4. APN (Access Point Name)

Configures the cellular data settings for the SIM card.

- **Why we use it:** If your company uses a **Private APN** (for extra security or a private network), you must push these settings so the device can connect to the internet.
- **Key Settings:**
  - **APN Name, MMSC, Proxy, and Port.**
- **On the Device:** The phone automatically connects to the cellular network without the user manually typing technical codes into the "Mobile Networks" menu.
- **To Stop:** Remove the APN profile; the device will revert to the default carrier APN.

---

## 5. VPN (Virtual Private Network)

Forces the device to send its data through a secure "tunnel" to your office.

- **Why we use it:** To allow users to access internal company websites (like HR portals) securely from home or public Wi-Fi.
- **Key Settings:**
  - **Always-on VPN:** If the VPN drops, the internet stops working entirely until it reconnects.
  - **Per-App VPN:** Only "Work Apps" use the VPN; personal apps (like Spotify) use regular internet.
- **On the Device:** A key icon appears in the status bar. All data is encrypted and secure.
- **To Stop:** Unassign the VPN profile or toggle "Always-on" to **Off**.

---

## 6. Event Profile (Automated Triggers)

This is "If-This-Then-That" for Knox. It changes the device profile automatically based on a condition.

- **Why we use it:** To automate security. For example: "If the SIM card is removed, lock the device."
- **Key Triggers:**
  - **Geofencing:** Apply a "Strict Profile" when the user enters the office coordinates.
  - **Time:** Apply a "Work Profile" from 9 AM to 5 PM, and a "Personal Profile" after hours.
  - **SIM Change:** Wipe or Lock the device if a new SIM is detected.
- **On the Device:** The phone's behavior changes dynamically. At 5 PM, the Camera might suddenly reappear for personal use.
- **To Stop:** Delete the **Event Rule** or set the "Action" to **No Action**.

---

## 7. Certificate

Deploys digital "Keys" used for identity and encrypted Wi-Fi.

- **Why we use it:** So users can connect to "Hidden" or "Enterprise" Wi-Fi without ever knowing the password.
- **Key Settings:**
  - **Upload Root/Intermediate Certificates.**
- **On the Device:** Certificates are installed into the "System Credential Storage" silently.
- **To Stop:** Remove the certificate from the Profile; it will be deleted from the phone's memory.

---

<!-- **Which specific option name is next on your list?** (e.g., Content, Kiosk, or Settings?) -->

# Knox Manage Guide: Kiosk Mode

**Kiosk Mode** is one of the most powerful features in Knox Manage. It transforms a standard mobile device into a dedicated, single-purpose tool by locking it down to specific applications and restricting access to the rest of the system.

---

### 1. What it is

Kiosk Mode is a lockdown mechanism that restricts a device to a "safe zone." It replaces the standard Android home screen with a custom interface that only shows the apps you have authorized.

There are two primary types:

- **Single App Mode:** The device is locked into exactly one application. The user cannot exit this app or see any other part of the phone.
- **Multi App Mode:** The device shows a custom home screen with a specific selection of allowed apps (e.g., a scanner, a calculator, and a work portal).

### 2. Why we use it

- **Absolute Focus:** Ideal for Point-of-Sale (POS) terminals, digital signage, or warehouse scanners where users shouldn't be distracted by social media or games.
- **Enhanced Security:** By hiding the Settings, Play Store, and Notification bar, you prevent users from accidentally or intentionally changing critical system configurations.
- **Simplified Experience:** Users only see what they need to do their job, reducing training time and IT support calls.

### 3. Step-by-Step: How to Use it

There are two ways to set up a kiosk: using the **Kiosk Wizard** (recommended for beginners) or directly within a **Profile**.

**Using the Profile Method:**

1.  Navigate to **Profile** and click your active profile.
2.  Click **Modify Policy** in the footer.
3.  On the left menu, select **Kiosk** (under the Android Enterprise drawer).
4.  Set the **Kiosk App Settings** to either **Single App Mode** or **Multi App Mode**.
5.  Click **Add** to select the app(s) from your App Library that will be visible in the kiosk.
6.  (Optional) Configure **Utilities** (like a clock or Wi-Fi toggle) to appear on the kiosk screen.
7.  Click **Save & Assign** to push the lockdown to your devices.

### 4. What happens on the Device

- **Visual Transformation:** The phone immediately switches to the Kiosk Launcher. The standard home screen, app drawer, and recent apps button are disabled.
- **Total Restriction:** If a user tries to reboot the device, it will boot directly back into the Kiosk.
- **Locked Interface:** The status bar (notifications) and navigation buttons are typically hidden or frozen.

### 5. How to Stop (Exit Kiosk)

There are two main ways to remove a device from Kiosk mode:

- **Option A: Remote Command (Fastest)**
  1.  Go to **Device** > **All Devices**.
  2.  Select the device and click **Device Command**.
  3.  Select **Exit Kiosk Mode** and click **OK**. The phone will instantly return to its normal Android state.

- **Option B: Exit Kiosk Code (For Offline Devices)**
  1.  Go to the **Device Details** page in your console.
  2.  Find the **Exit Kiosk Code** (often under Security > Kiosk Mode Status).
  3.  On the phone, tap the screen repeatedly (or use the hidden "About Kiosk" menu) to bring up the password prompt.
  4.  Enter the code to unlock the device manually.

---

<!-- **Which option from your list is next?** (e.g., Remote Support, Event Profile, or License Management?) -->

# Knox Manage Guide: Remote Support

**Knox Remote Support** allows IT administrators to troubleshoot devices as if they were holding them in their own hands. It provides a real-time view of the device's screen and allows for direct remote control.

---

### 1. What it is

It is a secure, cloud-based tool consisting of a **Remote Viewer** (on the admin's PC) and a **Remote Support Agent** (an app on the device). It supports screen sharing, file transfer, and full interaction with device buttons and menus.

### 2. Why we use it

- **Faster Troubleshooting:** Admins can diagnose issues instantly without the user having to explain complex errors over the phone.
- **Reduced Downtime:** Fixes can be applied immediately from any location, eliminating the need for physical on-site visits.
- **Hands-on Assistance:** Ideal for helping users with complex configurations or installing specific software remotely.
- **Audit and Training:** Supports session recording (up to 10 minutes) and screen captures for documentation or training purposes.

### 3. Step-by-Step: How to Use it

1.  **Deploy the Agent:** Ensure the **Knox Remote Support Agent** app is installed on the target device via [Managed Google Play](https://docs.samsungknox.com/admin/knox-manage/faqs/faq-517-how-to-assign-remote-support-app-to-devices).
2.  **Navigate to Device:** In the left sidebar, go to **Device** > **All Devices**.
3.  **Initiate Session:** Select the target device and click the **Knox Remote Support** icon (or click **ACTIONS** > **Launch Knox Remote Support**).
4.  **Select Start Type:** Choose how to begin the session:
    - **Automatically Start:** Instantly connects without user input (Samsung Knox devices only).
    - **Ask to Start:** Sends a prompt to the user to "Accept" the session.
    - **Start with Code:** Generates a 6-digit code for the user to enter in their agent app.
5.  **Remote Control:** Once connected, use the [Remote Viewer](https://docs.samsungknox.com/admin/knox-remote-support/knox-remote-support-console/) to interact with the device.

### 4. What happens on the Device

- **Permission Prompt:** If not set to "Automatic," the user must tap **Accept** to allow the admin to see their screen.
- **Visual Indicator:** A notification or overlay usually appears on the device to alert the user that a remote session is active.
- **Interactive Control:** The user will see their screen moving and buttons being pressed as the admin performs troubleshooting.

### 5. How to Stop

- **Admin Side:** Click the **Disconnect** or **Stop** button in the [Knox Remote Support viewer](https://docs.samsungknox.com/admin/knox-remote-support/knox-remote-support-console/) on your PC.
- **User Side:** The user can tap the **Stop** button within the Remote Support agent app on their phone at any time to immediately end the session.
- **Timeout:** By default, sessions have a **30-minute time limit**, after which they will automatically disconnect unless the admin extends the timer.

---

<!-- **What is the next option name on your list?** (e.g., Event Profile, License Management, or Content?) -->

# Knox Manage Guide: Event Profile

The **Event Profile** is the automation engine of Knox Manage. It allows the device to change its settings automatically based on real-world triggers, such as entering a specific location, a specific time of day, or a security breach.

---

### 1. What it is

An Event Profile is an **"If-This-Then-That" (IFTTT)** rule. It consists of a **Trigger** (the event) and an **Action** (the profile change). Instead of an admin manually changing settings, the device "realizes" something has happened and updates itself.

### 2. Why we use it

- **Contextual Security:** Apply a "Strict" profile (no camera, no social media) when a user enters a high-security office building (**Geofencing**).
- **Work-Life Balance:** Automatically switch to a "Personal" profile (allowing YouTube/Games) after 6:00 PM and switch back to "Work" at 9:00 AM (**Time-fencing**).
- **Theft Protection:** If a thief removes the company SIM card, the device can automatically **Lock** or **Wipe** itself instantly.
- **Battery Management:** If the battery drops below 10%, automatically dim the screen and disable Bluetooth to save power.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Profile** > **Event Profile**.
2.  **Create Event:** Click the **Add** button.
3.  **Define the Condition (The "If"):**
    - **Geofencing:** Define a location on a map.
    - **Time:** Set a start and end time/day.
    - **Connectivity:** Trigger when Wi-Fi is disconnected or SIM is changed.
4.  **Define the Action (The "Then"):**
    - Select **Apply Profile** and choose which profile should activate.
    - _Example:_ When "In Office Geofence" -> Apply "No Camera Profile."
5.  **Assign:** Select the Event and click **Assign** to your specific **Group** or **Organization**.

### 4. What happens on the Device

- **Automatic Transition:** The user does nothing. As they drive into the office parking lot, the phone detects the GPS coordinates and "poof"—the Camera icon disappears.
- **Notifications:** You can configure a message to pop up on the screen: _"Entering Work Zone: Camera Disabled."_
- **Instant Response:** If a SIM card is pulled out, the phone locks within 1–2 seconds, showing a custom "Stolen Device" message.

### 5. How to Stop

- **Exit Condition:** Most events have an "Exit" rule. For example, when the user leaves the Geofence, the device automatically reverts to the previous "Standard" profile.
- **Deactivate Event:** In the **Event Profile** menu, select the event and click **Modify**. Change the status to **Inactivate**.
- **Unassign:** Select the event and click **Unassign** from the group. The devices will immediately stop listening for those triggers and stay on their current permanent profile.

---

<!-- **What is the next option name on your list?** (e.g., Content, License Management, or Messaging?) -->

# Knox Manage Guide: License Management

**License Management** is the engine that keeps your management server running. Without a valid license, your devices will stop receiving updates and you will lose the ability to send remote commands.

---

### 1. What it is

The **License** section is where you input, track, and renew your authorization to use Samsung Knox services. It acts as the "subscription manager" for your console.

There are two main types:

- **Trial License:** Valid for 90 days for testing up to 30 devices.
- **Commercial License:** A paid key purchased from a Samsung reseller, usually valid for 1 or 2 years.

### 2. Why we use it

- **Service Continuity:** To ensure your devices stay managed without interruption.
- **Cost Control:** To see exactly how many seats (devices) you have paid for and how many are still available for new employees.
- **Upgrade Path:** To move a device from a "Testing" phase (Trial) to a "Production" phase (Commercial) without having to factory reset the phone.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Setting** > **License**.
2.  **Add a License:** Click the **Add** button.
    - Enter the **License Key** provided by Samsung or your reseller.
    - Click **Save**.
3.  **Assign/Change License:**
    - Go to **Device** > **All Devices**.
    - Select the checkbox for the device(s) you want to update.
    - Click the **Device Management** (or Change License) button.
    - Select the new Commercial License from the dropdown and click **OK**.
4.  **Monitor Expiration:** Regularly check the **Expiration Date** column in the License menu to avoid "Red Status" alerts.

### 4. What happens on the Device

- **Background Sync:** The device itself doesn't show a "License" app. It simply receives a silent update from the server confirming it is still "Authorized."
- **No Interruption:** If you replace a trial license with a commercial one correctly, the user will notice **nothing**—their apps and settings stay exactly as they were.
- **Expiration Warning:** If a license expires, the Knox Manage agent on the phone may show a notification: _"License Expired. Please contact your administrator."_

### 5. How to Stop

- **License Expiration:** If you stop paying or let the trial expire, the console will enter **Read-Only** mode. You can see your devices, but you **cannot** change settings or wipe them.
- **Delete License:** You can delete a license from the console _only_ if it is not currently assigned to any devices. You must move the devices to a different license first.
- **Grace Period:** Knox Manage often provides a **30-day grace period** after a license expires before the management features completely shut down.

---

<!-- **What is the next option name on your list?** (e.g., Messaging, Support, or Android Enterprise setup?) -->

# Knox Manage Guide: Content

The **Content** menu is your secure "Company Drive." It is used to distribute important files (PDFs, videos, or images) directly to employee devices without using external email or public cloud storage.

---

### 1. What it is

The Content section is a secure document repository. It allows an administrator to upload files to the Knox Manage server and "push" them into a protected folder within the Knox Manage app on the user's phone.

### 2. Why we use it

- **Secure File Sharing:** Distribute sensitive documents (Price lists, Training manuals, Safety protocols) that should not be sent via WhatsApp or personal email.
- **No Personal Account Required:** Users don't need a Google Drive or Dropbox account to receive work files.
- **Auto-Update:** When you upload a "Version 2" of a manual in the console, it automatically replaces "Version 1" on every employee's phone.
- **Offline Viewing:** Users can download the files once while on Wi-Fi and view them later without using mobile data.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Content** > **Content Management**.
2.  **Upload File:** Click the **Add** button.
    - Select the file from your PC (PDF, MP4, JPG, etc.).
    - **Content Name:** Give it a clear title (e.g., _Employee_Handbook_2024_).
3.  **Set Policy:**
    - Decide if the user can **Download** the file or only **View** it online.
    - Decide if the file should **Expire** on a certain date.
4.  **Assign:** Select the file and click **Assign**.
    - Choose the **Organization** or **Group** that needs the file.
5.  **Distribute:** Click the **Distribute** button to send the file to the devices.

### 4. What happens on the Device

- **Notification:** The user may receive a notification: _"New content has been arrived."_
- **Access:** The user opens the **Knox Manage app** on their phone and taps the **Content** tab at the bottom.
- **Viewing:** They will see the list of files. They can tap to open and read them using the built-in secure viewer.

### 5. How to Stop

- **Remove Access:** Go to **Content Management**, select the file, and click **Unassign**. Select the group to remove.
- **Delete File:** If you delete the file from the console, it will be **automatically deleted** from the users' phones the next time they connect to the internet.
- **Stop Distribution:** You can "Pause" a file by clicking **Modify** and changing the status to **Inactive**. The file will stay in your library but disappear from the users' phones.

---

<!-- **What is the next specific option name on your list?** (e.g., Messaging, Setting, or Support?) -->

# Knox Manage Guide: Device Enrollment

**Device Enrollment** is the critical process of connecting a physical phone or tablet to your Knox Manage server. It is the "Handshake" that brings a device under your professional control.

---

### 1. What it is

Enrollment is the initial setup phase where a device downloads the **Knox Manage Agent** and registers its unique identity (IMEI/Serial Number) to your console. Once enrolled, the device is "Managed" and will follow your profiles and rules.

### 2. Why we use it

- **Establish Management:** You cannot send commands (Lock/Wipe) or push apps until a device is enrolled.
- **Ownership Confirmation:** It proves the device belongs to the company, allowing you to enforce "Android Enterprise" security.
- **Automated Setup:** Enrollment triggers the automatic download of all your pre-set Wallpapers, Apps, and Wi-Fi settings so the user doesn't have to do it manually.

### 3. Step-by-Step: How to Use it

There are several ways to enroll, but the **QR Code** method is the most common for manual setup:

1.  **Generate QR Code:**
    - In the sidebar, go to **Enrollment** > **Android Enterprise**.
    - Select your **Organization** and **Group**.
    - Click **Save** or **Generate QR Code**.
2.  **Prepare the Device:**
    - Start with a **Factory Reset** (New) device on the "Welcome" screen.
    - Tap the "Welcome" text **6 times** in the same spot. This opens a hidden QR scanner.
3.  **Scan and Connect:**
    - Connect the phone to Wi-Fi.
    - Scan the QR code from your computer screen.
4.  **Complete Setup:**
    - Follow the on-screen prompts (Accept Terms, Sign in with the **User ID** you created in the User menu).

### 4. What happens on the Device

- **Work Profile Creation:** The phone will create a "Work Profile" (a separate, secure area for company apps).
- **App Downloads:** The phone will automatically start downloading all apps assigned to that user's group.
- **Lockdown:** If a "Strict" profile is assigned, features like the Camera or Guest Accounts will immediately disappear.
- **Management Badge:** You will see a small **Blue Briefcase icon** on work apps, indicating they are managed by Knox.

### 5. How to Stop (Unenroll)

- **From the Console (Recommended):**
  1.  Go to **Device** > **All Devices**.
  2.  Select the device and click **Device Command** > **Unenroll**.
  3.  The device will automatically remove all work apps and restrictions.
- **From the Device (If allowed):**
  1.  Open the **Knox Manage Agent** app.
  2.  Tap the menu and select **Unenroll**. (Note: This button is usually blocked by admins to prevent users from escaping management).
- **Wipe:** Sending a **Factory Reset (Wipe)** command also unenrolls the device by erasing everything, including the management agent.

---

<!-- **What is the next specific option name on your list?** (e.g., Messaging, Support, or Android Enterprise?) -->

# Knox Manage Guide: Unenroll Device

The **Unenroll Device** command is the official "Exit" process for a device. It breaks the management link between the phone and your console, typically returning the device to its original factory state.

---

### 1. What it is

**Unenrollment** is the process of removing the Knox Manage management profile and the MDM agent from a device. For corporate-owned devices, this is usually a "destructive" action, meaning it wipes the phone to ensure no company data is left behind.

### 2. Why we use it

- **Employee Offboarding:** When an employee leaves the company and needs to return their phone or keep it as a personal device.
- **Hardware Retirement:** When a device is old or broken and needs to be removed from the active inventory.
- **License Recovery:** To "free up" a license seat so you can enroll a new phone without buying more licenses.
- **Device Resale:** To completely clean the phone so it can be safely sold or given away without any company restrictions.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Device** > **All Devices**.
2.  **Select Device:** Find the phone in the list and check the box next to its name.
3.  **Command:** Click the **Device Management** button (or the **Unenroll** button) in the top action bar.
4.  **Confirm Options:**
    - A popup will ask if you want to **Wipe** the device (highly recommended for security).
    - If using **KME (Knox Mobile Enrollment)**, check the box to "Unassign KME Profile" so it doesn't try to re-enroll automatically.
5.  Click **OK**.

### 4. What happens on the Device

- **Instant Reset:** If the phone is online, it will immediately reboot and start a **Factory Reset**. All photos, apps, and accounts are erased.
- **Profile Removal:** The "Work Profile" (the briefcase icons) is deleted.
- **Restriction Lifted:** Once the process finishes, the phone is a "clean slate" with no camera blocks, no wallpaper locks, and no password requirements.
- **Agent Deletion:** The Knox Manage Agent app is uninstalled.

### 5. How to Stop

- **No "Undo":** Once you click OK and the device is online, there is **no way to stop** the unenrollment or the wipe.
- **Offline Force Unenroll:** If a device is lost or broken and cannot connect to Wi-Fi, you can use the **Force Unenroll** option in the console. This removes the device from your list and frees the license, but the physical phone will remain locked until it eventually connects to the internet.
- **Offline Code:** If a user is stuck with a locked phone and has no internet, you can give them an **Offline Unenrollment Code** (found in the Device Details page). They enter this into the Knox app settings to unlock it manually.

---

**What is the next specific option name on your list?** (e.g., **Wipe**, **Factory Reset Protection**, or **Delete Device**?)

# Knox Mobile Enrollment (KME): Device & Profile Guide

This guide covers the **Knox Mobile Enrollment (KME)** portal. While Knox Manage handles the _settings_ (like wallpaper), KME handles the **Automatic Deployment** (making sure the phone connects to Knox Manage as soon as it is turned on).

---

## 1. KME: Device Menu

### A. What it is

The **Device** menu is your inventory list. It contains the unique identifiers (IMEI or Serial Numbers) of every Samsung phone your company owns that is eligible for "Zero-Touch" enrollment.

### B. Why we use it

- **Reseller Integration:** When you buy phones from an authorized reseller, they appear here automatically.
- **Assignment:** This is where you tell a specific physical phone which **Profile** (Ruleset) it should follow.
- **Control:** It ensures that even if a thief factory resets the phone, it will immediately re-enroll into your company system.

### C. Step-by-Step: How to Use it

1.  Log in to the [Knox Mobile Enrollment Portal](https://www.samsungknox.com).
2.  Click **Devices** > **All Devices** on the left.
3.  **Find your device:** Search by IMEI or Serial Number.
4.  **Assign Profile:** Select the checkbox for the device, click **Actions**, and select **Configure Devices**.
5.  Pick your **MDM Profile** from the dropdown and click **Save**.

### D. What happens on the Device

- **Automatic Trigger:** As soon as the user connects to Wi-Fi for the first time, the phone "calls home" to Samsung.
- **Enforcement:** The phone sees it is assigned to your company and forces the download of the Knox Manage agent. The user **cannot** click "Skip" or "Back."

### E. How to Stop

- **Clear Profile:** Select the device and click **Actions** > **Clear Profile**. The phone will now act like a normal consumer phone.
- **Delete:** Remove the device from KME entirely if you sell it or give it away.

---

## 2. KME: Profile Menu

### A. What it is

A **KME Profile** is the "Setup Instructions" for a new phone. It tells the phone: _"Go to this specific Knox Manage server, download this app, and skip these Google setup screens."_

### B. Why we use it

- **Speed:** It hides annoying setup screens (Google Account, Samsung Account, Data Privacy) to get the user to the home screen faster.
- **Automation:** It passes the "Server URL" to the Knox Manage agent so the user doesn't have to type it.
- **DualDAR:** High-security encryption can be enabled here for sensitive government or medical data.

### C. Step-by-Step: How to Use it

1.  Click **Profiles** > **Create Profile**.
2.  Choose **Android Enterprise**.
3.  **Pick your MDM:** Select **Knox Manage** from the list.
4.  **EMM Agent APK:** This is usually pre-filled by Samsung.
5.  **Custom JSON (DPC Extras):** Paste the specific code from your Knox Manage console here (this links the two systems).
6.  **Skip Setup Wizard:** Check the boxes for "Skip Google Account," "Skip Samsung Account," etc.
7.  Click **Save**.

### D. What happens on the Device

- **Zero-Touch Experience:** The user turns on the phone, hits "Start," connects to Wi-Fi, and the phone does the rest.
- **Branding:** Your company name will appear on the screen during the "Checking for updates" phase.

### E. How to Stop

- **Modify Profile:** You can edit the profile to uncheck "Skip" options if you want users to sign in with personal accounts.
- **Delete Profile:** Deleting the profile in KME will cause any device assigned to it to fail enrollment until a new profile is assigned.

---

<!--
**What is the next specific option name on your list?** (e.g., Resellers, Activity Logs, or Knox Suite?) -->

# Apple ADE Guide: Server Setting & Device Management

**Automated Device Enrollment (ADE)**—formerly known as DEP—is Apple’s version of "Zero-Touch." It allows you to manage iPhones, iPads, and Macs from the moment they are turned on, without ever touching the device yourself.

---

## 1. ADE Server Setting

### A. What it is

The **Server Setting** is the "Digital Bridge" between **Apple Business Manager (ABM)** and your **Knox Manage** console. It uses a secure "Token" file to prove that your console has the authority to manage Apple’s hardware.

### B. Why we use it

- **Trust Establishment:** Without this link, Apple will not send device information to your console.
- **Security:** It ensures that only _your_ company can manage the iPhones you purchased.
- **Annual Renewal:** Apple requires this token to be updated once a year for security compliance.

### C. Step-by-Step: How to Use it

1.  **Download Public Key:** In Knox Manage, go to **Settings** > **Apple ADE** > **Server Setting** and click **Download Public Key (.pem)**.
2.  **Upload to Apple:** Login to [Apple Business Manager](https://business.apple.com), go to **Preferences** > **MDM Servers**, click **Add**, and upload that `.pem` file.
3.  **Download Apple Token:** Apple will generate a **Server Token (.p7m)**. Download it.
4.  **Upload to Knox:** Go back to Knox Manage and upload that `.p7m` token into the Server Setting screen.
5.  **Save:** Once uploaded, the "Status" should change to **Connected**.

### D. What happens on the Device

The device "checks in" with Apple's activation servers during the first "Hello" screen. Because the server is linked, Apple tells the phone: _"You belong to Knox Manage. Go there for instructions."_

### E. How to Stop

- **Delete Token:** Remove the token from Knox Manage.
- **Delete Server:** In Apple Business Manager, delete the MDM Server entry. This breaks the link for all devices.

---

## 2. ADE Device Management

### A. What it is

This is the **Inventory List** of every Apple device (iPhone, iPad, Mac) that your company has purchased through an authorized Apple reseller.

### B. Why we use it

- **Assignment:** This is where you decide which "Setup Rules" apply to which iPhone.
- **Syncing:** If you buy 10 new iPads, you use the **Sync** button here to make them appear in your Knox console.
- **Enrollment Profile:** You can choose to "Skip" screens like Siri, Touch ID, or Apple Pay to make the setup faster for the user.

### C. Step-by-Step: How to Use it

1.  **Assign in ABM:** First, go to Apple Business Manager > **Devices**, select your phones, and click **Edit MDM Server** to point them to your Knox server.
2.  **Sync in Knox:** In Knox Manage, go to **Device Enrollment** > **Apple ADE** > **Device Management** and click **Sync**. Your iPhones will now appear in the list.
3.  **Apply Profile:** Select the devices and click **Assign Profile**. Choose a profile that defines which setup screens to hide.
4.  **Verify:** Ensure the "Enrollment Status" shows as **Assigned** or **Pushed**.

### D. What happens on the Device

- **Remote Management Screen:** After the user connects to Wi-Fi, they will see a screen that says: _"Remote Management: [Your Company Name] will automatically configure your iPhone."_
- **Mandatory Enrollment:** The user **cannot** skip this screen. They must click "Next" to continue, which installs your management profile.

### E. How to Stop

- **Unassign:** In the Knox console, select the device and click **Remove Profile**.
- **Release Device:** If the device is stolen or sold, you must "Release" it in Apple Business Manager. **Warning:** Once a device is "Released" from Apple Business Manager, it can **never** be added back to ADE/DEP again.

---

<!-- **What is the next specific option name on your list?** (e.g., APNs Certificate, VPP (Apps), or Android Enterprise?) -->

# Windows Guide: Enrollment Setting & Device Management

This guide explains how to bring Windows 10 and 11 devices under management and how to control them once they are in your fleet.

---

## 1. Windows Enrollment Setting

### A. What it is

**Enrollment Setting** refers to the initial configuration and the method used to register a Windows device (PC, Laptop, or Tablet) into the Knox Manage console. Unlike mobile devices, Windows offers several "Cloud-native" paths for enrollment.

### B. Why we use it

- **Unified Fleet Management:** Manage your PCs alongside your mobile phones in one console.
- **Security Compliance:** Force BitLocker encryption, Windows Updates, and firewall settings.
- **Software Distribution:** Remotely install `.msi` or `.exe` applications across all office computers.

### C. Step-by-Step: How to Use it

There are three main ways to enroll Windows devices:

1.  **Manual Agent (Microsoft Store):**
    - Search for **"Samsung Knox Manage"** in the Microsoft Store on the PC.
    - Install the app and sign in with the **User ID** created in the Knox console.
2.  **Windows Settings (Entra ID / Azure AD):**
    - On the PC, go to **Settings** > **Accounts** > **Access work or school**.
    - Click **Connect** and select **"Join this device to Microsoft Entra ID"**.
    - Login with the work email. If auto-enrollment is configured, the device joins Knox Manage automatically.
3.  **Provisioning Package (.ppkg):**
    - Use the **Windows Configuration Designer** tool to create a `.ppkg` file.
    - Run this file on a new PC (even from a USB drive) to skip the setup wizard and enroll the device instantly.

### D. What happens on the Device

- **Management Sync:** A "Work or School" account is added to the Windows account settings.
- **Policy Application:** The PC will immediately download its assigned profile, which might change the wallpaper, disable the USB ports, or force a password change.
- **Agent Presence:** The Knox Manage agent runs in the background to report the PC's health and location to the admin.

### E. How to Stop

- **Disconnect:** On the PC, go to **Settings** > **Accounts** > **Access work or school**, select the account, and click **Disconnect**.
- **Note:** If the admin has "Locked Enrollment," the user will be blocked from disconnecting manually.

---

## 2. Windows Device Management

### A. What it is

This is the live list of all enrolled Windows PCs where you can view their real-time data and send remote "Commands."

### B. Why we use it

- **Remote Assistance:** View the PC's hardware specs and current status to help a remote user.
- **Inventory Tracking:** See exactly which version of Windows each PC is running and who is currently logged in.
- **Emergency Response:** If a laptop is stolen, you can **Lock** the user out or **Wipe** the hard drive.

### C. Step-by-Step: How to Use it

1.  Go to **Device** > **All Devices** in the Knox sidebar.
2.  Filter by **Platform: Windows** to see only your PCs.
3.  Select a device to see its **Details** (Battery, Disk Space, IP Address).
4.  Click **Device Management** to send a command:
    - **Lock Device:** Blocks the Windows login screen.
    - **Reboot:** Restarts the PC remotely (after a 5-minute warning to the user).
    - **Enterprise Wipe:** Removes only company apps and data, leaving personal files alone.
    - **Factory Reset:** Erases the entire hard drive and unenrolls the device.

### D. What happens on the Device

- **Real-time Commands:** Commands like "Lock" or "Reboot" happen almost instantly if the PC is connected to the internet.
- **Sync:** When you "Push Profile," the PC checks the server for new apps or changed restrictions immediately.

### E. How to Stop

- **Unenroll:** Select the device in the console and click **Unenroll**. This removes the management link but keeps the user's files.
- **Delete:** Once unenrolled, click **Delete** to remove the record from your console and free up a license seat.

---

<!-- **What is the next specific option name on your list?** (e.g., ChromeOS, License, or System Update?) -->

# Knox Manage Guide: Wear OS Token

The **Wear OS Token** is a specialized enrollment tool designed specifically for Samsung Galaxy Watches (Watch4 and newer) running the Wear OS platform. It allows these devices to be managed as professional enterprise tools.

---

### 1. What it is

A **Wear OS Token** is a unique, time-limited QR code generated in the Knox Manage console. It acts as the "key" to authorize a smartwatch to join your company’s management system, usually via a "Staging Phone" that handles the setup process.

### 2. Why we use it

- **Enterprise Pairing:** Standard Galaxy Watches are designed for personal use; the Token allows them to be registered to a **Company Account** instead of a personal Gmail.
- **Standalone Management:** It enables "Freestanding Mode," where the watch can function independently of a phone after the initial setup.
- **Bulk Enrollment:** An admin can use one "Staging Phone" to enroll 50 watches one after another using the same Token, saving hours of manual setup.
- **Kiosk Mode for Watches:** You can lock a watch into a single app (like a fitness tracker or a delivery notification app) which requires this token-based enrollment.

### 3. Step-by-Step: How to Use it

1.  **In the Console:**
    - Go to **Device Enrollment** > **Wear OS Token**.
    - Click **Add**.
    - Set a **Token Name** (e.g., _Warehouse_Watch_Batch_A_).
    - Choose an **Expiration Date** (how long the QR code will stay active).
    - Select the **User Group** these watches will belong to.
    - Click **Save**. A QR code will appear on your screen.
2.  **On the Staging Phone (The "Admin Phone"):**
    - Install the **Knox Manage Enrollment** app from the Play Store.
    - Open the app and select **Wear OS Enrollment**.
    - Scan the QR code from your computer screen.
3.  **On the Watch:**
    - Turn on the new Galaxy Watch.
    - When prompted on the Staging Phone, follow the Bluetooth pairing steps.
    - The phone will "push" the token to the watch, completing the enrollment.

### 4. What happens on the Device

- **Manager App:** A hidden "Knox Manage" controller is installed on the watch.
- **Policy Activation:** The watch will immediately follow your rules (e.g., **Always-on Screen**, **Disabled GPS**, or **Custom Watch Face**).
- **Enterprise Branding:** In the "About Watch" settings, it will show as **"Managed by [Your Company]"**.
- **Security:** The user is blocked from factory resetting the watch unless you allow it in the profile.

### 5. How to Stop

- **Expire the Token:** Once your batch of watches is enrolled, you can delete the token in the console so no more watches can be added.
- **Unenroll Command:** Go to **Device** > **All Devices**, select the watch, and click **Unenroll**. The watch will automatically factory reset and wipe all company data.
- **Offline Exit:** If the watch has no internet, you must provide the user with a **One-Time Password (OTP)** from the device details page in the console to manually bypass the lock.

---

<!-- **What is the next specific option name on your list?** (e.g., **Messaging**, **KSP**, or **Application List**?) -->

# Knox Manage Guide: Android Zero-Touch Enrollment

**Zero-touch enrollment** is Google's automated provisioning method for bulk-deploying corporate-owned Android devices. It allows devices to be configured online and shipped directly to users for immediate, "out-of-the-box" management.

---

### 1. What it is

Zero-touch enrollment is a streamlined process that automatically installs your management agent (Knox Manage) on a device during its very first boot or after a factory reset. It is the Android equivalent of Apple's Automated Device Enrollment (ADE).

### 2. Why we use it

- **Hands-Free Deployment:** Admins don't need to manually touch every phone; devices are pre-registered by authorized resellers.
- **Enforced Management:** Even if a user factory resets the device, it will automatically re-enroll into your company's Knox Manage system as soon as it hits the "Welcome" screen.
- **Security:** It creates a "chain of trust" from the manufacturer to your company, preventing unauthorized personal devices from entering your secure environment.
- **Scale:** Ideal for large roll-outs where manual QR code scanning or token entry would take too much time.

### 3. Step-by-Step: How to Use it

1.  **Purchase Devices:** Buy compatible hardware (Android 9.0+) from an [authorized zero-touch reseller](https://support.google.com/work/android/answer/7514005?hl=en).
2.  **Link Accounts:**
    - In the Knox Manage console, go to **Device Enrollment** > **Zero-Touch**.
    - Sign in with the corporate Google account linked to your reseller and click **Link**.
3.  **Create a Configuration:**
    - In the linked portal, navigate to **Configurations** and click the **+**.
    - **EMM DPC:** Select **"Samsung Knox Manage"** (or use the DPC extras provided in your console).
    - **Support Info:** Enter your company name, IT support email, and phone number.
4.  **Assign to Devices:**
    - Go to the **Devices** tab in the portal.
    - Select your devices and choose your new configuration from the dropdown to apply it.

### 4. What happens on the Device

- **Setup Trigger:** After unboxing and connecting to Wi-Fi, the device checks Google's servers and finds its assignment.
- **Forced Enrollment:** The user sees a screen stating: _"This device belongs to your organization"_.
- **Automatic Installation:** The phone silently downloads and launches the Knox Manage agent.
- **User Login:** The user simply enters their work credentials to finish the setup.

### 5. How to Stop

- **Temporary Stop:** To stop a device from enrolling on its next reset, go to the portal's **Devices** tab and set the configuration to **"No config"**.
- **Permanent Removal (Deregister):**
  - Select the device in the Zero-touch portal and click **Deregister**.
  - **Warning:** Once deregistered, you usually must contact your reseller to get it added back.
- **Unlink Portal:** To stop using zero-touch entirely for your tenant, go to **Device Enrollment** > **Zero-Touch** in Knox Manage and click **Unlink account**.

---

<!-- **What is the next specific option name on your list?** (e.g., **Knox Suite**, **Shared Device**, or **Report**?) -->

# Knox Manage Guide: History (Audit Log & Service History)

The **History** menu is the definitive record of every action taken within your Knox Manage console. It is primarily used for auditing, troubleshooting, and tracking the success of commands sent to devices.

---

### 1. What it is

The **History** section is a centralized log of all administrative and system events. It is divided into several key areas:

- **Audit Log:** Records who (admin) did what (action) and when (time) across the entire console.
- **Device Command History:** Tracks the lifecycle of commands (Lock, Wipe, Sync) sent to devices, showing if they were successfully received.
- **Send Message History:** Logs all emails and text messages sent to users from the portal.
- **Device Log / Diagnostics Log:** Technical logs collected directly from the device for deep troubleshooting.

### 2. Why we use it

- **Accountability:** If a device was accidentally wiped, you can use the **Audit Log** to find out which administrator triggered the command.
- **Verification:** After sending a "Push Profile" command, you check the **Device Command History** to confirm the device actually received the update.
- **Compliance:** Many industries require a "Paper Trail" of all security changes. Knox Manage retains these audit events for at least **three months**.
- **Troubleshooting:** If an app fails to install, the **Device Log** provides error codes that explain why (e.g., "Insufficient Storage").

### 3. Step-by-Step: How to Use it

1.  **To view General Audits:**
    - Navigate to **History** > **Audit Log**.
    - Set the **Log Date & Time** range.
    - Filter by **User ID** (Admin) or **Event** (e.g., "Add User" or "Modify Policy") and click **Search**.
2.  **To view Command Status:**
    - Navigate to **History** > **Device Command History**.
    - Search by **Device Name**.
    - Click **Detail** in the log row to see the **Result Code** (0 usually means success).
3.  **To Download Records:**
    - On any history page, click **Download** or **Export as Excel/CSV** to save the records for your internal documentation.

### 4. What happens on the Device

- **Passive Tracking:** The history logs are generated on the **Server side**. The user does not see any change on their phone when you view these logs.
- **Diagnostic Collection:** If you request a **Device Diagnostics Log**, the user may see a brief notification that logs are being collected and sent to the administrator.

### 5. How to Stop

- **Retention Limits:** You cannot "turn off" history logging as it is a core security feature. However, **Audit Events** are automatically deleted from the server after **three months**.
- **Managing Targets:** You can go to **History** > **Audit Log** > **Manage Audit Target** to choose which specific types of events (Console, Server, or Device) you want the system to keep track of.

---

<!-- **What is the next specific option name on your list?** (e.g., **Report**, **Settings**, or **Alert**?) -->

# Knox Manage Guide: Setting (Environment)

The **Setting** menu (often referred to as **Environment Settings**) is the "Control Center" for your management console itself. While Profiles control the devices, the **Setting** menu controls your administrators, your company branding, and the global behavior of the Knox Manage server.

---

### 1. What it is

The Setting section is where you configure the high-level infrastructure of your Knox Manage tenant. It is divided into sub-categories like **Administrator**, **Basic Configuration**, and **Android Enterprise**.

### 2. Why we use it

- **Administrator Control:** To invite other IT staff and define exactly what they can see or change (Role-Based Access Control).
- **Company Branding:** To make the Knox Manage agent on the phone look professional with your company's logo and support contact info.
- **Server Health:** To set how often devices "check-in" with the server (Heartbeat/Keepalive) so you know if a device has gone offline.
- **External Integration:** To link your console to Google (Android Enterprise) or Apple (ADE) for automated enrollment.

### 3. Step-by-Step: How to Use it

1.  **To Manage Admins:**
    - Navigate to **Setting** > **Administrator**.
    - Click **Add** to invite a new admin.
    - **Role:** Select **Super** (full access) or **Sub** (restricted to specific groups).
2.  **To Set Company Branding:**
    - Navigate to **Setting** > **Basic Configuration**.
    - **Logo Image:** Upload your company logo (GIF, JPG, or PNG, max 1MB).
    - **Support Info:** Enter the IT helpdesk phone number and email that will appear on user devices.
3.  **To Configure Android Enterprise:**
    - Navigate to **Setting** > **Android** > **Android Enterprise**.
    - Click **Link Account** to bind your Google corporate account to Knox.

### 4. What happens on the Device

- **Agent Branding:** The [Knox Manage agent app](https://docs.samsungknox.com/admin/knox-manage/configure/advanced-settings/set-the-logo/) on the phone will now show your company’s logo instead of the default Samsung one.
- **Support Shortcuts:** If a user taps "Contact Admin" in the app, it will automatically pull up the email or phone number you entered in the Settings.
- **Sync Frequency:** The phone will wake up and talk to the server based on the **Inventory Schedule** or **Keepalive** settings you defined here.

### 5. How to Stop

- **Removing Admins:** Go to **Setting** > **Administrator**, select the person, and click **Delete** or change their status to **Inactive**.
- **Resetting Branding:** In **Basic Configuration**, click the **Default** button next to the logo to revert to the standard Samsung Knox branding.
- **Unlinking Accounts:** To stop using Android Enterprise, go to the **Android Enterprise** tab and click **Unlink Account**. **Warning:** This may cause managed apps to stop working.

---

<!-- **What is the next specific option name on your list?** (e.g., **Messaging**, **KSP**, or **Application List**?) -->

# Knox Manage Guide: Setting - Configuration

This guide covers the core environmental settings located under **Setting** > **Configuration**. These settings dictate how the management server communicates with your devices and how the Knox Manage app behaves on the phone.

---

## 1. Basic Configuration

### A. What it is

The **Basic Configuration** is the "identity card" of your management console. It allows you to customize the branding and support information seen by your employees.

### B. Why we use it

- **Corporate Branding:** To replace the Samsung Knox logo with your company's own logo.
- **Support Access:** To provide users with an easy way to contact IT if their device is locked or malfunctioning.

### C. Step-by-Step Setup

1.  Go to **Setting** > **Configuration** > **Basic Configuration**.
2.  **Logo Image:** Click **Register** to upload your company logo (Recommended: 512x512 pixels).
3.  **Support Info:** Enter your Company Name, Support Phone Number, and Support Email.
4.  Click **Save**.

### D. Device Result

- The **Knox Manage Agent** app on the phone will now display your company logo.
- Under the "Support" tab in the app, the user will see your specific contact details.

### E. How to Stop

- Click the **Default** button next to the logo or clear the support fields and click **Save**.

---

## 2. Knox Manage Agent Policy

### A. What it is

This defines the security and behavior of the **Knox Manage app** itself on the user's device.

### B. Why we use it

- **Prevent Tampering:** To stop users from manually unenrolling or stopping the management service.
- **Access Control:** To require a password before a user can open the Knox Manage app.

### C. Step-by-Step Setup

1.  Go to **Setting** > **Configuration** > **Knox Manage Agent Policy**.
2.  **Agent Password:** Enable this to set a password required to open the app on the phone.
3.  **Allow Unenrollment:** Set to **No** to prevent users from removing the management.
4.  Click **Save**.

### D. Device Result

- If the user tries to open the Knox Manage app, they will be prompted for a password.
- The "Unenroll" button inside the app will be greyed out or hidden.

### E. How to Stop

- Change the settings back to **Allow** or **Disable** and click **Save**.

---

## 3. Keepalive

### A. What it is

**Keepalive** is the "Heartbeat" of the connection between the server and the device. It determines how often the device "pings" the server to say "I am still online."

### B. Why we use it

- **Real-time Commands:** A shorter Keepalive ensures that commands like "Lock" or "Wipe" reach the device almost instantly.
- **Battery Balance:** A longer Keepalive saves battery but makes the console data less "real-time."

### C. Step-by-Step Setup

1.  Go to **Setting** > **Configuration** > **Keepalive**.
2.  **Interval:** Set the time (e.g., 30 minutes, 1 hour, or 4 hours).
3.  Click **Save**.

### D. Device Result

- The device will wake up its cellular/Wi-Fi radio at the set interval to check for new commands from the admin.

### E. How to Stop

- Change the interval to a longer duration (e.g., 24 hours) to reduce network traffic and battery usage.

---

## 4. Profile Update Schedule

### A. What it is

This setting tells the device how often it should scan itself and report its current "Inventory" (installed apps, battery level, OS version) back to the console.

### B. Why we use it

- **Compliance Tracking:** To ensure your **Dashboard** and **Reports** have the most up-to-date information about your fleet.
- **Policy Verification:** To confirm that the device has actually applied the latest Profile rules.

### C. Step-by-Step Setup

1.  Go to **Setting** > **Configuration** > **Profile Update Schedule**.
2.  **Schedule:** Choose **Daily** or specific **Days of the week**.
3.  **Time:** Set a time (e.g., 12:00 AM) when the device is likely to be on Wi-Fi.
4.  Click **Save**.

### D. Device Result

- At the scheduled time, the device gathers a list of all its settings and sends a "Status Report" to the Knox console.

### E. How to Stop

- Uncheck the schedule boxes or set the frequency to the minimum required by your company policy.

---

# Knox Manage Guide: Android Settings

This guide covers the specialized Android configuration settings located under **Setting** > **Android**. These options define your relationship with Google and control which specific devices are allowed to join your console.

---

## 1. Android Enterprise

### A. What it is

**Android Enterprise (AE)** is the modern management framework developed by Google. This setting links your Knox Manage console to a **Google Managed Play Account**, which is required to silenty install apps and manage Work Profiles.

### B. Why we use it

- **App Management:** You cannot browse or deploy apps from the Google Play Store without this link.
- **Security:** It enables advanced features like "Work Profile" (separating personal and work data) and "Full Managed Device" mode.
- **Silent Install:** It allows you to push apps to phones without the user needing a personal Gmail account.

### C. Step-by-Step: How to Use it

1.  Go to **Setting** > **Android** > **Android Enterprise**.
2.  Click **Link Account** (or **Register**).
3.  You will be redirected to a Google login page. Sign in with a corporate Gmail account (e.g., *it-admin@company.com*).
4.  Follow the prompts to "Complete Registration."
5.  **Save:** Once returned to Knox, the status should show as **Linked**.

### D. What happens on the Device

- **Work Play Store:** A "Work" version of the Play Store appears on the phone, showing only the apps you have approved.
- **Management Features:** The device can now support strict policies like "Remote Wipe" and "App Permissions."

### E. How to Stop

- Click **Unlink Account**. **Warning:** This will break app updates and management for all currently enrolled Android devices.

---

## 2. Limited Enrollment

### A. What it is

**Limited Enrollment** is a "Gatekeeper" setting. It allows you to create a "Whitelist" or "Blacklist" of devices based on their unique hardware IDs.

### B. Why we use it

- **Strict Security:** To ensure that _only_ the specific 50 tablets you bought can join the system.
- **Prevent Personal Use:** Stops employees from trying to enroll their personal home phones into the corporate system.
- **Model Control:** You can set it to only allow "Samsung Galaxy Tab Active4 Pro" and block all other models.

### C. Step-by-Step: How to Use it

1.  Go to **Setting** > **Android** > **Limited Enrollment**.
2.  Change the setting to **Apply**.
3.  **Add Criteria:** Click **Add** and enter the **Model Name**, **IMEI**, or **Serial Number** of the allowed devices.
4.  **Save:** Only devices matching these details will be allowed to finish the enrollment process.

### D. What happens on the Device

- If an unauthorized device tries to enroll, it will get an error message: _"This device is not authorized for enrollment. Please contact your administrator."_

### E. How to Stop

- Change the setting back to **Not Apply**. This allows any device with the correct QR code or credentials to enroll.

---

## 3. Knox Asset Intelligence (KAI)

### A. What it is

**Knox Asset Intelligence** is an advanced analytics tool that provides deep data on battery health, app stability, and network connectivity.

### B. Why we use it

- **Predictive Maintenance:** See which phone batteries are dying (high cycle count) before the employee complains.
- **App Debugging:** Identify if a specific work app is crashing frequently across your fleet.
- **Connectivity Mapping:** See where devices are losing Wi-Fi or Cellular signal in your warehouse or office.

### C. Step-by-Step: How to Use it

1.  Go to **Setting** > **Android** > **Knox Asset Intelligence**.
2.  Set the status to **Allow**.
3.  **Data Collection:** Select which data you want to collect (Battery, App, Wi-Fi).
4.  **Sync:** Ensure the **KAI Agent** is pushed to your devices via the App Library.
5.  **View Data:** Data will then appear in the **Knox Asset Intelligence Console** (accessible via the Samsung Knox dashboard).

### D. What happens on the Device

- A background service monitors system health.
- **No User Impact:** The user does not see any change, though there may be a very slight increase in battery usage for the data reporting.

### E. How to Stop

- Set the status to **Disallow** and click **Save**. This stops all specialized health reporting from the devices.

---

<!-- **What is the next specific option name on your list?** (e.g., **Certificate**, **APNs Certificate**, or **VPP**?) -->

# Knox Manage Guide: iOS & macOS Settings

To manage Apple devices (iPhones, iPads, and MacBooks), Knox Manage must communicate with Apple’s global servers. This requires two specific security "Handshakes": **APNs** for commands and **VPP** for applications.

---

## 1. APNs Setting (Apple Push Notification service)

### A. What it is

The **APNs Setting** is the most important requirement for Apple management. It is a digital certificate that creates a secure, trusted "phone line" between your Knox console and Apple’s servers.

### B. Why we use it

- **Mandatory Requirement:** Apple does not allow any MDM to control its devices without this certificate.
- **Real-Time Commands:** Without APNs, you cannot **Lock**, **Wipe**, or **Sync** an iPhone. The command would simply sit in the console and never reach the phone.
- **Communication:** It tells the Apple device: _"It is okay to listen to instructions from this Knox Manage console."_

### C. Step-by-Step: How to Use it

1.  **Generate CSR:** In Knox Manage, go to **Setting** > **iOS** > **APNs Setting** and click **Download Certificate Signing Request (.csr)**.
2.  **Apple Portal:** Go to the [Apple Push Certificates Portal](https://identity.apple.com) and log in with your Company Apple ID.
3.  **Upload & Download:** Upload the `.csr` file from Knox. Apple will then give you a **Push Certificate (.pem)** file. Download it.
4.  **Upload to Knox:** Go back to the Knox console and upload that `.pem` file.
5.  **Save:** Ensure the status shows as **Active**.
    - **CRITICAL:** This certificate **expires every 365 days**. You must renew it before it expires, or you will lose control of all Apple devices.

### D. What happens on the Device

- **Instant Response:** The device will now react immediately when you send a "Lock" or "Profile Update" command.
- **Trust:** During enrollment, the user will see that the management profile is "Verified" by Apple.

---

## 2. VPP Server Setting (Volume Purchase Program)

### A. What it is

The **VPP Server Setting** links Knox Manage to your **Apple Business Manager (ABM)** Apps account. It manages your "App Licenses."

### B. Why we use it

- **No Apple ID Needed:** This is the best feature. It allows you to install apps on iPhones **without** the employee needing to sign in with a personal Apple ID.
- **Bulk Buying:** If you need 100 copies of a paid app, you buy them in ABM and sync them here.
- **License Reclaiming:** If an employee leaves, you can take the app license back from their phone and give it to a new employee.

### C. Step-by-Step: How to Use it

1.  **Get Token:** Log in to [Apple Business Manager](https://business.apple.com). Go to **Preferences** > **Payments & Billing** and download your **Location Token** (.vpptoken).
2.  **Upload to Knox:** In Knox Manage, go to **Setting** > **iOS** > **VPP Server Setting**.
3.  **Add Token:** Click **Add**, upload the `.vpptoken` file, and click **Save**.
4.  **Sync:** Click **Sync Now**. All the apps you "bought" (even free ones) in Apple Business Manager will now appear in your **Knox App Library**.

### D. What happens on the Device

- **Silent Install:** Apps will suddenly appear on the user's home screen without asking them for a password or permission.
- **Update Control:** You can force apps to update to the latest version automatically.

---

## 3. Device Management (iOS/macOS)

### A. What it is

This is the specialized set of commands and data specific to Apple hardware found in the **Device** and **Profile** menus.

### B. Why we use it

- **Supervised Mode:** If a device is enrolled via ADE (DEP), you get "Supervised" status, which allows you to do things like **Clear Passcode** or **Force Global Proxy**.
- **Mac Control:** For MacBooks, you can enforce **FileVault (Encryption)** and manage system software updates.

### C. Step-by-Step: How to Use it

1.  **Go to Profile:** Create a profile for **iOS** or **macOS**.
2.  **Set Restrictions:**
    - Find **Device Restriction** and set **Allow Camera** to **No**.
    - Find **Passcode** and set **Minimum length** to **6**.
3.  **Assign:** Apply this profile to your "Apple Users" group.

### D. What happens on the Device

- **Immediate Effect:** The iPhone or Mac will instantly require a 6-digit PIN.
- **Lockdown:** On a Mac, the user might be blocked from using the App Store or changing System Settings.

### E. How to Stop

- **Unenroll:** Select the device in the console and click **Unenroll**. This removes all corporate profiles and VPP apps.
- **Token Expiry:** If you let the **APNs token expire**, you cannot stop or change the devices anymore. You would have to factory reset every phone to fix it.

---

<!-- **What is the next specific option name on your list?** (e.g., **ChromeOS**, **Windows**, or **Messaging**?) -->

# Knox Manage Guide: ChromeOS (Preview)

Managing Chromebooks in Knox Manage is unique because it relies on a cloud-to-cloud link with the \*\*

\*\*. Knox Manage acts as the primary interface, while Google’s native technology handles the actual device communication.

---

## 1. ChromeOS Enrollment Setting

### A. What it is

Before managing ChromeOS, you must establish a connection between Knox Manage and your Google Workspace environment. This process is known as **registering the Google admin account**.

### B. Why we use it

- **Cloud Syncing:** Knox Manage cannot see your Chromebooks until they are synced from Google.
- **Centralised Control:** It allows you to manage ChromeOS users, apps, and policies alongside your Android and iOS fleet in one place.

### C. Step-by-Step Setup

1.  **Google Admin Console:** Purchase a **Chrome Enterprise Upgrade** or **Chrome Education Upgrade** license.
2.  **Organization Setup:** Create your Organizations (OUs) and Users in the Google Admin Console first.
3.  **Link to Knox:**
    - In Knox Manage, go to **Setting** > **ChromeOS** > **Sign in with Google**.
    - Sign in with your Google Admin account and authorize all requested permissions.
    - Once returned to Knox, enter the same admin email and click **Authorize**.

---

## 2. ChromeOS Device Management

### A. What it is

Once synced, your Chromebooks appear in the **Device** list. Management is based on the **Organization** they belong to.

### B. Why we use it

- **Organization-Based Profiles:** Knox Manage automatically generates a profile for each synced Organization.
- **Zero-Touch Support:** Chromebooks can be pre-provisioned via Google’s Zero-touch enrollment for out-of-the-box management.

### C. Step-by-Step: How to Enroll Devices

- **Manual Enrollment:**
  1.  Turn on a factory-reset Chromebook. Follow instructions until the sign-in screen.
  2.  Press **Ctrl + Alt + E** to open the **Enterprise Enrollment** screen.
  3.  Sign in with your managed Google account credentials.
- **Zero-Touch Enrollment:**
  1.  In

---

# Knox Manage Guide: Setting - Notice

The **Notice** function is a one-way communication tool used by Administrators to send official company announcements or technical alerts directly to the managed devices.

---

### A. What it is

A **Notice** is a text-based bulletin or announcement created in the Knox Manage console. Unlike a standard SMS or Email, these messages are housed directly inside the **Knox Manage Agent** app on the phone. They are designed for official corporate communication that needs to be archived on the device for a specific period.

### B. Why we use it

- **Company-Wide Announcements:** To notify all employees about office closures, holiday schedules, or new HR policies.
- **Technical Alerts:** To warn users about upcoming server maintenance or a known bug in a specific work app.
- **Security Reminders:** To remind staff to update their OS or change their passwords by a certain deadline.
- **Policy Updates:** To explain _why_ a certain app was recently blocked or why a new restriction was added to their profile.

### C. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Setting** > **Configuration** > **Notice**.
2.  **Create Notice:** Click the **Add** button at the top.
3.  **Fill in Details:**
    - **Title:** The "Subject Line" of your announcement.
    - **Content:** The full message body (e.g., _"Please update your Zoom app by Friday to avoid login issues."_).
4.  **Set Validity (Duration):**
    - **Start Date/Time:** When the message should first appear on phones.
    - **End Date/Time:** When the message should automatically disappear (be deleted) from the phones.
5.  **Assign:** Select the **Organization** or **Group** that needs to see this message.
6.  Click **Save & Apply**.

### D. What happens on the Device

- **Notification:** The user will receive a standard push notification on their phone: _"A new notice has arrived."_
- **Reading:** The user opens the **Knox Manage Agent** app and taps the **Notice** tab (usually a megaphone or bell icon).
- **History:** The message stays in that list until the "End Date" set by the admin is reached, allowing the user to refer back to it at any time.

### E. How to Stop

- **Manual Deletion:** If you sent a notice by mistake, go to **Setting** > **Notice**, select it, and click **Delete**. It will vanish from all devices immediately.
- **Modify:** You can click on an existing notice to edit the text or extend the "End Date" if the information is still relevant.
- **Automatic Expiry:** Once the "End Date" passes, Knox Manage automatically cleans up the message so the user's app doesn't get cluttered with old news.

---

<!-- **What is the next specific option name on your list?** (e.g., **Message Template**, **Reference Data**, or **Administrator**?) -->

# Knox Manage Guide: Setting - Message Template

The **Message Template** function is used to create standardized emails and SMS messages for common administrative tasks, such as sending enrollment invitations or password resets.

---

### 1. What it is

A **Message Template** is a pre-formatted layout for outgoing communications. It uses **Lookup Items** (placeholders) that automatically fill in specific details like a user's name, their temporary password, or the management server URL when the message is actually sent.

### 2. Why we use it

- **Consistency:** Ensures every employee receives the same clear instructions and professional branding.
- **Automation:** Saves time by using placeholders so you don't have to manually type unique details for every user.
- **Standard Workflows:** Predefined "Basic Templates" handle critical system tasks like **Agent Installation**, **Admin OTP**, and **Apple VPP Invites**.

### 3. Step-by-Step: How to Use it

1.  Navigate to **Setting** > **Message Template**.
2.  **Create Template:** Click the **Add** button.
3.  **Configure Details:**
    - **Template Type:** Choose between **Email** or **SMS**.
    - **Message Type:** Select the purpose (e.g., _User Temporary Password_ or _Agent Installation_).
    - **Subject & Content:** Type your message.
4.  **Insert Placeholders:** Click **Search** (or **Lookup**) to find items like `{User Name}` or `{Temporary Password}`. Double-click them to add them to your text.
5.  **Save:** Click **Save** and then **OK**.

### 4. What happens on the Device

- **Delivery:** The user receives a professional email or SMS.
- **Actionable Info:** Because of the placeholders, the user sees their _own_ specific credentials or a direct link to download the management agent.
- **Security:** For password resets, the template ensures the temporary password is delivered securely and formatted correctly for the login screen.

### 5. How to Stop (Manage Templates)

- **Modify:** Go to **Setting** > **Message Template**, select a template, and click **Modify** to update the text or placeholders.
- **Delete:** Select a custom template and click **Delete**. Note that you typically cannot delete "Basic" system-required templates.
- **Track History:** To see which messages were actually sent using these templates, check **History** > **Email & SMS History**.

---

<!-- **What is the next specific option name on your list?** (e.g., **Reference Data**, **Administrator**, or **Android Enterprise**?) -->

# Knox Manage Guide: Administrator

The **Administrator** menu is where you manage the IT staff who have access to the management console. It allows you to delegate responsibilities by assigning specific "Roles" and "Permissions" to different team members.

---

### 1. What it is

An **Administrator** account is a privileged login used to configure, monitor, and manage devices, users, and policies. Knox Manage uses **Role-Based Access Control (RBAC)** to ensure that each admin only has access to the tools they need for their specific job.

### 2. Why we use it

- **Security:** By creating separate accounts, you don't have to share a single "Super Admin" password with the whole team.
- **Delegation:** You can give a "Help Desk" person permission to lock/wipe devices but block them from changing security policies.
- **Accountability:** All actions taken by an administrator are recorded in the **Audit Log**, so you know exactly who made a change.
- **Organization-Specific Control:** You can restrict a "Sub-Admin" so they can only see and manage devices in a specific branch (e.g., "New York Office").

### 3. Step-by-Step: How to Use it

1.  **Invite an Admin:**
    - Log in to the [Knox Admin Portal](https://central.samsungknox.com) and go to **Administrators & Roles**.
    - Click **INVITE ADMIN**, enter their name and work email, and select a basic role (e.g., Knox Manage Sub-Admin).
2.  **Set Detailed Permissions:**
    - Go to **Setting** > **Administrator** in the **Knox Manage console**.
    - Select the newly invited admin and click **Modify**.
3.  **Select Admin Role:**
    - **Super:** Full access to everything.
    - **Sub:** Limited access based on your choices.
    - **Read-Only:** Can see everything but cannot change any settings.
    - **Service:** Can only send specific device commands (like Sync or Lock).
4.  **Define Access:** Check the boxes for specific menus (e.g., **Device**, **Profile**, **Application**) you want them to use.
5.  **Save:** Click **Save** to apply the permissions.

### 4. What happens on the Device

- **No Direct Change:** Creating an administrator does not change anything on the end-user's phone.
- **Command Execution:** When this admin sends a command (like a "Notice"), the device will see it coming from the authorized management server.

### 5. How to Stop (Modify or Delete)

- **Modify Permissions:** Go back to **Setting** > **Administrator**, select the user, and click **Modify** to add or remove their access to certain menus.
- **Deactivate:** To temporarily block access (e.g., for a staff member on leave), select the admin and click **Change Status** to set them to **Inactive**.
- **Delete:** To permanently remove an admin, select them and click **Delete**.
  - _Note:_ You cannot delete the original "Super Admin" who created the Knox Manage account.
- **Password Reset:** If an admin is locked out, a Super Admin can select them and click **Change Password** to give them a new temporary login.

---

<!-- **What is the next specific option name on your list?** (e.g., **Audit Log**, **Device Log**, or **Report**?) -->

# Knox Manage Guide: License

The **License** menu is the heartbeat of your management console. It is where you activate the "permission" to manage devices. Without a valid license, your commands (like Lock or Wipe) will not work.

---

### 1. What it is

The **License** section is a digital ledger where you store your Samsung Knox activation keys. Each license has a specific **Seat Count** (number of devices allowed) and an **Expiration Date**.

There are two main types:

- **Trial License:** A free 90-day key for testing.
- **Commercial License:** A paid key (usually 1 or 2 years) purchased from a reseller.

### 2. Why we use it

- **Activation:** You cannot enroll even one device until a license is added to the console.
- **Compliance:** To ensure you are staying within the legal limit of devices you have paid for.
- **Service Continuity:** To track when your management is about to expire so you can renew it before your phones lose their security settings.
- **Device Transfer:** To move a phone from a "Trial" status to a "Permanent" status once testing is finished.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Setting** > **License**.
2.  **Add a License:** Click the **Add** button at the top.
    - **License Name:** Give it a nickname (e.g., _2024_Fleet_Key_).
    - **License Key:** Paste the long code provided by Samsung or your reseller.
3.  **Check Status:** Look at the **Status** column:
    - **Active:** Everything is working.
    - **Expired:** The key has ended; you must replace it immediately.
4.  **Replace License:**
    - If your old license is expiring, select it and click **Replace**.
    - Enter the new key. Knox Manage will automatically move all your devices to the new key.
5.  **Assign to Device:**
    - Go to **Device** > **All Devices**.
    - Select your devices and click **Change License** to pick which key they should use.

### 4. What happens on the Device

- **Silent Background Check:** The phone periodically "checks in" to make sure its license is still valid. The user sees **nothing**.
- **Expired State:** If the license expires and isn't replaced, the Knox Manage app on the phone may show a "License Expired" warning.
- **Functionality Loss:** If the license is dead, you can no longer change the wallpaper, block the camera, or install apps. The phone stays in its "last known" state until a new key is added.

### 5. How to Stop

- **Unenrollment:** To "stop" using a license seat, you must **Unenroll** the device. This "frees up" the seat so you can give it to a new phone.
- **Deletion:** You can only **Delete** a license from the console if **zero** devices are currently using it.
- **Grace Period:** Samsung usually gives a **30-day grace period** after the expiration date. During this time, the console stays "Active," giving you time to buy a new key. After 30 days, the console goes into "Read-Only" mode.

---

<!-- **What is the next specific option name on your list?** (e.g., **Admin Role**, **Policy Update**, or **Device Log**?) -->

# Samsung Knox Manage: License Update & Registration Guide

This guide outlines the different workflows for managing Knox licenses within the admin console.

---

## 1. Register a New License Key

Use this method to add a brand-new license key to your console for the first time.

1. Go to **Setting** > **License**.
2. Click **Add**.
3. Enter a unique **License Name** (for your reference).
4. Enter the **License Key** provided by your reseller.
5. Click the **Check icon** to verify, then click **Save**.

---

## 2. Replace an Expiring License (Global Update)

This is the fastest way to swap an old license with a new one across **all** assigned devices at once.

1. Go to **Setting** > **License**.
2. Select the **expiring license** from the list to view its details.
3. Click the **Replace** button.
4. Enter the **New License Key** and click **Save**.
   - _Note: All settings and policies will be reapplied to the devices automatically._

---

## 3. Update License on Selected Devices

Use this if you only want to move specific devices to a different license key.

1. Go to the **Device** menu in the sidebar.
2. Select the specific device(s) you want to update.
3. Click the **Update License** button in the top action bar.
4. Confirm by clicking **OK** to push the latest license info to those endpoints.

---

## 4. Manual Sync (SLM Synchronization)

If you have renewed a license with your reseller but the console doesn't show the updated seat count or expiry date, use the Sync tool.

1. Go to **Setting** > **License**.
2. Select the license(s) you want to refresh.
3. Click the **Sync** button at the top.
   - _Note: This synchronizes data with the Samsung Electronics License Management (SLM) system._

---

## 5. Automated Updates (Scheduler)

You can configure the console to automatically check for license updates on a schedule.

1. Go to **Setting** > **Configuration**.
2. Select **Profile Update Schedule**.
3. Define the frequency (Daily is default) for devices to check in and pull updated license info.

## Pro-Tips for License Management

- Grace Period: Knox Manage typically offers a 30-day grace period after a license expires before devices lose management control.
- Expired Restrictions: On an expired license, you can still send Unenroll or Update License commands, but you cannot push new apps or policies.
- Automatic Migration: If you have multiple valid keys, Knox Manage often automatically uses the one with the earliest expiration that still has available seats for new enrollments.

---

# Knox Manage Guide: License & Capacity Alerts

In Knox Manage, the system automatically triggers a warning when a license reaches **less than 10% of its available seats** or is within **30 days of expiration**. However, you must configure the "Mailing Settings" to ensure these alerts reach your email.

---

### 1. What it is

The **Alert System** is a monitoring tool that watches your license "seats" (how many devices are left) and your "expiry date." It sends an automatic notification so you can buy more licenses before your enrollment stops working.

### 2. Why we use it

- **Prevent Service Block:** If you run out of seats, new employees cannot enroll their phones.
- **Avoid Expiration:** If the license expires, you lose the ability to change policies or lock devices.
- **Proactive Planning:** It gives your procurement team 30 days to process the paperwork for a new purchase.

### 3. Step-by-Step: How to Set Up Email Alerts

To ensure you get an email when seats are low (<10%), follow these steps:

1.  **Navigate to Alerts:**
    - On the left-hand sidebar, go to **History** > **Alert**.
2.  **Manage Alert Targets:**
    - Click the **Manage Alert** button.
    - Ensure that **License-related events** (like "License Expired" or "License Capacity Full") are moved to the **Selected** list.
3.  **Configure Email (Mailing Settings):**
    - Click the **Alert Mailing Settings** button at the top.
    - Set **Alert Mailing Settings** to **Enable**.
    - **Recipients:** Click **Add** and enter the email addresses of the IT admins who need to know.
    - **Frequency:** Choose how often to get the email (e.g., **Real-time** or **Daily Summary**).
4.  **Save:** Click **Save** at the bottom.

### 4. What happens in the Console

- **Dashboard Warning:** A red or orange "Warning" icon will appear on the **License** tile of your main Dashboard.
- **Status Change:** In **Setting** > **License**, the license row may be highlighted in red to show it is critically low.
- **Email Sent:** An automated email from `noreply@samsungknox.com` will be sent to your inbox with the subject: _[Knox Manage] Alert Notification_.

### 5. How to Stop or Reset

- **Add a New License:** Once you add a new license key with more seats, the "Low Capacity" alert will automatically disappear.
- **Disable Mailing:** To stop getting emails, go back to **History** > **Alert** > **Alert Mailing Settings** and set it to **Disable**.
- **Clear Alerts:** You can select old alerts in the **History** list and click **Delete** to clean up your log.

---

<!-- **Would you like to see how to generate a "License Usage Report" to see exactly which devices are using which keys?** -->

<layout>
    # domains_identified: [no_match]
</layout>

# Knox Manage Guide: Identity & Directory

The **Identity & Directory** menu is used to integrate your Knox Manage console with your company's existing user databases, such as **Active Directory (AD)**, **LDAP**, or **Microsoft Entra ID (Azure AD)**.

---

## 1. Connection Setting

### A. What it is

The **Connection Setting** is the link that synchronizes your company's employee data with the Knox console. It allows you to import users, groups, and organizations automatically rather than typing them in manually.

### B. Why we use it

- **Automatic Provisioning:** When a new employee is added to your company’s AD, they are automatically added to Knox Manage.
- **Single Sign-On (SSO):** Users can log into their devices using their standard work email and password.
- **Group Mapping:** You can map your AD groups to Knox Manage groups so that the correct apps and policies are applied based on a user's department.
- **De-provisioning:** If an employee is deleted from your company directory, their Knox account is automatically deactivated, securing the device instantly.

### C. Step-by-Step: How to Use it

1.  Navigate to **Setting** > **Identity & Directory** > **Connection**.
2.  **Add Connection:** Click the **Add** button.
3.  **Choose Connection Type:**
    - **On-premise AD/LDAP:** Requires the [Samsung Cloud Connector (SCC)](https://docs.samsungknox.com) installed on your server.
    - **Microsoft Entra ID (Azure AD):** Uses the Microsoft Graph API for a direct cloud-to-cloud link.
4.  **Enter Server Details:** Provide the IP/Host address, Port (default 389 for LDAP), and Administrator credentials.
5.  **Set Mapping:** Match your directory fields (e.g., `displayName`, `mail`) to Knox Manage fields.
6.  **Scheduler:** Select **Use** to set an automatic sync interval (e.g., Daily or Hourly).
7.  **Save & Sync:** Click **Save & Sync** to start the first import.

### D. What happens on the Device

- **Standardized Login:** During enrollment, the user sees a login screen where they enter their corporate credentials.
- **Automatic Updates:** If a user moves from "Sales" to "HR" in your company directory, their phone will automatically update its apps and restrictions to match their new role.

### E. How to Stop

- **Disable Sync:** Open the connection and set the **Scheduler** to **Not Use**.
- **Delete Connection:** Select the connection and click **Delete**.
  - _Note:_ You must choose whether to keep or delete the users that were already synced to the console.

---

## 2. Connection History

### A. What it is

The **History** tab within Identity & Directory is a dedicated audit log for all synchronization activities.

### B. Why we use it

- **Troubleshooting Sync Errors:** If a new employee is missing from Knox, you check here to see if the last sync failed and read the error code (e.g., "Network Timeout").
- **Verification:** To confirm that a scheduled sync actually ran at the intended time (e.g., 2:00 AM).
- **Change Tracking:** To see exactly how many users were added, modified, or deleted during the last update cycle.

### C. Step-by-Step: How to Use it

1.  Navigate to **Setting** > **Identity & Directory** > **History**.
2.  **View Logs:** You will see a list of every sync attempt.
3.  **Check Details:** Click on a specific sync event to see:
    - **Status:** Success or Failure.
    - **Total Targets:** How many users/groups were scanned.
    - **Result Details:** Specific IDs that failed to sync and why.

### D. What happens on the Device

- **No Direct Impact:** Viewing history is an admin-only action. However, a "Failed" sync in history means the user on the device may not have received their latest updates.

### E. How to Stop

- **Log Retention:** These logs are permanent system records and cannot be "turned off," though old logs are eventually archived by the server.
- **Filtering:** Use the **Filter** icon to hide successful syncs if you only want to see "Failures" to clean up your view.

---

<!-- **What is the next specific option name on your list?** (e.g., **External Certificate**, **Organization**, or **Messaging**?) -->

# Knox Manage Guide: Advanced - Report

The **Report** menu is the "Data Vault" of Knox Manage. While the Dashboard gives you a quick visual summary, the **Report** section allows you to pull deep, detailed information into Excel or CSV files for audits, inventory, and troubleshooting.

---

### 1. What it is

The **Report** section (located under **Advanced** > **Report**) is a powerful data extraction engine. It allows you to search through every piece of information the devices have reported—such as battery health, app versions, storage space, and security status—and organize it into a readable document.

### 2. Why we use it

- **Asset Inventory:** To generate a list of every Serial Number, IMEI, and Phone Number in your company for the finance department.
- **Security Auditing:** To see exactly which devices have a "Compromised" (rooted) OS or which ones are missing a critical security update.
- **Hardware Planning:** To identify devices with "Bad Battery Health" (high cycle counts) so you can replace them before they fail.
- **App Tracking:** To see exactly how many devices have successfully installed a specific work app and which ones failed.
- **Automation:** To set up an automatic "Weekly Report" that gets emailed to your boss every Monday morning.

### 3. Step-by-Step: How to Use it

1.  On the left-hand sidebar, click **Advanced** > **Report**.
2.  **Choose a Report Type:** You will see a list of "Basic Reports" like:
    - **Device Inventory:** General hardware info.
    - **Application Status:** Who has which app.
    - **Policy Compliance:** Who is following the rules.
3.  **Create a Custom Report:**
    - Click the **Add** button.
    - **Report Name:** Give it a title (e.g., _Warehouse_Battery_Health_).
    - **Output Fields:** Click **Add** to choose exactly which columns you want (e.g., _Model, User ID, Battery Status_).
4.  **View & Export:**
    - Click **View** to see the data on your screen.
    - Click **Export to CSV** or **Export to Excel** to download the file to your PC.
5.  **Set Up Mailing:**
    - Click **Report Mailing Settings** at the top.
    - Add your email address and choose a schedule (e.g., _Every Monday at 9:00 AM_).

### 4. What happens on the Device

- **Background Reporting:** The phone silently collects its own "Health Data" (battery level, storage, etc.) and sends it to the server during its periodic **Sync**.
- **No User Interruption:** The user will never know a report is being generated. There is no pop-up or slowdown on the phone.

### 5. How to Stop

- **Stop Mailing:** If you are getting too many emails, go to **Report Mailing Settings**, select the schedule, and click **Delete**.
- **Delete Custom Report:** Select the report you created and click **Delete**. This only removes the "Template"; it does not delete the actual devices.
- **Limit Data:** If you want to save battery on the devices, go to **Setting** > **Configuration** and increase the **Profile Update Schedule** (e.g., once every 24 hours instead of every 4 hours) so the phone reports data less often.

---

<!-- **What is the next specific option name on your list?** (e.g., **Device Log**, **Audit Log**, or **Alert**?) -->

# Knox Manage Guide: Dashboard Management

**Dashboard Management** allows you to customize the very first screen you see when you log in. It turns raw data into visual charts and maps so you can understand your fleet's health in seconds.

---

### 1. What it is

Located under **Advanced** > **Dashboard Management**, this tool lets you create, edit, and organize multiple "Dashboard Views." You can have one dashboard for **Security** (showing compromised devices), one for **Inventory** (showing models and OS versions), and one for **Location** (showing a GPS map).

### 2. Why we use it

- **Customization:** Different admins need different data. A Security Admin wants to see "Policy Violations," while a Helpdesk Admin wants to see "Battery Levels."
- **Efficiency:** Instead of searching through lists, you can see a "Red Slice" on a pie chart and know exactly how many devices are failing.
- **Real-Time Monitoring:** It provides a live "Pulse" of your company's mobile devices.
- **Executive Reporting:** You can show these visual charts to management to prove the fleet is 100% secure.

### 3. Step-by-Step: How to Use it

1.  Navigate to **Advanced** > **Dashboard Management**.
2.  **Create a New View:** Click the **Add** button.
    - **Name:** Give it a title (e.g., _Security_Overview_).
    - **Dashboard Type:** Choose **Widget Type** (for charts) or **Report Type** (for data tables).
3.  **Select Widgets:** Click **Add Widget** to choose what to display:
    - **Device Status:** (Online vs. Offline).
    - **Compliance Status:** (Who is following the rules).
    - **Device Model:** (How many S22s vs. S23s).
    - **Location Map:** (Real-time GPS view).
4.  **Set as Main:** Select your new dashboard and click **Set as Main Dashboard** to make it your default home screen.
5.  **Interactive Action:** On the home screen, you can **click on any chart slice** (e.g., "Offline Devices") to jump directly to the list of those specific phones.

### 4. What happens on the Device

- **Passive Reporting:** The device does not "know" you are looking at the dashboard.
- **Data Push:** The phone sends small "Heartbeat" updates to the server based on your **Keepalive** and **Profile Update Schedule** to make sure the dashboard stays accurate.

### 5. How to Stop

- **Delete View:** Select a custom dashboard you created and click **Delete**. (Note: You cannot delete the "Default" system dashboard).
- **Hide Widgets:** Click the **X** on any specific chart on your home screen to hide it from your view.
- **Reset:** Click **Default Dashboard** to return to the standard Samsung layout.

---

<!-- **What is the next specific option name on your list?** (e.g., **Device Log**, **Audit Log**, or **Alert**?) -->

# Knox Manage Guide: Advanced Certificate Management

This guide covers the **Certificate** infrastructure within Knox Manage. Certificates are the digital "ID cards" that allow devices to connect to secure company Wi-Fi, VPNs, and Email servers without users needing to type in passwords manually.

---

## 1. External Certificate

### A. What it is

An **External Certificate** is a pre-existing digital file (like `.cer` or `.p12`) that you upload directly into Knox Manage. It is not created by the console; it is "imported" from your network team.

### B. Why we use it

- **Trust:** To tell the phone to "Trust" your company's private Wi-Fi server.
- **Authentication:** To give the phone a specific key so it can log into a VPN or Exchange email.
- **iOS Supervision:** For Apple devices, a "Supervision Certificate" allows a specific Mac computer to manage the iPhone via a USB cable.

### C. Step-by-Step: How to Use it

1.  Go to **Advanced** > **Certificate** > **External Certificate**.
2.  Click **Add**.
3.  **Purpose:** Select where this will be used (Wi-Fi, VPN, or Exchange).
4.  **Type:** Choose **Root** (for the server) or **User** (for the person).
5.  **Upload:** Select your certificate file from your PC.
6.  **Save:** Once saved, you must go to your **Profile** and attach this certificate to the Wi-Fi or VPN setting.

### D. Device Result

The certificate is silently installed into the phone's "Credential Storage." When the user tries to connect to the office Wi-Fi, the phone "shows" this certificate to the router, and access is granted instantly.

### E. How to Stop

Select the certificate in the list and click **Delete**. It will be removed from the console and pulled off all assigned devices during their next sync.

---

## 2. Certificate Authority (CA)

### A. What it is

The **Certificate Authority (CA)** setting is a "Bridge." It connects Knox Manage to your company's internal Certificate Server (like Microsoft ADCS or SCEP).

### B. Why we use it

- **Automation:** Instead of manually uploading 500 files for 500 users, Knox Manage "talks" to your server to generate them automatically.
- **Scale:** Essential for large companies where manual certificate handling is impossible.

### C. Step-by-Step: How to Use it

1.  Go to **Advanced** > **Certificate** > **Certificate Authority (CA)**.
2.  Click **Add**.
3.  **CA Type:** Select your server type (e.g., **Microsoft ADCS** or **SCEP**).
4.  **URL:** Enter the web address of your certificate server.
5.  **Test:** Click **Connection Test**. You **must** see a "Success" message before saving.

---

## 3. Certificate Template

### A. What it is

A **Template** is a set of "Instructions" for the CA. It tells the server exactly what kind of certificate to make for the user.

### B. Why we use it

- **Personalization:** You can set the "Subject Name" to `{User Email}`. This ensures every employee gets a certificate with _their_ own name on it automatically.
- **Standardization:** Ensures all certificates have the correct security strength (bits) and expiration length.

### C. Step-by-Step: How to Use it

1.  Go to **Advanced** > **Certificate** > **Certificate Template**.
2.  Click **Add**.
3.  **Select CA:** Pick the CA server you linked in the previous step.
4.  **Subject Name:** Use **Lookup Items** to set the name (e.g., `CN={User Name}`).
5.  **Save:** Now this template is ready to be used in a Profile.

---

## 4. Certificate Issuing History

### A. What it is

This is the **Audit Log** for every certificate the system has ever handed out.

### B. Why we use it

- **Tracking:** To see which devices successfully received their "ID card" and which ones failed.
- **Expiry Monitoring:** To check when certificates will expire so you can renew them before the Wi-Fi stops working for employees.
- **Troubleshooting:** If a user can't connect to VPN, you check here to see if their certificate was actually "Generated."

### C. Step-by-Step: How to Use it

1.  Go to **Advanced** > **Certificate** > **Certificates Issuing History**.
2.  **Search:** Filter by **Device Name** or **User ID**.
3.  **Status:** Look for **"Generated"** (Success) or **"Revoked/Deleted"** (Removed).
4.  **Detail:** Click on a row to see the exact **Issue Date** and **Expire Date**.

### D. How to Stop

You cannot "stop" the history from recording, but you can select old records and click **Delete** to clean up the list. Note that deleting a record for an iOS device may actually trigger the removal of that certificate from the physical device.

---

<!-- **What is the next specific option name on your list?** (e.g., **Reference Data**, **External Certificate**, or **Device Log**?) -->

# Knox Manage Guide: EMM API Settings

The **EMM API** menu (under **Advanced**) is used to integrate Knox Manage with third-party software, such as security platforms or custom company portals, through the **Knox Manage OpenAPI**.

---

## 1. API Client

### A. What it is

The **API Client** is the "User Account" for a piece of software. Instead of a person logging in, an external system uses these credentials to talk to Knox Manage.

### B. Why we use it

- **Third-Party Integration**: To connect Knox Manage with services like **Check Point Harmony Mobile** or **Cisco Umbrella**.
- **Automation**: To allow custom scripts to automatically locate devices, manage users, or send commands without manual admin work.
- **Secure Access**: It provides an **OAuth 2.0** authentication method, generating a unique **Client ID** and **Password** (Client Secret) for the external app.

### C. Step-by-Step: How to Use it

1.  Navigate to **Advanced** > **EMM API** > **API Client**.
2.  **Add a Client**: Click the **Add** button.
3.  **Configure Details**:
    - **Client ID**: Assign a unique name (under 50 characters).
    - **Password**: Enter a secure password (8–30 characters).
    - **Token Validity**: Set how long an authentication token stays active (e.g., 86400 seconds for 24 hours).
    - **Permission Level**: Choose **Management** (can change things) or **Read-Only** (can only view data).
4.  **Save**: Click **Save**. The status will show as **Active**.
    - _Note_: Only **five** API clients can be active at one time.

### D. Device & Console Result

- **External Access**: The third-party software can now use the Client ID and Password to generate a "Bearer Token" and start managing your fleet.
- **No User Impact**: The device user sees no changes, as the API works entirely in the background.

---

## 2. API Log (API Integration Log)

### A. What it is

The **API Log** (often under the **API INTEGRATION** tab) is the "Phone Bill" for your API calls. It records every time an external system successfully or unsuccessfully "talks" to Knox Manage.

### B. Why we use it

- **Verification**: To confirm that your third-party integration is actually sending commands to the console.
- **Troubleshooting**: If an integration stops working, you check here for **Error Codes** to see why (e.g., "Invalid Token" or "Permission Denied").

### C. Step-by-Step: How to Use it

1.  Navigate to **Advanced** > **EMM API** > **API Log**.
2.  **Search**: Filter by **Client ID** or **Date Range** to find specific activities.
3.  **Check Result**: Look for **Success** or **Failure** in the result column.

---

## 3. API Client Log

### A. What it is

The **API Client Log** (under the **API CLIENT** tab) tracks the "Login History" of your API clients. It focuses on the authentication attempts themselves rather than the individual commands being sent.

### B. Why we use it

- **Security Auditing**: To see which external apps are logging in and if there are any suspicious failed login attempts.
- **Authentication Debugging**: If an external app can't connect, this log tells you if it's because of a **wrong password** or an **inactive status**.

### C. Step-by-Step: How to Use it

1.  Navigate to the **API CLIENT** tab in the log section.
2.  **Filter**: Search by **Client ID**, **API Name**, or **Time**.
3.  **View Details**: Click **View Details** to see specific error messages for failed logins.
4.  **Export**: Click **DOWNLOAD AS CSV** if you need to share the login history with your developers or security team.

### How to Stop

- **Deactivate**: Go to **API Client**, select the client, and click **Change Status** to **Inactive**.
- **Invalidate Token**: Click **Invalidate Token** to instantly kill any currently active sessions for that client.
- **Delete**: Select the client and click **Delete** to remove it from the console permanently.
