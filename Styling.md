## Styling

Resource files can also define styling, these styles work off triggers and setters. 

 - Setters apply values to properties.
 
 - Triggers listen for conditions or changes in properties or events.


~~~xml
    <?xml version="1.0" encoding="utf-8" ?>
    <Resources xmlns:ns="Entropy" xmlns:ns1="MonoGame.Framework" xmlns:ns2="Entropy.UI">
        <Style Id="style0">
            
            <Setters>
                <Setter Property="Background" Value="@Properties/Tog_Button"/>
            </Setters>

            <Triggers>
                <Trigger Property="Toggled" Value="true">
                    <Setters>
                        <Setter Property="Background" Value="@Properties/Tog_ButtonPressed"/>
                    </Setters>
                </Trigger>

                <Trigger Property="Toggled" Value="false">
                    <Setters>
                        <Setter Property="Background" Value="@Properties/Tog_Button"/>
                    </Setters>
                </Trigger>
            </Triggers>

        </Style>
    </Resources> 
~~~
