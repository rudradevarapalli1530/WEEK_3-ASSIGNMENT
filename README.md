Table Creation and Sample Data
*Projects Table*
Description:
>Stores project info like name, budget, and start/end dates.
>ProjectID is the primary key.
*Tasks Table*
Description:
>Stores tasks for each project.
>Foreign key links tasks to the Projects table.
>Includes AssignedTo, Status, and Due_Date.
*Teams Table*
Description:
>Keeps track of team names, leaders, number of members, and location.
*Model_Training Table*
Description:
>Tracks AI model training per project, with accuracy and training_date.
*Data_Sets Table*
Description:
>Stores dataset info: size_gb and last_updated.
>Links datasets to projects via project_id
*Projects with total and completed tasks*
>Counts total tasks and completed tasks per project.
>Calculates completion percentage.
*Top 2 team members by number of tasks*
>ROW_NUMBER() ranks team members by tasks assigned.
>Returns top 2 members.
*Tasks earlier than project average due date*
>Finds tasks with Due_Date earlier than the average for their project.
*Project with maximum budget*
>Finds project(s) with the highest budget.
*Best AI model per project*
>Uses window function to rank models per project.
>Selects the highest accuracy model for each project.
*Projects with datasets > 10GB updated in last 30 days*
>Filters datasets larger than 10GB and updated in the last 30 days.
>Joins with Projects to show project info.
*Tasks assigned to team leads, not completed, due within 15 days*
>Filters tasks assigned to team leaders, not completed, and due soon.
*Projects with no tasks*
>Uses LEFT JOIN to find projects without any task records.
