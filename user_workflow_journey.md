# UX Workflow Documentation: Parent Fund Management for Youth Account

## Experience Mindset

**Primary User:** Parent/Guardian
**Experience:** Managing a youth account to teach financial responsibility while maintaining control and visibility.

---

## Scenarios & Workflow Variations

### Scenario 1: Access Youth Account Dashboard
**Context:** Parent is logged into the banking web application.
**Action:** Navigates to the youth account section.
**Goal:** Quickly view youth account balance and recent activity.

#### Workflow Variation A: Direct Dashboard Access
- **1.0 Login Screen**
  - *Goal:* Securely authenticate parent.
  - *Description:* Standard login with 2FA.
  - *Design Problem:* HMW reduce login friction while maintaining security?
  - *Design Opportunity:* What if biometric login is available?
- **2.0 Main Dashboard**
  - *Goal:* Provide overview of all accounts.
  - *Description:* Parent sees all accounts, including youth account tile.
  - *Design Problem:* HMW make youth account prominent?
  - *Design Opportunity:* What if youth account is highlighted with recent activity?
- **3.0 Youth Account Dashboard**
  - *Goal:* Show youth account balance, recent transactions, and quick actions.
  - *Description:* Balance summary, recent activity, Add Funds, Set Limit, View Activity.
  - *Design Problem:* HMW surface key actions without clutter?
  - *Design Opportunity:* What if dashboard is customizable?

**Screen Sequence:** 1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Account Dashboard

#### Workflow Variation B: Quick Access from Notifications
- **1.0 Login Screen** (as above)
- **2.0 Notification Center**
  - *Goal:* Alert parent to youth account activity.
  - *Description:* Notification for recent youth account transaction.
  - *Design Problem:* HMW avoid overwhelming with notifications?
  - *Design Opportunity:* What if notifications are actionable?
- **3.0 Youth Account Dashboard** (as above)

**Screen Sequence:** 1.0 Login -> 2.0 Notification Center -> 3.0 Youth Account Dashboard

---

### Scenario 2: Allocate Funds to Youth Account
**Context:** Parent is on youth account dashboard.
**Action:** Selects "Add Funds".
**Goal:** Transfer funds from parent to youth account efficiently.

#### Workflow Variation A: Inline Transfer Modal
- **3.0 Youth Account Dashboard** (from above)
- **Pu.1 Add Funds Modal**
  - *Goal:* Allow quick fund transfer without leaving dashboard.
  - *Description:* Source account selector, amount input, confirm button.
  - *Design Problem:* HMW prevent errors in transfer?
  - *Design Opportunity:* What if modal shows available balance and transfer limits?
- **Pu.2 Confirmation Modal**
  - *Goal:* Confirm transfer details before execution.
  - *Description:* Summary of transfer, confirm/cancel options.
  - *Design Problem:* HMW reduce accidental transfers?
  - *Design Opportunity:* What if confirmation includes educational tips?
- **Pu.3 Success/Error State**
  - *Goal:* Communicate result of transfer.
  - *Description:* Success message or error (e.g., insufficient funds).
  - *Design Problem:* HMW clearly communicate errors?
  - *Design Opportunity:* What if error suggests next steps?

**Screen Sequence:** 3.0 Youth Account Dashboard -> Pu.1 Add Funds Modal -> Pu.2 Confirmation Modal -> Pu.3 Success/Error State

#### Workflow Variation B: Dedicated Transfer Page
- **3.0 Youth Account Dashboard**
- **4.0 Fund Transfer Page**
  - *Goal:* Provide detailed transfer interface.
  - *Description:* Source account, amount, transfer limits, educational content.
  - *Design Problem:* HMW balance detail with speed?
  - *Design Opportunity:* What if page adapts based on transfer history?
- **4.1 Confirmation Step** (inline or modal)
- **4.2 Success/Error State**

**Screen Sequence:** 3.0 Youth Account Dashboard -> 4.0 Fund Transfer Page -> 4.1 Confirmation -> 4.2 Success/Error State

---

### Scenario 3: Set Spending Limit
**Context:** Parent is managing youth account.
**Action:** Configures weekly spending limit.
**Goal:** Set and adjust spending limits easily.

#### Workflow Variation A: Inline Limit Editor
- **3.0 Youth Account Dashboard**
- **Pu.4 Edit Limit Modal**
  - *Goal:* Quickly set or edit spending limit.
  - *Description:* Input for weekly limit, contextual guidance, save/cancel.
  - *Design Problem:* HMW prevent invalid values?
  - *Design Opportunity:* What if guidance is personalized based on spending?
- **Pu.5 Success/Error State**

**Screen Sequence:** 3.0 Youth Account Dashboard -> Pu.4 Edit Limit Modal -> Pu.5 Success/Error State

#### Workflow Variation B: Dedicated Limit Management Page
- **3.0 Youth Account Dashboard**
- **5.0 Spending Limit Page**
  - *Goal:* Provide comprehensive limit management.
  - *Description:* Current limit, edit history, educational content.
  - *Design Problem:* HMW make limits understandable?
  - *Design Opportunity:* What if page shows projected savings?
- **5.1 Success/Error State**

**Screen Sequence:** 3.0 Youth Account Dashboard -> 5.0 Spending Limit Page -> 5.1 Success/Error State

---

### Scenario 4: View Youth Spending Activity
**Context:** Parent wants to review youth account transactions.
**Action:** Selects activity section.
**Goal:** Scan and understand spending patterns.

#### Workflow Variation A: Embedded Activity List
- **3.0 Youth Account Dashboard**
  - *Goal:* Show recent transactions inline.
  - *Description:* List with date, merchant, amount, remaining balance, filters.
  - *Design Problem:* HMW make info scannable?
  - *Design Opportunity:* What if patterns are highlighted (e.g., frequent merchants)?

**Screen Sequence:** 3.0 Youth Account Dashboard

#### Workflow Variation B: Full-Screen Activity View
- **3.0 Youth Account Dashboard**
- **6.0 Activity Page**
  - *Goal:* Provide detailed transaction history and filtering.
  - *Description:* Full list, advanced filters (date, merchant, amount), export option.
  - *Design Problem:* HMW support deep dives without overwhelming?
  - *Design Opportunity:* What if insights are surfaced (e.g., monthly summaries)?

**Screen Sequence:** 3.0 Youth Account Dashboard -> 6.0 Activity Page

---

### Scenario 5: Handle Insufficient Balance During Fund Allocation
**Context:** Parent attempts to transfer funds but lacks sufficient balance.
**Action:** System detects insufficient funds.
**Goal:** Clearly communicate error and guide next steps.

#### Workflow Variation A: Inline Error Message
- **Pu.1 Add Funds Modal**
- **Er.1 Insufficient Funds Error**
  - *Goal:* Alert parent immediately.
  - *Description:* Inline error below amount input, link to add funds to parent account.
  - *Design Problem:* HMW reduce frustration?
  - *Design Opportunity:* What if system suggests alternate funding sources?

**Screen Sequence:** Pu.1 Add Funds Modal -> Er.1 Insufficient Funds Error

#### Workflow Variation B: Dedicated Error Page
- **4.2 Error State**
  - *Goal:* Provide detailed explanation and options.
  - *Description:* Error page with options to retry, contact support, or view help.
  - *Design Problem:* HMW turn errors into learning moments?
  - *Design Opportunity:* What if error page includes financial tips?

**Screen Sequence:** 4.2 Error State

---

## Minimum Viable Experience (MVE)
- Parent logs in, accesses youth account dashboard, views balance and recent activity, allocates funds, sets spending limit, and reviews transactions. Errors (e.g., insufficient funds) are clearly communicated with guidance.

---

## User & Business Goals
- **User Goal:** Empower parents to teach financial responsibility by managing youth account funds, limits, and visibility efficiently and securely.
- **Business Goal:** Increase engagement, build trust, and drive adoption of youth banking products by providing intuitive, transparent, and supportive tools for parents.

---

## Accessibility & Scalability Considerations
- All screens and modals are designed for keyboard and screen reader accessibility.
- Responsive layouts for desktop and tablet.
- Error states and guidance are clear and actionable.
- Workflows support future features (e.g., multiple youth accounts, advanced analytics).

---

## Summary of Screen Sequences (per scenario & workflow)

**Scenario 1:**
- A: 1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Account Dashboard
- B: 1.0 Login -> 2.0 Notification Center -> 3.0 Youth Account Dashboard

**Scenario 2:**
- A: 3.0 Youth Account Dashboard -> Pu.1 Add Funds Modal -> Pu.2 Confirmation Modal -> Pu.3 Success/Error State
- B: 3.0 Youth Account Dashboard -> 4.0 Fund Transfer Page -> 4.1 Confirmation -> 4.2 Success/Error State

**Scenario 3:**
- A: 3.0 Youth Account Dashboard -> Pu.4 Edit Limit Modal -> Pu.5 Success/Error State
- B: 3.0 Youth Account Dashboard -> 5.0 Spending Limit Page -> 5.1 Success/Error State

**Scenario 4:**
- A: 3.0 Youth Account Dashboard
- B: 3.0 Youth Account Dashboard -> 6.0 Activity Page

**Scenario 5:**
- A: Pu.1 Add Funds Modal -> Er.1 Insufficient Funds Error
- B: 4.2 Error State

---

# End of UX Workflow Documentation
