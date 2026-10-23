1. Your GitHub repository link (Step 3).

https://github.com/airasandigan flutter_basics_lab.git

2. The last three build() called lines from Activity 2.

        build() called: 4 glasses
        build() called: 5 glasses
        build() called: 6 glasses

3. Your observations from the experiments in Activities 2, 3 and 5.

        Activity 2: Observation

        When I moved _glasses++ outside setState() and tested the Add button without calling setState(), the glass count did not immediately update on the screen. The variable changed, but Flutter was not notified to rebuild the interface.

        Activity 3: Observation
        
        When I removed Expanded from one StatBox, the box no longer shared the available row width equally with the other boxes. It used its natural width instead, which could make the layout uneven or cause a horizontal overflow.

        Activity 5: Observation

        I changed the button corner radius from 8 to 20 using BorderRadius.circular(20). The buttons now have more rounded corners, giving the user interface a softer appearance.

4. Your answers to the ten review questions.

        1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each
        from this lab.

            - A StatelessWidget does not change its data, while a StatefulWidget can change when the user interacts with it. An example of a StatelessWidget is WeatherApp, and an example of a StatefulWidget is WaterTrackerPage.

        2. Why is a StatefulWidget written as two classes? What does each class do?

            - A StatefulWidget has two classes because they have different jobs. The first class creates the widget, while the State class stores the changing data and updates the screen.

        3. In Activity 2, what happened when you changed _glasses outside setState()? Why?

            - When I changed _glasses outside setState(), the number on the screen did not update immediately. This is because Flutter was not told to refresh the screen.

        4. Looking at the Debug Console in Activity 2, when is build() called?

            - The build() method is called when the screen is first displayed and when setState() is called to update the interface.

        5. Explain the main axis and the cross axis of a Row and of a Column.

            - In a Row, the main axis is horizontal and the cross axis is vertical. In a Column, the main axis is vertical and the cross axis is horizontal.

        6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?

            - When I removed Expanded from a StatBox, the boxes no longer shared the space equally. Expanded helps the boxes divide the available width equally.

        7. Why do we use GridView.builder for the menu instead of a Column with many children?

            - We use GridView.builder because it displays items in a grid and can scroll when there are many items. It is also more efficient than putting many items inside a Column.

        8. How do Stack and Positioned create the Best seller badge in Activity 4?

            - Stack allows widgets to overlap, while Positioned places the Best seller badge in a specific location on the menu card.

        9. What is the difference between customizing with ThemeData and with a style on one widget? Give
        one example of each from Activity 5.

            - ThemeData changes the style of widgets throughout the app, while a widget's own style changes only that widget. For example, elevatedButtonTheme styles the app's ElevatedButtons, while TextStyle can change the font size of one text.

        10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the
        change reach MaterialApp?

            - The _ThemeDemoAppState class holds the _isDark variable. When I switch dark mode on or off, setState() updates the value, and MaterialApp changes the app's theme.