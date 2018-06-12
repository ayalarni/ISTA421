# C# Chapter25 Pages601-650

## Norma I. Ayala-Rosa

1. What is the purpose of the Universal Windows Platform?
The purpose of this platform is to help develop universal apps that run on Windows 10, Windows 10 Mobile, Xbox One and HoloLens without the need to be re-written for each.

What was the name of the predecessor to UWP? It was Windows Run Time 8x.

2. Describe in detail how the lifetime of a UWP app differs from a traditional desktop application.
The lifetime of a UWP app is somewhat different from that of a traditional desktop app.  One should design apps that can run on devices such as smartphones to suspend execution when the user switches focus to another app and then to resume running when the focus returns.  This approach can help to conserve resources and battery life on a constrained device. Windows might actually decide to close a suspended app if determines that it needs to release system resources such as memory.  When the app next runs, it should be able to resume where it left off.  This means that one need to be prepared to manage app state information in the code, save it to hard disk, and restore it at the appropriate juncture. 

3. Describe two ways you can set and modify the properties of controls.
Under Customers app, the UI breaks down into two main areas: a heading containing the title and the body containing the customers' details.  Allowing for some spacing between these areas and a margin at the bottom of the form, one can assign relative sizes to each of these areas. 

4. Describe the two layout schemes of UWP apps that we constructed in class.
The <Grid.RowDefinitions> section defines the rows for the grid.
ListView and GridView controls manage how their items are arranged (horizontal, vertical, wrapping, etc…) and how a user interacts with the items, but not how the individual items are shown on the screen. Item visualization is managed by item containers. When you add items to a list view they are automatically placed in a container.

5. Describe three ways you can use the Visual State Manager to adapt the layout of UWP apps.
 a. One can create several versions of the MainPage.xaml file, one for each device family.

 b. One can use the Visual State Manager to modify the layout of the page at run time.

 c. One can use the Visual State Manager to switch between views based on the height and width of the window.

6. Describe how you can modify multiple properties of multiple controls with one document.
These container controls consist of two important parts that combine to create the final visuals shown for an item: the data template and the control template.
    Data template - You assign a DataTemplate to the ItemTemplate property of the list view to specify how individual data items are shown.
    Control template - The control template provides the part of the item visualization that the framework is responsible for, like visual states. You can use the ItemContainerStyle property to modify the control template. Typically, you do this to modify the list view colors to match your branding, or change how selected items are shown.

How do you connect this modification document with your UWP application?
Universal Windows Apps (apps) can access certain file system locations by default. Apps can also access additional locations through the file picker, or by declaring capabilities.
