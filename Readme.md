<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128534041/14.2.3%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E2050)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->

# Grid View for ASP.NET Web Forms - How to create command buttons with tooltips

Command buttons in [ASPxGridView](https://docs.devexpress.com/AspNet/DevExpress.Web.ASPxGridView) do not support tooltips. This example demonstrates how to emulate command buttons or custom buttons with HTML elements and provide tooltips for them (attribute `title`).

![](grid-custom-buttons-with-tooltip.png)

```aspx
<dx:GridViewDataTextColumn Name="Command" Caption="#" VisibleIndex="0">
    <DataItemTemplate>
        <a href = "javascript:grid.AddNewRow();" title="Add new row">New</a>
        <a href = "javascript:grid.StartEditRow('<%#Container.VisibleIndex%>');" title="Start edit row '<%#Container.VisibleIndex%>'">Edit</a>
        <a href = "javascript:grid.DeleteRow('<%#Container.VisibleIndex%>');" title="Delete row '<%#Container.VisibleIndex%>'">Delete</a>
        <a href = "javascript: alert ('This is the custom button');" title="Custom action">Custom action</a>
    </DataItemTemplate>
</dx:GridViewDataTextColumn>
```

## Files to Review

* [Default.aspx](./CS/WebSite/Default.aspx)
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs)
<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=asp-net-web-forms-grid-command-buttons-with-tooltips&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=asp-net-web-forms-grid-command-buttons-with-tooltips&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
