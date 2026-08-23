# Complete Feature Overview

[中文原文 / Chinese version](功能总览.md)

## v2.1.11 Update Summary

- Attachments can be reordered with a visible drop-position cue. Editors decide per file whether and where it is inserted into the body, and preview actions appear only for browser-native formats.
- Authorized users can select “Edit” from a published content page and enter an editor that fetches the latest saved data. Revision records include attachment additions, removals, order changes, and body-insertion state.
- System administrators can reorder Public Resources and configure their per-file upload limit. Public Resources, notification archives, platform users, and fee statistics have dedicated refresh actions.
- Primary subpages silently fetch current data on entry. Device renaming, audit-detail layout, and the branch-deletion approval flow were refined.
- Safe cleanup now recognizes legacy watermark-derivative keys and walks every results page; source files, avatars, and notification assets remain excluded.
- Product surfaces show the full version number 2.1.11.

## v2.1.10 Update Summary

- Notification-event wakeups, rich-text sanitization, anonymous public-resource verification, branch-storage redaction, and device-session semantics were hardened.
- The rich-text editor is prepared earlier and no longer stalls on circular initialization. Installed standard document fonts are preferred, with first-party compressed fonts as fallback; content remains visible while fonts load.
- Closing an avatar preview no longer redirects to Profile, fee content no longer exposes HTML markup, and help/copy controls were refreshed.
- Watermark derivatives older than 30 days are removed automatically and regenerated from protected sources on the next authorized access. Source files, avatars, and notification assets are excluded.
- Product surfaces show the full version number 2.1.10.

## v2.1.9 Update Summary

- Platform users now appear in a multidimensional table. A separate behavior-audit page presents important actions through plain-language actor, action, target, time, and controlled-detail fields.
- Branch deletion requires a final backup, download evidence from the system administrator and at least one branch administrator, unanimous approval from all branch administrators, and final system-administrator confirmation. An expired backup or any rejection restarts the workflow.
- Automatic notifications are validated and delivered asynchronously after the business operation succeeds.
- Public Resources are grouped into League Affairs, Current Rules, and Learning Resources. Learning Resources are platform-only, while anonymous visitors can access only public items in the first two categories.
- Anonymous visitors see the resource page immediately while security verification runs in the background. Failed or suspicious checks prevent continued access.
- Fee content temporarily excludes body images and attachments, while confirmation, statistics, and archiving remain available. Without a published fee item, only the current-period message and archive history appear.
- Dashboard storage uses actual storage totals. The rich-text editor loads on demand and supports paragraph-level indentation. Product surfaces show the full version number 2.1.9.

## v2.1.8 Update Summary

- The original publisher remains accountable, while editing can be shared with selected administrators and editors in the same branch; all eligible collaborators are selected by default.
- At most one fee item can be published for a period. Each formal archive maps to one fee item, revocation requires a recorded reason, and archive details cannot be deleted.
- Administrators can add, update, or clear single and batch payment notes. Saving refreshes the related lists and dashboard without changing payment status or confirmation time.
- Mobile workspace feedback, the fee dashboard card, role menus, global alerts, and collapsed settings were refined. All time-zone labels now use `GMT+8:00`.
- Both normal and remembered sessions have a fixed 30-day absolute lifetime from initial authentication. Current privacy choices are kept separately from time-limited detailed audits.

## v2.1.7 Update Summary

- Core interface fonts are now lightweight first-party assets loaded early, while compressed document fonts load on demand. Layout remains consistent on slow networks and phones with custom system fonts.
- Pages show structured loading states and reuse local caches for longer. Public PDFs use larger range chunks and retain retry, open-in-new-page, and original-download actions.
- The Devices page groups browser sessions by device and shows this-device status, online state, operating system, recent activity, and coarse network region. Refresh, rename, revoke, and collapsed details are available.
- The Cookie and privacy notice is a formal scrollable document explaining sign-in, security verification, device recognition, and coarse network data. The new policy version requires a fresh choice.
- Notification changes reach the bell and toast sooner. A notification detail opens above the still-open list, so closing the detail returns directly to the same list.
- Storage views emphasize file name and source while treating object paths as truncated auxiliary information. Member tables, device cards, and mobile overlays no longer collapse under long text or sit behind bottom navigation.
- The user-facing role name is simplified to “Member”; legacy import labels remain compatible.

## v2.1.6 Update Summary

- On slow networks, the page no longer interrupts the human-verification challenge with its own retries. Sign-in still waits for a valid result, and the server continues to enforce verification.
- An ordinary session keeps a 24-hour active window while the site remains in use. Sign-in can remember a device for 30 days, and one account may be used on multiple devices.
- “Mine — Devices” merges sessions by actual device and shows browser, operating system, device type, this-device status, online status, last activity, and active-session count. Users can name or revoke unfamiliar devices.
- Public PDFs load in requested ranges. The unified Public Resources entry uses the latest system-administrator records, while member-facing cards omit author and date.
- Avatars in navigation and administration lists open a large preview. On “Mine,” selecting the circular avatar opens the editor and first shows the current avatar at a larger size.
- Editors can enter their branch storage statistics reliably. Long object paths are truncated with a full hover view, preserving the type, size, and latest-update columns.
- Branch deletion still requires backup and approval, but member accounts, passwords, avatars, trusted devices, and sign-in records remain. Storage created by a member is attributed to that member's branch.

## Sign-In and Accounts

- Opening the root site first shows the product introduction page. “Sign In” opens the dedicated sign-in page, while “View Public Files” opens public resources directly.
- The embedded product windows use fictional information to demonstrate structure and basic interactions. They do not read real accounts, branches, fee records, attachments, or database data.
- Sign in with the assigned student ID and password. Security checks begin when the page loads, and submission is unavailable until verification completes.
- A valid session can be restored automatically. Initial passwords must be changed, and old sessions on other devices expire after a password change.
- The sign-in page uses the platform's warm visual palette and provides entries for branch onboarding, sign-in feedback, and public files.
- The concept page, sign-in assistance area, desktop sidebar, and mobile tools drawer share one automatically updated copyright notice.
- Every user can crop an avatar and change the password. Names are maintained by administrators and cannot be changed by members.
- The password form explains the 12–128 character range, passphrases, accepted characters, and password reuse guidance, and asks for the new password twice.
- After sign-in, sign-out, or an account switch, the header, avatar, branch details, and permissions immediately match the current identity.
- Active sessions renew during use but remain bounded by inactivity and absolute lifetime limits. Signing out or changing a password invalidates the relevant old sessions.

## Home and Navigation

- Show a Beijing-time greeting, recent notices, activities, fee status, and common entry points in one place.
- Feature cards are fully selectable and retain “Click to View.” Clear empty states appear when no notice, activity, or fee item is available.
- Desktop navigation can collapse, temporarily reveal, and pin open again. Details pages provide same-module navigation and a location trail.
- Phones use five direct navigation choices: Home, Notices, Activities, Fees, and Mine. Each main module includes a question-mark feature overview for first-time users; administrators, editors, and system administrators can enter the management workspace directly from the header.
- On phones, Home sits in the center of the bottom navigation with an emphasized icon; everyday modules are arranged around it.

## Notices and Activities

- Browse only published content from the member's branch, with search, filtering, sorting, and continuous same-module navigation.
- Details support rich text, images, attachment preview, and downloads. Notice attachments and activity images can be embedded in the body.
- Online preview covers PDFs, TXT/LOG, CSV, Markdown, JSON, XML, and images. Historical TXT metadata with charset parameters is recognized correctly. Office files, audio, and complex legacy formats show download only, without a non-working preview control.
- Revision records identify the operator, time, status change, and summary and are visible to authorized members.
- Protected files display markings related to the current user during preview or download.

## Fee Coordination

- View the current fee notice, personal status, and a branch list containing only names and payment statuses.
- After selecting “I Have Paid,” the button turns green; an administrator verifies the final status.
- Without an active fee notice, payment status cannot be changed and misleading payment entry points are hidden.
- Administrators can verify members individually or in batches. Each fee notice has only one active member-by-member archive.
- Archiving saves a complete snapshot and resets current member statuses to unpaid. Archive details cannot be deleted; correcting a previous archive requires a recorded revocation reason, and the original archive and revocation trail remain available.
- A direct fee-page link returns to the fee page after sign-in or the required first password change.

## Public Resources

- Visitors and signed-in users can view published resources from the public entry regardless of branch.
- Usage guidelines load after selection. Resources can be previewed or downloaded with separate mobile and desktop controls.
- Only system administrators maintain public resources, and the public page does not expose branch content or member information.

## Content and Attachments

- Editors and administrators can create notices, activities, and fee content as drafts, published items, or archives.
- Editors and administrators can view storage statistics scoped to their own branch.
- Notice and activity editors support headings, lists, quotations, links, alignment, images, and freely inserted attachments. Fee content temporarily excludes body images and attachments.
- For supported content types, files can be selected, dragged, or pasted with upload progress. Each attachment follows the size guidance shown on the page.
- The publisher is the current user's name and cannot be hidden or changed. Revision logs are appended automatically.
- Editors see all same-type branch items and can modify items they first published or for which the publisher explicitly granted collaboration access; administrators can manage every item in their branch.
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
- Filter the list to unread items or mark all currently visible notifications as read.
- Opening the list without opening each detail changes existing counts to a dot. A later message or another mutation of the same content restores a numeric badge.
- A content publication creates one notification; later edits update the same notification and append a complete mutation timeline instead of creating repeated messages.
- A new member receives a welcome notice and the full latest platform release. Only platform-wide notices from the last two months are retained; when that window is empty, the latest two are shown.
- Phones use an easy-to-close bottom notification panel. The drawer, cards, and details keep a fixed rounded frame with internal scrolling, and details clear the bottom navigation. Rich text, images, attachments, and related-page links remain supported.
- Administrative notices include the operator, Beijing time, and detailed changes. Deletion decisions are sent to all affected branch members.
- System administrators can publish flexible notifications and search both manual and automatic archives by category, scope, and keyword.

## Branch Details, Capacity, Backup, and Deletion

- From the first visit, branch administrators can maintain organization category, names, field, parent organization, graduation time, person in charge, description, fee guidance, and file purpose.
- Each branch has an independent quota. System administrators can inspect branch usage and categorized actual platform-wide usage.
- The platform notifies all users near the free allowance and pauses storage-increasing actions at the protection threshold.
- System administrators can export a complete branch backup containing content, status, authors, dates, logs, members, fee details, and original attachments.
- Preparation and download progress are visible, leaving is blocked until completion, and the latest backup is required before branch deletion.
- The latest final backup must be downloaded by the system administrator and at least one current branch administrator. A data change invalidates that backup and restarts the workflow.
- Every administrator captured when the request starts must vote. Unanimous approval is required; any rejection invalidates the request and backup, after which the system administrator must restart from a new final backup.

## Multi-Device Experience

- Long titles, paths, tables, rich text, and file previews adapt to narrow screens without page-level horizontal overflow. Important text wraps instead of being hidden by an ellipsis.
- PDFs open fitted to the preview width and support continuous downward reading. The first two pages render first, later pages load progressively, and touch devices support pinch zoom.
- Uploads, downloads, saves, archives, and backups provide loading, progress, or completion feedback.
- Published titles are centered and automatically shrink to one line when no subtitle is present. English body text prefers Times New Roman, Chinese text falls back to FangSong, and code blocks use Calibri.
- Help panels explain the page purpose, available actions, permissions, and safety notes. Error messages identify the affected object, likely cause, save state, and next action instead of exposing a bare HTTP status.
- Complete times are labeled `GMT+8:00`, and reduced-motion device preferences are respected.
- The platform checks the account-level free request allowance every 10 minutes. At the 80% protection threshold, the site switches to a static peak-traffic notice. Accounts and business data remain safe, and full functionality returns automatically after the allowance resets at 08:00 Beijing time.
- The static notice uses the same flag logo as the main site and does not read account, content, payment, or attachment data.
# 2.1 Refinement (2026-07-17)

Rich-text images are inserted at the current cursor as centered block media. Editors independently control body placement and attachment-list visibility. Branch storage now includes source objects, watermarked derivatives, and avatars with a 1.5 GiB default quota. Published saves open the member-facing page, Turnstile offers recoverable retries without bypassing server verification, and transparent avatar crops preserve alpha.
# July 17, 2026 Preview refinement

- Body images have adjustable heights, and an activity can select an explicit cover independently from body and attachment visibility.
- Avatars can use the default, a public HTTPS image URL, or a local file. Every source uses the same circular crop flow; remote images are validated and copied into platform storage.
- System administrators can batch-freeze, unfreeze, or require password changes while sole-administrator protections remain enforced.
- Notification archives are grouped into five operational categories and include a system-administrator-only security-alert class.
- Help dialogs separate purpose, common actions, and cautions with four semantic colors and direct, non-promotional language.

# 2.1 Production Wrap-up (2026-07-18)

- Branch usage is based on actual R2 ownership. Source files, watermark derivatives, and branch avatars all count toward the same branch quota and are shown as separate totals to system administrators.
- New content revision entries show the actual title, summary, body-text, publishing-setting, formatting, and activity-cover changes. Existing historical summaries remain unchanged.
- The visible product version remains 2.1.

# v2.1.4 Production Update (July 23, 2026)

- Refined desktop page height, entry-page typography, mobile management access, metric cards, and tools drawers while reducing repeated avatar loading during navigation.
- Added unread filtering, mark-all-read, structured automatic notices, concise new-member history, and content-level notification aggregation.
- Standardized the copyright notice across four platform surfaces. The visible major version remains 2.1, while the formal release archive is version 2.1.4.
