# How-to-create-fully-customizable-tab-headers-in-.NET-MAUI-TabView

A sample application that demonstrates how to create fully customizable tab headers in .NET MAUI TabView. You can customize header text, images, border, alignment, fonts, colors or completely custom header layouts for a polished and professional UI.

In the example below, we demonstrate:

 1. Visual state customization: Using `VisualStateManager` to dynamically change the header text color of each `SfTabItem` based on selection state.
 2. Icon color binding: Applying FontImageSource to each ImageSource property in `SfTabItem   and binding its color to the tab’s TextColor for consistent styling.
 3. Border styling: Customizing the tab header area’s border using properties such as `TabBarBorderColor`, `TabBarBorderThickness`, and `TabBarCornerRadius`.
 4. Indicator and layout settings: Adjusting `IndicatorPlacement`, `IndicatorBackground`, and `TabBarHeight` for a modern look.

## Prerequisites

* Visual Studio 2026 with .NET MAUI workload

## How to run this sample

1. Clone the repository.
2. Open the solution file `TabViewHeaderCustomization.sln` in Visual Studio 2026.
3. Build and run the project.

## Code Snippet

To achieve fully customizable tab headers, use the following XAML:

```xml
     <ContentPage.Resources>
    <Style TargetType="tabView:SfTabItem">
        <Setter Property="VisualStateManager.VisualStateGroups">
            <VisualStateGroupList>
                <VisualStateGroup>
                    <VisualState x:Name="NormalFilled" >
                        <VisualState.Setters>
                            <Setter Property="TextColor" Value="#111111" />
                        </VisualState.Setters>
                    </VisualState>
                    <VisualState x:Name="SelectedFilled">
                        <VisualState.Setters>
                            <Setter Property="TextColor" Value="#FFFFFF" />
                        </VisualState.Setters>
                    </VisualState>
                </VisualStateGroup>
            </VisualStateGroupList>
        </Setter>
    </Style>
</ContentPage.Resources>

<tabView:SfTabView x:Name="tabView" IndicatorBackground="SkyBlue" IndicatorPlacement="Fill" TabBarHeight="60" TabBarBackground="Transparent"  TabBarBorderColor="#6A11CB" TabBarBorderThickness="3" Margin="10" TabBarCornerRadius="15" >
    <tabView:SfTabView.Items>
        <tabView:SfTabItem Header="Call" x:Name="callItem"
                       ImagePosition="Left">
            <tabView:SfTabItem.ImageSource>
                <FontImageSource Glyph="ﺶ" x:Name="call"
                               Color="{Binding Source={x:Reference callItem},Path=TextColor}"
                           FontFamily="MaterialDesignIcons"/>
            </tabView:SfTabItem.ImageSource>
            <Grid Padding="16">
                <Label Text="Make and manage calls. View recent calls, dial new numbers, and quickly start a call from your contacts."
          FontSize="16" TextColor="#222" LineBreakMode="WordWrap"/>
            </Grid>
        </tabView:SfTabItem>

        <tabView:SfTabItem Header="Favourite" x:Name="favItem"
                       ImagePosition="Left">
            <tabView:SfTabItem.ImageSource>
                <FontImageSource Glyph="" x:Name="fav"
                           Color="{Binding Source={x:Reference favItem},Path=TextColor}"
                           FontFamily="MaterialDesignIcons"/>
            </tabView:SfTabItem.ImageSource>
            <Grid Padding="16">
                <Label Text="Your favorite contacts and shortcuts. Pin people you reach often for one‑tap calling or messaging."
          FontSize="16" TextColor="#222" LineBreakMode="WordWrap"/>
            </Grid>
        </tabView:SfTabItem>

        <tabView:SfTabItem Header="Contacts" x:Name="contactsItem"
                       ImagePosition="Left">
            <tabView:SfTabItem.ImageSource>
                <FontImageSource Glyph="" x:Name="contacts"
                           Color="{Binding Source={x:Reference contactsItem},Path=TextColor}"
                           FontFamily="MaterialDesignIcons"/>
            </tabView:SfTabItem.ImageSource>
            <Grid Padding="16">
                <Label Text="Browse and manage your contacts. Search, view details, and quickly add or edit entries in your address book."
          FontSize="16" TextColor="#222" LineBreakMode="WordWrap"/>
            </Grid>
        </tabView:SfTabItem>
    </tabView:SfTabView.Items>
</tabView:SfTabView>
```

## Further references

* [TabBar Customization ](https://help.syncfusion.com/maui/tabview/tab-bar-customization)

