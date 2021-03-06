---
title: Masked Input Column
page_title: Masked Input Column
description: Masked Input Column
slug: radgridview-columns-column-types-masked-input-column
tags: masked,input,column
published: True
position: 12
---

# Masked Input Column


__GridViewMaskedInputColumn__ derives from the __GridViewBoundColumnBase__, which means that it inherits all of the functionality too. In edit mode every field of the column will be represented by a  [RadMaskedInput]({%slug radmaskedinput-overview%}) control depending on what __MaskType__ is set, unless a __CellEditTemplate__ is defined for the column.
        

This is a list with short descriptions of the editors which will be created based on MaskType property setting:
        

* __MaskType="Standard"__ - the __RadMaskedTextInput__ control, supports restriction of the user input to customized text formats. [Read more ]({%slug radmaskedinput-features-controls-text%})

* __MaskType="DateTime"__ - the __RadMaskedDateTimeInput__ control, ensures that the date entered by the user is verified and accurate. [Read more ]({%slug radmaskedinput-features-controls-datetime%})

* __MaskType="Numeric"__ - the __RadMaskedNumericInput__ controls supports restricting the user input to decimal, fixed-point, percent and currency values, where currency values are also culture sensitive. [Read more ]({%slug radmaskedinput-features-controls-numeric%})

* __MaskType="Currency"__ -the __RadMaskedCurrencyInput__ control allows broad customization of culture-aware currency values. [Read more]({%slug radmaskedinput-features-controls-currency%})

For example add a __GridViewMaskedInputColumn__ that represents the OrderNumber for an Order object. The OrderNumber should not be more than 7 symbols. As it allows both text and digits use the __Standard MaskType__ and set "SO#####" as __Mask__.
        

__Example 1: Define a GridViewMaskedInputColumn:__

#### __XAML__

{{region radgridview-columns-column-types-masked-input-column_0}}

	<telerik:RadGridView x:Name="radGridView"
	         AutoGenerateColumns="False">
	    <telerik:RadGridView.Columns>
	        <telerik:GridViewMaskedInputColumn 
				DataMemberBinding="{Binding OrderNO}" 
				Header="Order No."
				UniqueName="OrederNo"
				MaskType="Standard"
				Mask="SO#####"/>
	    </telerik:RadGridView.Columns>
	</telerik:RadGridView>
{{endregion}}


# See Also
* [RadMaskedInput Overview]({%slug radmaskedinput-overview%})
* [How to migrate from the RadMaskedTextBox to the RadMaskedInput]({%slug radmaskedinput-migrating%})
