# Entropy (Monogame Toolkit)
<h4>Entropy.UI</h4>

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

- [ ] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request

  ![Tux, the Linux mascot](/assets/images/tux.png)
