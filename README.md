# Entropy (Monogame Extension)

## Entropy.UI

The Entropy.UI library is a work in progress user interface (UI) codebase for the Monogame framework.  

~~~csharp
    public class MenuContext : UIContext
    {
        LinearLayout layout0 = new LinearLayout(){
            Padding = "0,0,8,4",
            Spacing = 10,
            Orientation = Orientation.Vertical,
            Anchor = Alignment.VCenter | Alignment.HCenter,
        };
        
        Button button0 = new Button() { Content = "btn0" };
        Button button1 = new Button() { Content = "btn1" };
        Button button2 = new Button() { Content = "btn2" };
        
        layout0.Add(button0, button1, button2)
        
        AddView(layout0);
    }
~~~

Or Xml Equivalent

~~~xml
    <!--Object Tree-->
    <LinearLayout Padding="0,0,8,4" Anchor="VCenter,HCenter" Orientation="Vertical">
        <Button Content="btn0"/>
        <Button Content="btn1"/>
        <Button Content="btn2"/>
    </LinearLayout>
~~~

 ![Tux, the Linux mascot](Layout0.PNG=100x20)

## Resources 

Resource files are any xml file that uses the 'Resources Token', 
namespaces for types, must be included so the xml parser can translate and create objects.

There are two types of resources:

- Value defined resources.
   
   -Simple objects like primitive data types (int, bool) or any data type that can be represented in the form of a single string. 
    The codebase provides support for creating Attribute Encoders and Decoders for custom classes to use value defined resourcing.  

- Property defined resources.
    
    -Complex objects with attributes, that are defined using xml attributes only.

<i>Resource file example:</i>
~~~xml
    <?xml version="1.0" encoding="utf-8" ?>

    <!--Main Token, with all included namespaces-->
    <Resources xmlns:ns="Entropy" xmlns:ns1="MonoGame.Framework" xmlns:ns2="Entropy.UI">
        
        <!--Value defined-->
        <String Id="btn_play_Name" Value="Play"/>
        <USize Id="btn_size0" Value="34"/>
        
        <!--Property defined-->
        <Thickness Id="btn_title_margin" Value="5"/>
        <NinePatchRegion Id="Tog_Button" Texture="Textures/sheet0" X ="0" Y="0" Width="32" Height="32" Padding="2"/>
        <NinePatchRegion Id="Tog_ButtonPressed" Texture="Textures/sheet0" X="0" Y="32" Width="32" Height="32" Padding="1"/>

    </Resources>
~~~


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


- [ ] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request

  ![Tux, the Linux mascot](/assets/images/tux.png)
