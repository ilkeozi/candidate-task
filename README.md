### **Senior Fullstack Engineer Task**

Thank you for your interest in the role. To evaluate your skills, we’ve prepared a task focusing on **Next.js**, **Material-UI**, and working with APIs. This task must be implemented using **TypeScript**.

Please follow the instructions below and submit your work within **3 days**.

---

### **Task: User Management Dashboard**

**Objective**  
Build a user management dashboard using **Next.js**, **Material-UI**, and **TypeScript**, displaying and interacting with user data from the [JSONPlaceholder API](https://jsonplaceholder.typicode.com/).

---

### **Requirements**

#### **1. Use TypeScript**
- Implement the entire task in **TypeScript**.
- Define proper types/interfaces for API responses and components.

---

#### **2. Fetch and Display Data**
- Use the **JSONPlaceholder API** to fetch user data from `/users`.
- Display the following fields in a **Material-UI DataGrid**:
  - Name
  - Email
  - Address (Street, City, Zipcode)

---

#### **3. Server-Side Filtering and Pagination**
- **Pagination**:
  - Implement server-side pagination using **Next.js API Routes**.
  - The frontend should call an API route like `/api/users` with query parameters for `page` and `limit` to fetch paginated data.

- **Filtering**:
  - Add a search bar to filter users by **name** or **email**.
  - The filtering logic should reside in the API route. When the user types in the search bar, the API route should filter the results based on the query.

- **Implementation Steps**:
  1. Create an API route (`/pages/api/users.ts`) that:
     - Fetches the user list from `https://jsonplaceholder.typicode.com/users`.
     - Implements filtering and pagination logic.
     - Returns a response containing:
       - Filtered and paginated user data.
       - Total count of filtered users (to calculate the total number of pages).

  2. Example API Route Response:
     ```json
     {
       "users": [
         {
           "id": 1,
           "name": "Leanne Graham",
           "email": "Sincere@april.biz",
           "address": {
             "street": "Kulas Light",
             "city": "Gwenborough",
             "zipcode": "92998-3874"
           }
         }
       ],
       "total": 10,
       "page": 1,
       "limit": 5
     }
     ```

  3. Integrate this API route with the **Material-UI DataGrid** in server-side mode.

---

#### **4. User Detail Page**
- Clicking on a user in the DataGrid should navigate to a detail page (e.g., `/users/[id]`).
- Display all the user’s details, including:
  - **Basic Details**: Name, Username, Email
  - **Address**: Street, Suite, City, Zipcode, Latitude, Longitude
  - **Contact**: Phone, Website
  - **Company**: Name, CatchPhrase, BS
- Use Material-UI components (e.g., **Card**, **Typography**) to present the data.

---

#### **5. Styling**
- Use **Material-UI's ThemeProvider** to define a custom theme:
  - Set a custom primary color and secondary color.
  - Apply the theme globally.

---

#### **6. Testing**
- Write at least one **unit test** for a key feature (e.g., search functionality or API call).
- Write at least one **integration test** to verify end-to-end functionality (e.g., navigation from the dashboard to the detail page).
- Use **Jest** and **React Testing Library** for testing.

---

### **Bonus Points**
- Add loading and error states to the DataGrid and detail page.
- Deploy the application to **Vercel** and share the live URL.
- Use Material-UI's **Snackbar** to display notifications (e.g., API errors).

---

### **Deliverables**
1. A **GitHub repository** containing your code.
2. (Optional) A **live deployment link** (e.g., Vercel).
3. A README file explaining:
   - Your approach to solving the task.
   - Any trade-offs made.
   - Steps to run the project locally.

---

### **Evaluation Criteria**
- **TypeScript**: Proper usage of types and interfaces.
- Adherence to **Next.js** and **Material-UI** best practices.
- Code quality, readability, and modularity.
- Efficient use of API calls and state management.
- Bonus: Testing and deployment.

---

### **Example API Documentation**
Use the [JSONPlaceholder API](https://jsonplaceholder.typicode.com/) for data. Example endpoints:
- **Fetch Users:** `GET https://jsonplaceholder.typicode.com/users`
- **Fetch User Details:** `GET https://jsonplaceholder.typicode.com/users/{id}`

