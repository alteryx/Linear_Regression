# Linear_Regression Workflow Tests



These tests were run at 2017-03-02 10:50:27



| id|name                         |status  |time           |message    |
|--:|:----------------------------|:-------|:--------------|:----------|
|  1|_4_Scatterplot               |&#9989; |16.596 seconds |           |
|  2|_8_Linear_Regression         |&#9989; |19.212 seconds |           |
|  3|BasicTest                    |&#9989; |12.946 seconds |2 warnings |
|  4|CVRegularizationTest1        |&#9989; |12.255 seconds |5 warnings |
|  5|CVRegularizationTest2        |&#9989; |12.539 seconds |5 warnings |
|  6|LinearTest1                  |&#9989; |9.042 seconds  |1 warning  |
|  7|LinearTest2                  |&#9989; |9.592 seconds  |3 warnings |
|  8|LinearTest3                  |&#9989; |9.367 seconds  |3 warnings |
|  9|LinearTestAll                |&#9989; |13.308 seconds |2 warnings |
| 10|LinearWithCVTest             |&#9989; |7.004 seconds  |3 warnings |
| 11|LinearWithCVTest2            |&#9989; |8.117 seconds  |3 warnings |
| 12|LinearWithCVTest3            |&#9989; |8.646 seconds  |3 warnings |
| 13|New Workflow3                |&#9989; |32.981 seconds |2 warnings |
| 14|RegularizationTest1          |&#9989; |19.358 seconds |3 warnings |
| 15|RegularizationTest2          |&#9989; |19.613 seconds |3 warnings |
| 16|RegularizationTest3          |&#9989; |17.166 seconds |3 warnings |
| 17|RegularizationTest4          |&#9989; |13.440 seconds |2 warnings |
| 18|RegularizationTest5          |&#9989; |14.741 seconds |3 warnings |
| 19|RegularizationTest6          |&#9989; |19.808 seconds |           |
| 20|Test_linear_w_integer_target |&#9989; |12.414 seconds |1 warning  |
| 21|TestScoreTool                |&#9989; |28.840 seconds |5 warnings |
| 22|TestScoreTool2               |&#9989; |15.243 seconds |3 warnings |
| 23|TestStepwise                 |&#9989; |34.566 seconds |2 warnings |
| 24|WeightedLinearWithCVTest     |&#9989; |14.186 seconds |3 warnings |


## UI Test Checklist.

1. Check that configuration persists. This includes widgets, tabs, pages, accordions, and pretty much any other ui element that the user interacts with. The configuration window should always.
2. Check navigation. This includes checking if pages show up correctly when the Customize/Back buttons are clicked. It is also important to check that persistence holds under these operations.
3. The `Customize` button should always appear.
4. Clicking on the `Customize` button should take the user to the second page.
5. Checking `Use a weighted variable ...` should bring up a dropdown to let the user select a weighting variable. This dropdown should be clearable. If the user checks this option, but does not select a weighting variable, then the workflow should display a configuration time error.
6. Checking the box in the upper left corner of the "Select the Predictor Variables" should check all the variables when checked for the first time on a fresh tool. Checking it again should uncheck all the variables.
7. A variable should show up under in the list of potential target variables if and only if it is a numeric type (double, Int, etc.).
8. All words should be spelled correctly. Additionally, no config text should end in punctuation, and all config options should be in sentence case.
9. The option to use regularized regression should not display if an XDF input is connected to the tool. Neither should the option to use cross-validation.
10. The config options `Enter value of alpha` `Standardize predictor variables` and `Use cross-validation to determine model parameters` should display if and only if regularization is selected.
11. If regularization is selected, `Standardize predictor variables` and `Use cross-validation to determine model parameters` should be selected by default. Additionally, the report generated should be the appropriate type depending on whether regularization is used.
12. If `Use cross-validation to determine model parameters` is selected, the options `Simpler model` and `Set seed` should be selected by default. The default value of the seed should be 1. Additionally, the cross-validation graphs should appear in the R report if cross-validation is selected (assuming Display graphs is checked.)
13. The options `Number of folds` `What type of model` and `Set seed` should display if and only if cross-validation with regularization is selected.
14. The slider under `Enter value of alpha` should prevent you from selecting a value less than 0 or greater than 1. If you type a value into the box or use the up/down widget to change the value of alpha, the slider should change its position accordingly.
15. `Use Cross-validation to determine estimates of model quality` should be unchecked by default. 
16. In the Cross-validation tab, `Number of folds`, `Number of trials`, and `Set seed` should appear if and only if cross-validation is selected. If CV is selected, `Set seed` should be checked by default, and the default value of the seed should be 1.
17. The default graph resolution should be 1x. The option `Display graphs` should display if and only if regularization is selected. If regularization is selected, `Display graphs` should be selected by default.
