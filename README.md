# Entropy (Monogame Toolkit)
<h4>Entropy.UI</h4>

The Entropy.UI library is a work in progress user interface (UI) codebase for the Monogame framework.  

~~~csharp
    public class MenuContext : UIContext
    {
        LinearLayout layout0 = new LinearLayout(){
            Padding = "0,0,8,4",
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
    <LinearLayout Padding="0,0,8,4" Anchor = "VCenter,HCenter" Orientation ="Vertical">
        <Button Content="btn0"/>
        <Button Content="btn1"/>
        <Button Content="btn2"/>
    </LinearLayout>
~~~

Styling
~~~xml
    <?xml version="1.0" encoding="utf-8" ?>
    <Resources xmlns:ns = "Entropy" xmlns:ns1 = "MonoGame.Framework" xmlns:ns2 = "Entropy.UI">
        <Style Id = "style0">
            
            <Setters>
                <Setter Property ="Background" Value ="@Properties/Tog_Button"/>
            </Setters>

            <Triggers>
                <Trigger Property = "Toggled" Value ="true">
                    <Setters>
                        <Setter Property ="Background" Value ="@Properties/Tog_ButtonPressed"/>
                    </Setters>
                </Trigger>

                <Trigger Property = "Toggled" Value ="false">
                    <Setters>
                        <Setter Property ="Background" Value ="@Properties/Tog_Button"/>
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
