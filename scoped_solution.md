# Unified List of General Solutions and Scopes

## Goal Alignment and Hierarchy

1. **Provide a Hierarchy of Goals**:

   - Three levels: long-term, short-term, and weekly.
   - Long-term goals: Must be set within 3 to 12 months.
   - Short-term goals: Must be set within 1 month to the duration of the long-term goal.
   - Weekly goals: Fixed and must be written on Sundays.
   - Daily schedules: Can only be set if part of the current week (excluding Mondays) and if they have not passed.

2. **Goal Setting and Periods**:
   - Ensure that the hierarchy of goals eventually leads to daily schedules.
   - Allow users to set periods for the hierarchy (e.g., yearly, semesterly, weekly, daily).
   - Provide previews of the immediate higher goals in the hierarchy and calendar events within the specified period.
   - Allow linking of lower hierarchy goals to the encompassing higher-level goal.

## Goal Sharing and Privacy

1. **Mandatory Sharing**:
   - Users must share at least one weekly goal. They cannot start sharing from the daily schedule level.
2. **Selective Sharing**:
   - Allow users to share selected goals.
   - By default, share all goals and schedules linked up to the goal.
   - Allow users to prevent selected goals and schedules from being shared by default.
   - Enable friends to monitor the progress of shared goals, showing total progress without revealing the specifics of unshared sub-goals and schedules.

## Updating Goals

1. **Managing Goals**:

   - Removing Goals: Goals can be deleted, but this action will also delete all sub-goals and schedules. To avoid this, goals can only be closed.
   - Impact on Progress: When goals are closed, their previous progress will still affect the overall progress.
   - Fixed Time Allocation: Time allocated for a goal or hierarchy cannot be extended. Users can close the goal and extend a new goal from it to maintain historical records.
   - Sub-Goals Continuation: When a higher hierarchy goal is closed, all sub-goals and schedules will continue to exist until explicitly closed.
   - New Goals from Closed Goals: Extending a new goal from a closed one will reflect all progress from the previous goal.

2. **Editing Goals and Schedules**:
   - Rearranging Daily Schedules: Daily schedules can be rearranged unless the allocated time has passed.
   - Editing Content: Users can edit the content of schedules and goals, but the system will not treat the changes semantically.
   - Adding New Goals: Enable adding new goals after the initial plan is set.

## Keeping Track of Wasted Time

1. **Tracking Wasted Time**:
   - Wasted time is collected from unchecked tasks in the daily schedule.
   - Metrics for Active Hours: Active hours are measured based on the value of accomplished tasks.

## Task Overload and Prioritization

1. **Prioritization**:
   - Allow users to assign priorities to goals.
   - Enable users to update assigned priorities.
   - Provide default priorities based on the number of linked goals.

## Estimating Progress Metrics

1. **Progress Metrics**:
   - Allow users to enter multiple quantitative measures for goals and schedules.
   - Enable users to set scale factors to determine the effect of sub-goals when linking goals.
   - Allow users to enter quantitative values of metrics after completing schedules.

## Real-Time Progress Updates

1. **Automatic Updates**:
   - Provide automatic progress updates for higher hierarchy goals using the received scale factors.

## Visualizing Progress

1. **Progress Visualization**:
   - Display progress made so far towards goals and how much is left.
   - Show the rate at which users are reaching their goals.

## Missed Alarms

1. **Notifications**:
   - Send notifications with motivational messages when the time for a task in the daily schedule is finished.
   - Allow users to disable this feature.

## Income and Expense Tracking

1. **Financial Management**:
   - Allow users to enter their income.
   - Enable users to record expenses with reasons.
   - Allow users to set a percentage for savings.
   - Calculate the savings amount based on the set percentage.
   - Provide summarized financial data over time based on the hierarchy of goal periods.

## Calendar Integration

1. **Integration with Google Calendar**:
   - Allow users to import calendars from other platforms.
   - Enable users to manage their calendars within the app to mark events.
   - Integration will only be with Google Calendar.

## Historical Data Analysis

1. **Data Persistence**:
   - Persist data until explicitly removed by the user.
   - Provide structured historical goals and schedules.

## Accessibility and Cross-Device Sync

1. **Web Platform Accessibility**:
   - Use a web platform for accessibility on various devices (phones, tablets, computers).
