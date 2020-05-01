# DataGrid

## Scenarios

- should display column or cell
  - should have sticky header
- should display data
- should have a11yText if customText exist
- should have sticky column
- should put focus cell on autofocus
- should not focus cell if autofocus is false
- should render column indicator (on hover)
- should render column expand (on hover)
- _should open side panel_
- should scroll to the bottom
- should lode more data
- should infinite scroll
- should use arrow keys to focus
- _collapse (extra)_

## DataGrid Test Task

|       | Tool | Description                                                                              |
| ----- | ---- | ---------------------------------------------------------------------------------------- |
| 1\*   | S    | Does the table, columns, headers and cell render/display                                 |
| 2     | S    | Does the data display inside the cells                                                   |
| 3 \*  | J    | Does custom cell content work                                                            |
| 4     | S    | Do customs styles display                                                                |
| 5\*   | S    | Does isSticky create a new sticky header                                                 |
| 6     | C    | Does focus cell apply autofocus correctly                                                |
| 7 \*  | C    | Does the table include the indicator and/or expandable when added and on hover           |
| 8     | C    | Does the table accept callback functions and execute them properly (ex: alerts on click) |
| 9 \*  | C    | Does the show more button display when you scroll to the bottom of the table             |
| 10    | C    | Does infinity scroll display more content when scrolled to the desired row               |
| 11 \* | C    | Do the arrow keys change focus on proper cells                                           |
| 12    | J    | Does content not show when the table cell is collapsed                                   |
| 13    | J    | Does content show when the table cell is expanded                                        |
| 14 \* | C    | Does the collapsible cell function properly with key commands (arrows and enter)         |
