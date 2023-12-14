# How-to-apply-style-to-the-.NET-MAUI-Badge-View-control
This section is explains how to apply style to the .NET MAUI Badge View control

#   Getting Started with .NET MAUI Badge View (SfBadgeView)

## Adding a SfBadgeView reference
The Syncfusion .NET MAUI controls are available in Nuget.org. To add SfBadgeView to your project, open the NuGet package manager in Visual Studio, search for Syncfusion.Maui.Core and then install it.

##  Adding a namespace
Add the following namespace to add .NET MAUI Badge Notifications.

**XAML**

```
xmlns:badge="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"
```
## Initializing a badge view
Create an instance for the Badge View control, and add it as content.

**XAML**

```
<badge:SfBadgeView>        
    <badge:SfBadgeView BadgeText="20" />          
</badge:SfBadgeView>
```

**C#**

```
SfBadgeView sfBadgeView = new SfBadgeView();
sfBadgeView.BadgeText = "20";
this.Content = sfBadgeView;
```

#   Apply style to the .NET MAUI Badge View control

**XAML**
```
<ContentPage.Resources>
     <Style TargetType="core:SfBadgeView" x:Key="badgeView" >
         <Setter Property="BadgeText">New User</Setter>
         <Setter Property="BadgeSettings">
             <Setter.Value>
                 <core:BadgeSettings Position="TopRight"                                      
                                      CornerRadius="5"
                                      Offset="-15,-8"
                                      Type="None" 
                                      BadgeAlignment="Start" />
             </Setter.Value>
         </Setter>
     </Style>
 </ContentPage.Resources>

 <Grid>
    <core:SfBadgeView HorizontalOptions="Center"
                      VerticalOptions="Center"
                      Style="{StaticResource badgeView}">
        <core:SfBadgeView.Content>
            <Image  Source="People_Circle1.png"
                    VerticalOptions="Center"
                    HorizontalOptions="Center"
                    HeightRequest="100"
                    WidthRequest="100"/>
        </core:SfBadgeView.Content>
    </core:SfBadgeView>
</Grid>

```

## How to run this application?

To run this application, you need to first clone the How-to-apply-style-to-the-.NET-MAUI-Badge-View-control repository and then open it in Visual Studio 2022. Now, simply build and run your project to view the output.

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## License

Syncfusion has no liability for any damage or consequence that may arise by using or viewing the samples. The samples are for demonstrative purposes, and if you choose to use or access the samples, you agree to not hold Syncfusion liable, in any form, for any damage that is related to use, for accessing, or viewing the samples. By accessing, viewing, or seeing the samples, you acknowledge and agree Syncfusion’s samples will not allow you seek injunctive relief in any form for any claim related to the sample. If you do not agree to this, do not view, access, utilize, or otherwise do anything with Syncfusion’s samples.