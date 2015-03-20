---
title: GridViewImageColumn
page_title: GridViewImageColumn
description: GridViewImageColumn
slug: gridview-columns-gridviewimagecolumn
tags: gridviewimagecolumn
published: True
position: 11
---

# GridViewImageColumn



__GridViewImageColumn__ displays *read-only* images for database columns of image data (OLE container or BLOB). 

>RadGridView tries to convert data columns that contain unspecified binary data to an image.

>Some databases such as Access use OLE image container. RadGridView automatically recognizes that and skips the added header. 

Supported image formats are those supported by the Image class of .net framework. 



![gridview-columns-gridviewimagecolumn 001](images/gridview-columns-gridviewimagecolumn001.png)

#### __[C#] Adding GridViewImageColumn__

{{region addImageColumn}}
	            GridViewImageColumn imageColumn = new GridViewImageColumn();
	            imageColumn.Name = "ImageColumn";
	            imageColumn.FieldName = "Photo";
	            imageColumn.HeaderText = "Picture";
	            imageColumn.ImageLayout = ImageLayout.Zoom;           
	            radGridView1.MasterTemplate.Columns.Insert(4, imageColumn);
	{{endregion}}



#### __[VB.NET] Adding GridViewImageColumn__

{{region addImageColumn}}
	        Dim imageColumn As New GridViewImageColumn
	        imageColumn.Name = "ImageColumn"
	        imageColumn.FieldName = "Photo"
	        imageColumn.HeaderText = "Picture"
	        imageColumn.ImageLayout = ImageLayout.Zoom
	        RadGridView1.MasterTemplate.Columns.Add(imageColumn)
	{{endregion}}



## Image Layout

GridViewImageColumn also implements resizing functionality where sizing is controlled by the __ImageLayout__ property. __ImageLayout__can be set to one of the following: None, Tile, Center, Stretch and Zoom:

* __None__ - Image is positioned at the upper left corner of the cell. This value can be used in a combination
  with the value of the ImageAlignment property to specify the position of an image in a cell:
  
  ![gridview-columns-gridviewimagecolumn 002](images/gridview-columns-gridviewimagecolumn002.png)

#### __[C#]__

{{region none}}
	            imageColumn.ImageLayout = ImageLayout.None;
	            imageColumn.ImageAlignment = ContentAlignment.BottomRight;
	{{endregion}}



#### __[VB.NET]__

{{region none}}
	        imageColumn.ImageLayout = ImageLayout.None
	        imageColumn.ImageAlignment = ContentAlignment.BottomRight
	{{endregion}}



* __Tile__ - Image is repeated:
 ![gridview-columns-gridviewimagecolumn 003](images/gridview-columns-gridviewimagecolumn003.png)

#### __[C#]__

{{region tile}}
	            imageColumn.ImageLayout = ImageLayout.Tile;
	{{endregion}}



#### __[VB.NET]__

{{region tile}}
	        imageColumn.ImageLayout = ImageLayout.Tile
	{{endregion}}



* __Center__ - Image is positioned at the cell center regardless of the ImageAlignment value:
    ![gridview-columns-gridviewimagecolumn 004](images/gridview-columns-gridviewimagecolumn004.png)

#### __[C#]__

{{region center}}
	            imageColumn.ImageLayout = ImageLayout.Center;
	{{endregion}}



#### __[VB.NET]__

{{region center}}
	        imageColumn.ImageLayout = ImageLayout.Center
	{{endregion}}



* __Stretch__ - Image is stretched in the cell:
  ![gridview-columns-gridviewimagecolumn 005](images/gridview-columns-gridviewimagecolumn005.png)

#### __[C#]__

{{region stretch}}
	            imageColumn.ImageLayout = ImageLayout.Stretch;
	{{endregion}}



#### __[VB.NET]__

{{region stretch}}
	        imageColumn.ImageLayout = ImageLayout.Stretch
	{{endregion}}



* __Zoom__ - Image is zoomed but the aspect ratio is preserved:
    ![gridview-columns-gridviewimagecolumn 006](images/gridview-columns-gridviewimagecolumn006.png)

#### __[C#]__

{{region zoom}}
	            imageColumn.ImageLayout = ImageLayout.Zoom;
	{{endregion}}



#### __[VB.NET]__

{{region zoom}}
	        imageColumn.ImageLayout = ImageLayout.Zoom
	{{endregion}}

