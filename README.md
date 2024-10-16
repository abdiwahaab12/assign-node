# Target Calculation Excluding Specific Days

## Overview
This project implements a function to calculate the proportional distribution of an annual target across multiple months while excluding specific non-working days (Fridays). The function allows users to determine the number of working days for each month within a specified date range and distribute a total target amount based on those valid working days.

## Function: `calculateTotalTarget`

### Description
The `calculateTotalTarget` function calculates:
- The number of working days in each month of the specified range, excluding Fridays.
- The number of days actually worked within the range, also excluding Fridays.
- The proportional distribution of an annual target across valid working days for each month.

### Parameters
- **startDate**: A string in `YYYY-MM-DD` format representing the start of the period for which the target is calculated.
- **endDate**: A string in `YYYY-MM-DD` format representing the end of the period for which the target is calculated.
- **totalAnnualTarget**: A number representing the total annual target amount to be distributed across the date range.

### Returns
An object containing:
- `daysExcludingFridays`: An array with the count of non-Friday working days for each month in the range.
- `daysWorkedExcludingFridays`: An array showing how many non-Friday working days were actually worked between the given start and end dates in each month.
- `monthlyTargets`: An array representing the target assigned to each month, proportional to the valid working days.
- `totalTarget`: The total calculated target based on the working days within the given range.

### Example of Usage
To use the function, you can call it as follows:

```javascript
console.log(calculateTotalTarget('2024-01-01', '2024-03-31', 5220));
Sample Output
The above example call would output an object similar to:

javascript
Copy code
{
    daysExcludingFridays: [27, 25, 26],
    daysWorkedExcludingFridays: [27, 25, 26],
    monthlyTargets: [435, 434.99999999999994, 435],
    totalTarget: 1305
}
Installation and Setup
Clone the repository to your local machine using:
bash
Copy code
git clone <repository-url>
Navigate to the project directory:
bash
Copy code
cd <project-directory>
Run the script using Node.js:
bash
Copy code
node targetCalculation.js
Assumptions
The input dates must be in the correct format (YYYY-MM-DD).
The function currently excludes only Fridays from the calculation.
The implementation does not consider public holidays or other non-working days besides Fridays.
Limitations
The code assumes that the input date range is valid and does not handle cases where the range starts and ends in the same month.
The function does not dynamically handle other non-working days besides Fridays, but this can be a future enhancement.
Contribution
If you wish to contribute to this project, please feel free to fork the repository, make your changes, and submit a pull request.

License
This project is licensed under the MIT License.
