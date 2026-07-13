# Complete Feature Overview

[中文原文 / Chinese version](功能总览.md)

## Sign-In and Accounts

- Sign in with the assigned student ID and password. Security checks begin when the page loads, and submission is unavailable until verification completes.
- A valid session can be restored automatically. Initial passwords must be changed, and old sessions on other devices expire after a password change.
- The sign-in page shows only the platform product name and provides entries for branch onboarding, sign-in feedback, and public official resources.
- Every user can crop an avatar and change the password. Names are maintained by administrators and cannot be changed by members.
- After sign-in, sign-out, or an account switch, the header, avatar, branch details, and permissions immediately match the current identity.

## Home and Navigation

- Show a Beijing-time greeting, recent notices, activities, fee status, and common entry points in one place.
- Feature cards are fully selectable and retain “Click to View.” Clear empty states appear when no notice, activity, or fee item is available.
- Desktop navigation can collapse, temporarily reveal, and pin open again. Details pages provide same-module navigation and a location trail.
- Mobile uses bottom navigation, while administrators, editors, and system administrators can enter the management workspace directly from the header.

## Notices and Activities

- Browse only published content from the member's branch, with search, filtering, sorting, and continuous same-module navigation.
- Details support rich text, images, attachment preview, and downloads. Notice attachments and activity images can be embedded in the body.
- Revision records identify the operator, time, status change, and summary and are visible to authorized members.
- Protected files display markings related to the current user during preview or download.

## Fee Coordination

- View the current fee notice, personal status, and a branch list containing only names and payment statuses.
- After selecting “I Have Paid,” the button turns green; an administrator verifies the final status.
- Without an active fee notice, payment status cannot be changed and misleading payment entry points are hidden.
- Administrators can verify members individually or in batches. Each fee notice has only one active member-by-member archive.
- Archives can be expanded, deleted, or revoked with a reason when allowed, and a revoked archive can be recreated.

## Emblem, Flag, Anthem, and Official Resources

- Visitors and signed-in users can view published resources from the public entry regardless of branch.
- Usage guidelines load after selection. Resources can be previewed or downloaded with separate mobile and desktop controls.
- Only system administrators maintain public resources, and the public page does not expose branch content or member information.

## Content and Attachments

- Editors and administrators can create notices, activities, and fee content as drafts, published items, or archives.
- The editor supports headings, lists, quotations, links, alignment, images, and freely inserted attachments.
- Files can be selected, dragged, or pasted, with upload progress. Each attachment follows the size guidance shown on the page.
- The publisher is the current user's name and cannot be hidden or changed. Revision logs are appended automatically.
- Editors see all same-type branch items but can modify only their own; administrators can manage every item in their branch.
- Leaving with unsaved changes triggers a warning, and pending attachment deletions occur only after a successful save.

## Members, Roles, and Accounts

- Administrators can add or batch-import members and maintain names, roles, status, and passwords.
- Role changes automatically notify the affected user with the operator and time. Branch administrators cannot remove other administrators.
- Each ordinary account is unique across the platform and can belong to at most one branch. An account in another branch cannot be added again.
- “Remove from Branch” preserves the account, password, avatar, and historical responsibility records. Unassigned accounts can still open the profile and send feedback.
- Only system administrators can permanently delete accounts or reset any user's password from “Platform Users.”
- Platform users can be filtered by keyword, role, branch, and status. The current account, last system administrator, and every branch's sole administrator are deletion-protected.

## Notification Center

- Automatically receive platform releases, branch settings, content publications or updates, role changes, account security, backups, and deletion decisions.
- Unread items are clearly marked and become read after opening. Details support rich text, images, attachments, and related-page links.
- Administrative notices include the operator, Beijing time, and detailed changes. Deletion decisions are sent to all affected branch members.
- System administrators can publish flexible notifications and search both manual and automatic archives by category, scope, and keyword.

## Branch Details, Capacity, Backup, and Deletion

- From the first visit, branch administrators can maintain organization category, names, field, parent organization, graduation time, person in charge, description, fee guidance, and file purpose.
- Each branch has an independent quota. System administrators can inspect branch usage and categorized actual platform-wide usage.
- The platform notifies all users near the free allowance and pauses storage-increasing actions at the protection threshold.
- System administrators can export a complete branch backup containing content, status, authors, dates, logs, members, fee details, and original attachments.
- Preparation and download progress are visible, leaving is blocked until completion, and the latest backup is required before branch deletion.
- The first administrator decision locks the current deletion request, and the result is sent to the system administrator and every branch member.

## Multi-Device Experience

- Long titles, paths, tables, rich text, and file previews adapt to narrow screens without page-level horizontal overflow.
- Uploads, downloads, saves, archives, and backups provide loading, progress, or completion feedback.
- Complete times are labeled “Beijing Time GMT+8:00,” and reduced-motion device preferences are respected.
