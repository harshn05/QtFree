## Using Qt in a Closed-Source Project Without Paying a Fee

To use Qt in a closed-source project without paying a fee, you need to comply with the licensing terms of the open-source version of Qt. Here’s how you can do that:

### Use the LGPL Version of Qt
- Qt is available under the GNU Lesser General Public License (LGPL) version 3, which allows you to use it in proprietary applications under certain conditions.
- You can dynamically link your application to the Qt libraries. This means your application can call the Qt library, but the Qt library remains separate from your application.
- You must provide a way for users to replace or update the Qt libraries used by your application. This typically means providing the Qt libraries separately or linking to them dynamically.

### Comply with LGPL Requirements
- Any modifications you make to the Qt source code must be made available under the same LGPL license.
- You need to provide a copy of the LGPL license text with your application.
- If your application uses plugins or dynamically loads Qt libraries, users should be able to replace these libraries with their own versions of the Qt libraries.

### Avoid Static Linking
- Static linking of the Qt libraries into your application is not allowed under the LGPL unless you make your entire application open source under the LGPL.

### No Modifications to Qt
- If you do not modify the Qt library itself and only use it as is, you can keep your application closed-source while adhering to the LGPL conditions.

### Practical Steps to Use Qt under LGPL

1. **Download and Install Qt:**
   - Download the open-source version of Qt from the official Qt website.

2. **Configure Your Project:**
   - Set up your project to dynamically link to the Qt libraries. This is usually done in your project's build system (like CMake, qmake, etc.).

3. **Provide Necessary Information:**
   - Include the LGPL license text in your application’s documentation.
   - Provide instructions on how users can obtain and replace the Qt libraries used by your application.

4. **Distribute Qt Libraries:**
   - Distribute the unmodified Qt libraries alongside your application, or provide a clear link to where users can download the appropriate version of Qt.

### Qt Components to Avoid

To comply with the LGPL licensing requirements when using Qt in a closed-source project, you need to be cautious about using certain components of Qt that are licensed under the GPL (General Public License). The GPL has stricter requirements that would require your entire application to be open-sourced if you use GPL-licensed components. Here are some Qt components you should avoid:

1. **Qt Charts**
2. **Qt Data Visualization**
3. **Qt Virtual Keyboard**
4. **Qt Purchasing**
5. **Qt WebEngine**
6. **Qt for Device Creation**

These modules are typically licensed under GPL or commercial licenses and should be avoided unless you are willing to open-source your entire application or obtain a commercial license.

### Best Practices

- **Stick to LGPL Components:** Focus on using only the parts of Qt that are available under the LGPL. Core modules like `QtCore`, `QtGui`, `QtWidgets`, and other essential libraries are generally safe under LGPL.
- **Review Licensing Information:** Always check the specific licensing information for each Qt module you plan to use. The official Qt documentation provides clear licensing details for each component.
- **Dynamic Linking:** Ensure that you dynamically link to the Qt libraries to comply with the LGPL requirements. This allows users to replace the Qt libraries with their own versions if needed.
- **No Modifications:** Avoid modifying the Qt source code. If you do need to make modifications, be prepared to release those modifications under the same LGPL license.

By avoiding GPL-licensed components and adhering to the LGPL requirements, you can use Qt in your closed-source project without any licensing fees.

### List of Qt Modules Available Under LGPL:

1. **Qt Core** (`QtCore`)
2. **Qt GUI** (`QtGui`)
3. **Qt Widgets** (`QtWidgets`)
4. **Qt Network** (`QtNetwork`)
5. **Qt QML** (`QtQml`)
6. **Qt Quick** (`QtQuick`)
7. **Qt SQL** (`QtSql`)
8. **Qt Test** (`QtTest`)
9. **Qt XML** (`QtXml`)
10. **Qt Concurrent** (`QtConcurrent`)
11. **Qt DBus** (`QtDBus`)
12. **Qt Print Support** (`QtPrintSupport`)
13. **Qt Sensors** (`QtSensors`)
14. **Qt Serial Port** (`QtSerialPort`)
15. **Qt Multimedia** (`QtMultimedia`)
16. **Qt Multimedia Widgets** (`QtMultimediaWidgets`)
17. **Qt OpenGL** (`QtOpenGL`)
18. **Qt WebSockets** (`QtWebSockets`)
19. **Qt Positioning** (`QtPositioning`)
20. **Qt Bluetooth** (`QtBluetooth`)
21. **Qt NFC** (`QtNfc`)
22. **Qt Speech** (`QtSpeech`)
23. **Qt WebChannel** (`QtWebChannel`)
24. **Qt SVG** (`QtSvg`)
25. **Qt XML Patterns** (`QtXmlPatterns`)
26. **Qt Help** (`QtHelp`)
27. **Qt Quick Controls 2** (`QtQuickControls2`)
28. **Qt Remote Objects** (`QtRemoteObjects`)

### Notes:

- Some modules have both LGPL and GPL components, so ensure you are using only the LGPL parts if you need to comply with the LGPL licensing terms.
- Always refer to the official Qt documentation for the most up-to-date information on licensing. The licensing terms can change, and it's important to verify the current status of the modules you are using.

