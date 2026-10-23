
# User Stories - Campus Cafeteria Ordering

## Group Information
- **Group Number:** G03
- **Module:** Campus Cafeteria Ordering
- **Group Label:** team-03
- **Product Owner: Tooba
- **Story Writer:** tooba
- **Task Planner:** tooba
- **Tester:** tooba
- **Reviewer:** tooba

---

## US-01 - Browse cafeteria menu

### User Story
As a student, I want to view the cafeteria menu so that I can explore available food items before visiting the counter.

### Acceptance Criteria
- [ ] The menu screen displays all available food categories (e.g., Snacks, Drinks, Meals).
- [ ] Each food item shows its image, title, and price.
- [ ] Items that are out of stock are clearly marked as unavailable.

### Technical Tasks
- [ ] Design the cafeteria menu layout UI.
- [ ] Implement API endpoint to fetch menu categories and items.
- [ ] Connect the menu UI with the backend database.
- [ ] Render food details dynamically on the screen.
- [ ] Test page loading speed and item rendering with sample menu data.

### Story Information
- **Priority:** High
- **Assignee:** tooba-sajid580
- **Status:** Backlog
- **Labels:** `type:user-story`, `team-03`

### Definition of Done
- [ ] All acceptance criteria are satisfied.
- [ ] The assigned tester has verified the story.
- [ ] Another group member has reviewed the work.
- [ ] The team has recorded the required evidence.

---

## US-02 - Search or filter food items

### User Story
As a student, I want to search or filter food items by category or dietary preference so that I can quickly find the exact food I want.

### Acceptance Criteria
- [ ] A search bar and category filter pills are present at the top of the screen.
- [ ] Entering text in the search bar dynamically filters items by name.
- [ ] Selecting a category filter displays only items belonging to that category.
- [ ] The system displays "No food items found" when search results are empty.

### Technical Tasks
- [ ] Add search bar and filter UI components to the menu layout.
- [ ] Write client-side/server-side filtering logic for keywords and category tags.
- [ ] Connect search input to trigger dynamic menu list updates.
- [ ] Handle empty search result states with an appropriate user message.
- [ ] Test filtering with valid keywords, partial words, and non-matching queries.

### Story Information
- **Priority:** Medium
- **Assignee:** [Your GitHub Username]
- **Status:** Backlog
- **Labels:** `type:user-story`, `team-03`

### Definition of Done
- [ ] All acceptance criteria are satisfied.
- [ ] The assigned tester has verified the story.
- [ ] Another group member has reviewed the work.
- [ ] The team has recorded the required evidence.

---

## US-03 - Add items to cart

### User Story
As a student, I want to add food items and select quantities into a shopping cart so that I can collect multiple items into a single order.

### Acceptance Criteria
- [ ] Each menu item card includes an "Add to Cart" button.
- [ ] The student can increase or decrease item quantities before or after adding them to the cart.
- [ ] A cart summary banner or icon updates in real time to show total item count and price.

### Technical Tasks
- [ ] Build cart state management logic (add, remove, update item quantity).
- [ ] Create UI cart component and persistent cart floating bar/button.
- [ ] Validate maximum allowed quantity limits per item.
- [ ] Connect cart state with temporary local storage/session storage.
- [ ] Test adding single, multiple, and duplicate items to the cart.

### Story Information
- **Priority:** High
- **Assignee:** [Your GitHub Username]
- **Status:** Backlog
- **Labels:** `type:user-story`, `team-03`

### Definition of Done
- [ ] All acceptance criteria are satisfied.
- [ ] The assigned tester has verified the story.
- [ ] Another group member has reviewed the work.
- [ ] The team has recorded the required evidence.

---

## US-04 - Place an order

### User Story
As a student, I want to review my cart and confirm payment/order placement so that my food request is submitted to the cafeteria kitchen.

### Acceptance Criteria
- [ ] The checkout page lists all cart items, individual prices, total price, and order summary.
- [ ] The student can select a payment method and click "Confirm Order".
- [ ] Upon successful placement, the system displays an order confirmation with a unique Order ID.
- [ ] The system displays an out-of-stock warning and prevents checkout if an item in the cart becomes unavailable.

### Technical Tasks
- [ ] Design order checkout and summary screen.
- [ ] Implement backend API to process order creation and save order details.
- [ ] Integrate payment gateway mock/logic.
- [ ] Clear cart state upon successful order placement.
- [ ] Test placing orders with valid payment, failed payment, and network drop scenarios.
- [ ] Implement real-time stock verification when proceeding to cart checkout

### Story Information
- **Priority:** High
- **Assignee:** [Your GitHub Username]
- **Status:** Backlog
- **Labels:** `type:user-story`, `team-03`

### Definition of Done
- [ ] All acceptance criteria are satisfied.
- [ ] The assigned tester has verified the story.
- [ ] Another group member has reviewed the work.
- [ ] The team has recorded the required evidence.

---

## US-05 - View order status

### User Story
As a student, I want to view the real-time status of my order so that I know when my food is ready to be picked up.

### Acceptance Criteria
- [ ] The order status page shows active order stages (e.g., Received, Preparing, Ready for Pickup).
- [ ] The system updates status automatically as cafeteria staff updates the order state.
- [ ] The student receives a notification banner when the status changes to "Ready for Pickup".

### Technical Tasks
- [ ] Design active order tracking UI with progress indicators.
- [ ] Implement API endpoint / WebSocket to fetch live order status updates.
- [ ] Connect status updates to staff/kitchen dashboard backend.
- [ ] Add notification alert banner upon "Ready for Pickup" status trigger.
- [ ] Test order state transitions across all stages.

### Story Information
- **Priority:** Medium
- **Assignee:** [Your GitHub Username]
- **Status:** Backlog
- **Labels:** `type:user-story`, `team-03`

### Definition of Done
- [ ] All acceptance criteria are satisfied.
- [ ] The assigned tester has verified the story.
- [ ] Another group member has reviewed the work.
- [ ] The team has recorded the required evidence.

---

## Change Challenge Response

- **Affected User Story:** US-03 (Add items to cart) / US-04 (Place an order)
- **New Requirement:** A food item becomes unavailable after a student adds it to the cart (out-of-stock inventory update during cart holding).
- **Updated Acceptance Criterion:** [ ] If an item in the cart becomes out of stock before order confirmation, the system highlights the item in red, displays an error alert ("Item no longer available"), and prevents checkout until the unavailable item is removed.
- **New or Updated Task:** [ ] Implement pre-checkout inventory validation check to verify item stock availability before finalizing order submission.

---

## Peer Review

- **Reviewed By Group:** G03
- **User role is clear:** Yes
- **User value is clear:** Yes
- **Acceptance criteria are testable:** Yes
- **Missing condition:** Edge case where item inventory drops to zero while user is on the payment screen.
- **Recommended improvement:** Add automatic item removal button directly inside the checkout warning modal for smoother user experience.
