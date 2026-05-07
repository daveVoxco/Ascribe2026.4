---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-illustrator/current-filter-management
---

# Current Filter Management

![](https://static.goascribe.com/Help/Current_Filter_Management.gif)

Illustrator is very interactive, and filtering plays a big role in that. The filtering allows you to view the data in different ways. The visualizations contain data points, which represent codes (or in the case of word clouds, words.) You can filter by any data point.

When you click a data point in a chart or a table, that data point becomes a filter. It applies to all visualizations on all canvases in the illustration, except for visualizations marked as not filterable. (The filterable option is in the Options area for every visualization.)

When a filter is applied, the sample size is updated and displayed with a yellow background.

## Apply a Single Filter

To apply a single filter, click on any data point in a table or chart. For example, add a bar chart for a closed-ended question, and click on one of the bars in the chart.

![](https://static.goascribe.com/Help/Close-ended_question_as_bar_chart.gif)

![](https://static.goascribe.com/Help/Single_filter_applied.gif)

## Remove Filter

There are several ways to remove a filter. You can click the data point used as the filter, and that removes it. Or you can click the Remove Filter button in the toolbar.

## Apply Multiple Filters

To apply multiple filters, first apply one filter. The Filter Logic drop-down is enabled, and you can change it. After you change the Filter Logic drop-down, click another data point in a visualization to add it as a filter.

Here are the Filter Logic options:

<table><thead><tr><th width="193.333251953125" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">One</td><td valign="top">Only 1 filter is applied at a time</td></tr><tr><td valign="top">Or</td><td valign="top">When selected and multiple filters are used, the visualizations display data that meet any of the filters.</td></tr><tr><td valign="top">And</td><td valign="top">When selected and multiple filters are used, the visualizations display data that meet all of the filters.</td></tr></tbody></table>

To view the filters, click the Current Filter drop-down.

## Reverse Filter

If you want to see the reverse of the current filter, unselect the checkbox to the left of the Filter Logic drop-down. That action displays the data which is not included in the current filter.

## Manipulating Filters

Once you have created a filter, you can use these buttons to change filters:

<table><thead><tr><th width="211.333251953125" align="center" valign="top">Option</th><th valign="top">Description</th></tr></thead><tbody><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Remove_filter_button_illustration.gif" alt=""> <br>Remove All Filters</td><td valign="top">Removes all filters and redraws the visualizations.</td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Previous_filter_illustration.gif" alt=""> <br>Previous Filter</td><td valign="top"><p>Resets the filters to the last filter or filters applied. For example, if you have 3 filters applied and you click Previous Filter, it removes the 3rd filter and redraws the visualizations according to the remaining filters.</p><p> </p><p>If you only have 1 filter applied, Previous Filter will remove it.</p><p> </p><p>Only useful if you have applied a filter or filters during your current Illustrator session.</p></td></tr><tr><td align="center" valign="top"><img src="https://static.goascribe.com/Help/Next_filter_illustration.gif" alt=""> <br>Next Filter</td><td valign="top">Only useful if you have applied a filter or filters and removed them during your current Illustrator session. For example, if you apply multiple filters and then remove a filter, Next Filter reapplies the removed filter and redraws the visualizations.</td></tr></tbody></table>

## Illustration-Level Filters are not Saved

When you apply filters using individual data points, these are considered illustration-level filters. They are not saved to the illustration, but allow for interactive filtering. (The filters are saved for use in Code Drivers and Question Drivers.) For saved filters, see [Saved Filter Management](saved-filter-management.md).
