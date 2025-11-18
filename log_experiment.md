# Data Collection Log

## Experiment Factors and Levels Table

| Factor               | Categories / Levels                                              | Notes                                                             |
|----------------------|------------------------------------------------------------------|-------------------------------------------------------------------|
| Time of Day (TOD)    | Morning (09:00), Afternoon (13:00), Sunset (17:00), Evening (18:00+) | Times in 24-hour format. Represents planned data collection windows. |
| Road Segment         | All segments selected in UNL City Campus                        | s1 = Vine St EB, s2 = Vine St WB. See accompanying PNG map.      |
| Road Surface Type*   | Asphalt (a), Concrete (c), Brick (b), or combinations (b+c)     | Mixed surfaces possible (e.g., Brick + Concrete).                |
| Road Condition Type  | Cracks, Potholes, Mixed                                         | Multiple conditions may appear together (e.g., Crack + Pothole). |
| Traffic Level        | Low, Moderate, Congestion                                       | Most traffic conditions expected to be low volume.               |
| Vehicle Speed Target | 15–20 mph                                                       | Maintain consistent speed within campus.                         |
| Weather              | Clear, Cloudy, Rainy, After-rain (wet road), Snow               | Weather will be included in the log and file name.               |
| ROS Bag Recording    | platform.launch + Autoware.AI recording                         | Example: `2025-11-18-08-58-52.bag`                               |
| ROS Bag Name         | Use short codes for Run + TOD + Segment + Date + Time + Weather + Condition | See naming scheme below.                             |

### Notes

- **r1–r4** represent the four time categories (TOD):
  - r1 = morning  
  - r2 = afternoon  
  - r3 = sunset  
  - r4 = evening

- **s1–s10** represent the testing road segments (see map for details).

### File Naming Example

A recommended filename:

- `r1-s1-2025-11-18-08-58-clear.bag` means data was collected on 11/18/2025 at 8:58 AM, on road segment 1 - Vine St. Westbound, under clear weather conditions. 


## Field Run Observation Table

| Field Run 1          | Seg1         | Seg2          |Seg3       |Seg4       |Seg5           |Seg6       |Seg7           |Seg8       |Seg9            |Seg10          |
|----------------------|--------------|---------------|-----------|-----------|---------------|-----------|---------------|-----------|----------------|---------------|
| Road Surface Type    | A            | A             | B         | A         | A             | A         | A             | A         | B              | A             |
| Road Condition Type  |crack+pothole | crack         |brick+concrete | crack | crack+pothole | crack     | crack+pothole | crack     | brick+concrete | crack+pothole |
| Date                 |2025-11-18    |2025-11-18     |2025-11-18 |2025-11-18 |2025-11-18     |2025-11-18 |2025-11-18     |2025-11-18 |2025-11-18      |2025-11-18     |
| Start Time           | 8:55 AM      | 8:56 AM       | 8:57 AM   | 8:58 AM   | 9:01 AM       | 9:01 AM   | 9:05 AM       | 9:06 AM   | 9:06 AM        | 9:07 AM       |
| Traffic Level        | L            |  L            | L         | L         | L             | L         | L             | L         | L              | L             |
| Vehicle Speed        | < 20 mph     | < 20 mph      | < 20 mph  | < 20 mph  | < 20 mph      | < 20 mph  | < 20 mph      | < 20 mph  | < 20 mph       | < 20 mph      |
| Weather              | Clear        | Clear         | Clear     | Clear     | Clear         | Clear     | Clear         | Clear     | Clear          | Clear         |
| ROS Bag File name    | r1-s1-2025-11-18-08-58-52-clear.bag  | ... | ... |... |... |... |... |... |... |... |


| Field Run 2          | Seg1         | Seg2          |Seg3       |Seg4       |Seg5           |Seg6       |Seg7           |Seg8       |Seg9            |Seg10          |
|----------------------|--------------|---------------|-----------|-----------|---------------|-----------|---------------|-----------|----------------|---------------|
| Date                 |2025-11-18    |2025-11-18     |2025-11-18 |2025-11-18 |2025-11-18     |2025-11-18 |2025-11-18     |2025-11-18 |2025-11-18      |2025-11-18     |
| Start Time           | 12:43 PM     | 12:44 PM      | 12:45 PM  | 12:46 PM  | 12:48 PM      | 12:49 PM  | 12:51 PM      | 12:52 PM  | 12:53 PM       | 12:53 PM      |
| Traffic Level        | L            |  L            | L         | L         | L             | L         | L             | L         | L              | L             |
| Vehicle Speed        | < 20 mph     | < 20 mph      | < 20 mph  | < 20 mph  | < 20 mph      | < 20 mph  | < 20 mph      | < 20 mph  | < 20 mph       | < 20 mph      |
| Weather              | Cloudy       | Cloudy        | Cloudy    | Cloudy    |  Cloudy       | Cloudy    | Cloudy        | Cloudy    | Cloudy         | Cloudy        |
| ROS Bag File name    | r2-s1-2025-11-18-12-43-34-cloudy.bag  | ... | ... |... |... |... |... |... |... |...|


| Field Run 3          | Seg1         | Seg2          |Seg3       |Seg4       |Seg5           |Seg6       |Seg7           |Seg8       |Seg9            |Seg10          |
|----------------------|--------------|---------------|-----------|-----------|---------------|-----------|---------------|-----------|----------------|---------------|

