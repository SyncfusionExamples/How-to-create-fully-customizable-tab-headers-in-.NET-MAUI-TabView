# How-to-create-fully-customizable-tab-headers-in-.NET-MAUI-TabView

A sample application that demonstrates how to create fully customizable tab headers in .NET MAUI TabView. You can customize header text, images, badges, alignment, fonts, colors, and even apply gradients or completely custom header layouts for a polished and professional UI.

## Prerequisites

* Visual Studio 2026 with .NET MAUI workload

## How to run this sample

1. Clone the repository.
2. Open the solution file `TabViewHeaderCustomization.sln` in Visual Studio 2026.
3. Build and run the project.

## Code Snippet

To achieve fully customizable tab headers, use the following XAML:

```xml
    <tabView:SfTabView x:Name="TabView" TabBarPlacement="Top"                            
    TabWidthMode="SizeToContent"  TabBarHeight="72"   IndicatorPlacement="Fill">
    <tabView:SfTabView.TabBarBackground>
        <LinearGradientBrush StartPoint="0,0" EndPoint="1,0">
            <GradientStop Color="#6A11CB" Offset="0.0" />
            <GradientStop Color="#2575FC" Offset="1.0" />
        </LinearGradientBrush>
    </tabView:SfTabView.TabBarBackground>

    <tabView:SfTabView.IndicatorBackground>
        <LinearGradientBrush StartPoint="0,0" EndPoint="0,1">
            <GradientStop Color="#FF512F" Offset="0.0" />
            <GradientStop Color="#DD2476" Offset="1.0" />
        </LinearGradientBrush>
    </tabView:SfTabView.IndicatorBackground>
    <tabView:SfTabView.IndicatorCornerRadius>8</tabView:SfTabView.IndicatorCornerRadius>
    <tabView:SfTabView.IndicatorStrokeThickness>0</tabView:SfTabView.IndicatorStrokeThickness>

    <tabView:SfTabView.HeaderHorizontalTextAlignment>Center</tabView:SfTabView.HeaderHorizontalTextAlignment>
    <tabView:SfTabItem Header="Home" ImageSource="dotnet_bot.png" ImagePosition="Left"                
                       ImageTextSpacing="8" TextColor="#FFFFFF" FontAttributes="Bold"
                       FontSize="14">
        <tabView:SfTabItem.Content>
            <Grid Padding="16">
                <Label Text="Welcome to the Home tab. Here you can find an overview of your application and quick access to essential features."
                           FontSize="16" TextColor="#222" LineBreakMode="WordWrap"/>
            </Grid>
        </tabView:SfTabItem.Content>
    </tabView:SfTabItem>

    <tabView:SfTabItem Header="Tasks" BadgeText="10" TextColor="#FFFFFF"
                        FontAttributes="Bold" FontSize="14">
        <tabView:SfTabItem.BadgeSettings >
            <core:BadgeSettings FontSize="15" Background="Violet" Type="None"/>
        </tabView:SfTabItem.BadgeSettings>
        <tabView:SfTabItem.Content>
            <Grid Padding="16">
                <Label Text="Manage your tasks efficiently. Add new tasks, track progress, and stay organized to meet your goals."
                           FontSize="16" TextColor="#222" LineBreakMode="WordWrap"/>
            </Grid>
        </tabView:SfTabItem.Content>
    </tabView:SfTabItem>

    <tabView:SfTabItem Header="Reports"  TextColor="#FFFFFF"
                        FontAttributes="Bold" FontSize="14">
        <tabView:SfTabItem.Content>
            <Grid Padding="16">
                <Label Text="View detailed reports and analytics. Gain insights into your performance and make informed decisions."
                           FontSize="16" TextColor="#222" LineBreakMode="WordWrap"/>
            </Grid>
        </tabView:SfTabItem.Content>
    </tabView:SfTabItem>
</tabView:SfTabView>
```

## Further references

* [TabBar Customization ](https://help.syncfusion.com/maui/tabview/tab-bar-customization)

