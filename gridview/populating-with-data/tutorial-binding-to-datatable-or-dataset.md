---
title: Tutorial Binding to DataTable or DataSet
page_title: Tutorial Binding to DataTable or DataSet
description: Tutorial Binding to DataTable or DataSet
slug: gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset
tags: tutorial,binding,to,datatable,or,dataset
published: True
position: 5
---

# Tutorial: Binding to DataTable or DataSet



## 

The following tutorial demonstrates binding to a single database table. For information on binding to multiple tables see the [Binding to Hierarchical Data]({%slug gridview-hierarchical-grid-binding-to-hierarchical-data%}) topic.
        ![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 001](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset001.png)

1. Place a RadGridView component on a form. Set the Dock property to Fill.

1. In the Properties window locate the DataSource property and click the arrow to open the list. Select the __Add Project Data Source...__ link. *This step will display the Data Source Configuration Wizard.*![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 002](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset002.png)

1. In the Data Source Configuration Wizard __Choose a Data Source Type page__, select the __Database__ icon. Click the __Next__ button.
            ![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 003](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset003.png)

1. In the Choose Your data Connection page click the __New Connection...__ button. *This step will display the Add Connection dialog.*![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 004](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset004.png)

1. In the Add Connection dialog click the __Change...__ button. *This step will display the Change Data Source dialog.*![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 005](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset005.png)

1. Select the __Microsoft Access Database File__ data source. Click the __OK__ button to close the Change Data Source dialog.
            ![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 006](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset006.png)

1. The Add Connection dialog will appear. Click the Database File Name __Browse__button and locate the "NWind.mdb" file from the Telerik UI for WinForms directory in the "\Examples\DataSources" directory.  Click the __OK__button to close the Add Connection dialog.
            

1. In the Choose Your Database Objects page, select the __"Categories"__ checkbox. Click the __Finish__ button to close the Data Source Configuration Wizard.
            ![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 007](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset007.png)

1. In the Visual Studio Properties window for the grid __DataSource__ property select the __"Categories"__ table. *This step will create DataSet, BindingSource and TableAdapter objects for the categories table.*![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 008](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset008.png)

1. The project design should look something like the screenshot below. Note the new data components in the component tray under the design surface.![gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset 009](images/gridview-populating-with-data-tutorial-binding-to-datatable-or-dataset009.png)

1. Replace the Form_Load event handler with the following code. *The "foreach" code iterates all the columns in the grid and calls BestFit() so that the columns will expand to show the data.*

#### __[C#] Best fit columns__

{{region bestFitColumns}}
	        private void TutorialBindingToDataTableOrDataSet_Load(object sender, EventArgs e)
	        {
	            this.categoriesTableAdapter.Fill(this.nwindDataSet.Categories);
	            foreach (GridViewDataColumn column in radGridView1.Columns)
	            {
	                column.BestFit();
	            }
	        }
	{{endregion}}



#### __[VB.NET] Best fit columns__

{{region bestFitColumns}}
	    Private Sub TutorialBindingToDataTableOrDataSet_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load
	        Me.CategoriesTableAdapter.Fill(Me.NwindDataSet.Categories)
	        For Each column As GridViewDataColumn In RadGridView1.Columns
	            column.BestFit()
	        Next
	    End Sub
	{{endregion}}



1. Press __F5__ to run the application.
            