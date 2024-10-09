FanCode City API Automation:
This project automates the verification of user todo tasks based on the provided scenario for the city FanCode. The automation framework checks if all users belonging to the city FanCode have more than half of their todo tasks completed.
Scenario Requirement: All users of city FanCode should have more than half of their todo tasks completed.
Scenario Details:
      Given: The user has todo tasks.
      And: The user belongs to the city FanCode, which can be identified by:
      Latitude: Between -40 and 5.
      Longitude: Between 5 and 100.
      Then: The user's completed task percentage should be greater than 50%.
APIs Used:
The automation framework uses the JSONPlaceholder APIs for fetching data. Below are the relevant endpoints:
/users: Retrieve user details including latitude and longitude.
/todos: Retrieve the user's todo list to calculate the completion percentage.
Approach:
Identify FanCode City Users:
      Fetch users from /users endpoint.
      Filter users whose address.geo.lat and address.geo.lng fall within the given range for FanCode city.
Calculate Task Completion Percentage:
      Fetch todo tasks for each user from /todos.
      Calculate the percentage of tasks with completed = true.
Validation:
      Verify that each user has a task completion percentage greater than 50%.
