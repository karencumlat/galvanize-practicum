# ActionBar

## Unit Test

Test Filter and Sort Functions using Jest and React Testing Library

## Cypress Test

|        | Scenarios                                                                           |
| ------ | ----------------------------------------------------------------------------------- |
| 1      | Does the action bar render? (the filter, sort, and arrange columns buttons)         |
| **2**  | Do the sub-elements render? (buttons within the filter, sort, and arrange buttons). |
| 3      | When selecting add filter it should display goals and equals                        |
| **4**  | Should add new rows by selecting add filter                                         |
| 5      | When applying a filter it should filter the table                                   |
| **6**  | When applying a sort it should sort accordingly                                     |
| 7      | Under arrange columns, selecting hide all should hide all columns                   |
| **8**  | Under arrange columns, selecting show all should show all columns                   |
| 9      | Under arrange columns, moving the items should rearrange the table                  |
| **10** | Under arrange columns, typing in filter should filter the options.                  |
