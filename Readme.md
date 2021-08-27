<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128534041/14.2.3%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E2050)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [MyException.cs](./CS/WebSite/App_Code/MyException.cs)
* [Default.aspx](./CS/WebSite/Default.aspx)
* [Default.aspx.cs](./CS/WebSite/Default.aspx.cs)
<!-- default file list end -->
# ASPxGridView - How to emulate custom and action buttons with tooltips
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e2050/)**
<!-- run online end -->


<p>While this functionality is not available out of the box, it is possible to emulate command buttons with HTML element and assign tooltips using default HTML approach (attribute <strong>title</strong>).<br><br>In this example, we created a Data Item Template inside the command column:</p>


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



<br/>


