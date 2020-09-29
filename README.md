# Entropy (Monogame Extension)

## Entropy.UI

The Entropy.UI library is a work in progress user interface (UI) codebase for the Monogame framework.  

- [Getting Started](/GettingStarted.md)
- [Styling](/Styling.md)
- [Xml Serialization](/Xml.md)
- [Layouts](/GettingStarted.md)
- [Text](/GettingStarted.md)
- [Binding](/GettingStarted.md)


## Prerequisites

- Monogame.Framework
- Entropy.Core

## License

- MIT License

## Contact

Email: Hamish.Moulder@Outlook.com


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




