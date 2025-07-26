# Project Aman - MVP User Flow

This document defines the core user experience for the Minimum Viable Product (MVP) of the Aman mobile application. The guiding principle is **ruthless minimalism**. Every screen and every action must directly serve the core loop of attesting and confirming a real-world payment to build a verifiable reputation.

---

### **Flow 1: First-Time User Onboarding**

1.  **Screen: Welcome**
    *   **Text:** "Welcome to Aman. The simple way to make your community's trust verifiable and portable. Let's create your secure digital identity."
    *   **Action:** [Create Identity] button.

2.  **Screen: Identity Creation**
    *   **Text:** "Choose a username. This cannot be changed."
    *   **Input Field:** Username.
    *   **Action:** [Next] button.

3.  **Screen: Secure Your Account**
    *   **Text:** "IMPORTANT: Write down these 12 words in order and keep them somewhere safe. This is the only way to recover your account if you lose your phone. We cannot help you recover it."
    *   **Display:** A list of 12 unique words (the recovery phrase).
    *   **Action:** [I Have Written It Down] checkbox.
    *   **Action:** [Go to My Account] button (only becomes active after the checkbox is ticked).

---

### **Flow 2: The Core Loop (For an Existing Group Member)**

1.  **Screen: Group Home**
    *   **Context:** The user is a member of the "University Friends Iqub".
    *   **Display:**
        *   Group Name: University Friends Iqub
        *   Your Status: `5 of 12 payments made.`
        *   Next Payment Due: `[Date]`
        *   Contribution Amount: `1,000 ETB`
        *   A simple list of members and their payment status (e.g., "Paid" or "Pending").
    *   **Action:** [Mark My Payment as Made] button. This is the primary call to action.

2.  **Screen: Payment Attestation**
    *   **Context:** User has pressed the primary button.
    *   **Text:** "You are about to signal on the blockchain that you have paid your 1,000 ETB contribution to the group treasurer. The treasurer will need to confirm this."
    *   **Action:** [Confirm Signal] button.

3.  **Screen: Awaiting Confirmation**
    *   **Context:** User has confirmed their signal.
    *   **Text:** "Your signal has been sent. Your status will update to 'Paid' once the treasurer confirms receipt of the funds."
    *   **Display:** The user's status on the Group Home screen now shows "Awaiting Confirmation".

---

### **Flow 3: The Treasurer's Action**

1.  **Screen: Treasurer's Group Home**
    *   **Context:** The treasurer opens the app.
    *   **Display:** They see the same Group Home screen, but next to the member who has attested, there is a new prompt.
        *   `[Member Name]: Awaiting Confirmation`
    *   **Action:** [Confirm Receipt] button next to the member's name.

2.  **Screen: Confirmation**
    *   **Text:** "Are you confirming that you have received 1,000 ETB in cash from [Member Name]?"
    *   **Action:** [Yes, Confirm] button.
    *   **Action:** [No, Reject] button.

3.  **Result:**
    *   If confirmed, the blockchain is updated. The member's status for the month flips to "Paid" for everyone in the group to see. The reputation ledger is updated.