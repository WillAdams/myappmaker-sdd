
[← back to README/table of contents](README.md)


# Usage and basic design

After learning about what myappmaker is supposed to be, as well as its requirements and design challenges, we can finally learn about its usage and basic design.

It is important to note that we are at an early stage in myappmaker's design and as such its ultimate design is expected to change, specially once its development starts. On top of the usual reasons for this, like the fact that only by implementing the design we'll be able to test and refine it, there is also another important reason: because of the immense challenge that the very nature of the app poses, that is, an app builder. We visited that notion deeply on the previous chapter.

This chapter is divided into 02 main sections, the first presenting more or less how an usage session would be, and the second presenting the basic design of the app.

Making an app is already difficult. Making an app that makes other apps adds even more complexity to the problem. As such, in our first attempts to learn about effective and intuitive ways to design interfaces for our users, we'll take inspiration from other software projects that are doing similar things, hoping to be able to adapt strategies, designs and features to app building. Some of these software projects are game engines or 3D design software (given the high number of entities and workflows they manage to coordinate) and other app builders (and similar projects) already mentioned, like HyperCard and Qt Designer. As mentioned briefly in a previous chapter, a game engine like Godot is in fact so versatile that it is used by many business/developers to make apps.



## myappmaker usage


### Main elements and their layout

By this point, we learned about myappmaker definition, its requirements and nice-to-haves and also about its design challenges. Now it is time to define how users will interact with the app. How does all this information defines its usage? Given all the possibilities and attempts at making app builder tools throughout history, how does myappmaker intends to be different?

The solution is in exploring different approaches to app building. As we mentioned in the previous section, people using myappmaker will have at their disposal a drag-and-drop interface and also a block coding interface. The block coding interface however will only brought into view when editing the behaviour of the elements laid down on the canvas. That is, before worrying about their behaviour, users will think about the elements per se and how they'll be placed.

Similarly to game engines and 3D design tools, an app builder app requires the designer to deal with a lot of complexity, innumerable entities and various tasks/workflows. It is only natural them that an app builder must offer many different tasks/workflows. For that end, myappmaker will make available to users several different panels/interfaces that the user can access at different points in time and different stages of their app building session. The user will be able to close such panels, bring them back into view or collapse them (and expand them back into view again at a later time).

We'll have panels...

- representing a view of the app (a canvas), where users will lay and organize widgets
- containing several widgets so users can drag them into the canvas
- containing layouts that can be applied to the widgets laid out on the canvas
- for block coding where users can edit the behaviours of the widgets and the app

And many others.

Our challenge is to present all of this to the user in an intuitive way that doesn't scare the user away.

Despite the several panels/interfaces available to users, when launching the app for the first time, users must only see the most basic interfaces that still must be enough to start working right away. We'll start by presenting 03 main panels/areas: the canvas in the center, occupying almost all the available space, where the elements of the app will be laid, and 02 (two) panels in the shape of columns positioned at each side on the canvas, one for picking widgets (to the left) and another for picking layouts (to the right) with which to organize the widgets.

The panel holdings elements to the left (in the case of myappmaker, widgets) is present in many other software of all kinds. Raster and vector image editors like Photoshop, Inkscape and GIMP use a similar layout. Unreal Engine's Blueprint (a node editor) also uses this layout. Qt Designer also offers a similar layout. It allows users to start working right away by placing elements onto the canvas. The same way a physical palette holds colors with which an artist can paint, that panel will hold widgets with which the user can populate its application.

The panel to the right will complement the one to the left, by providing layouts with which to organize/align widgets laid on the canvas.

In other words, the canvas will be the most prominent and important work space for the users. All other panels/windows will be invoked and used as needed.

As discussed previously on the challenges of picking the main organizing elements for an app (frames/cards/pages/etc.), such main element will be a static element like frames/cards/etc., but that we'll call **views**. Only once we gather enough experience and feedback from users over time we'll think about adopting a concept closer to what we present previously as the **context**.

Throughout human history, many complex crafts were thought to people with no formal education or training, so in theory there must be possible to teach people the "craft" of app making without complex lingo, interfaces and workflows. It all hangs on our ability to divide complex tasks into simple steps and complex know-how/rules into intuitive and foolproof interfaces.


### Template-based layouts

Once presented with the canvas and other panels in order to start working, the user can start laying the widgets freely on the canvas and then choose layouts with which to organize them.

In addition to that, I'd also like to offer a template system, in order to speed up the layout process. Templates are used in several software projects, app builders or not, and are very handy for both beginner and experienced users, since they simplify the work of laying elements for common, frequently used representations.

For instance, in many different kinds of software, including pages on the web, the "form" format is used frequently, that is, elements organized as a document with several spaces where users can insert information. In fact, many applications consist of a single form where the user can insert all the info needed to carry out an specific operation and be done with it.


### Avoid the lifeless blank screen

On top of displaying simple interfaces on launch to users, myappmaker will also always load a default document already populated with elements and other basic info. This is actually seen in many other software as well. On launch, MS Word can already receive text typed by the user. Blender 3D already opens with a default document loaded containing basic shapes and elements.

This allows users to "play" with the software right away. Rather than fearing the next step when presented with a blank lifeless interface, the user is thrown in a lively system already populated with basic elements. From there it is easier to play with the visible elements, see how one can interact with them, add more elements or delete the existing ones, etc.

It is all about providing the user with the "app making" experience right away, rather than hiding it behind complex settings that the user have to overcome before being able to start making their apps. Users should not be afraid to experiment or have to spend time assuming how something works.


### Adding logic/behaviour

Once the elements are added and properly laid out on the canvas, the user can finally give them life by adding logic/behaviour to them by bringing up the proper interfaces. The main one will be a block coding interface where the user will be able to access the elements on the app.

Although a separate project, I also intend to add a dedicated fork of Nodezator in the future, so people can have a node editing interface available for performing different tasks as well.

I'm also considering the possibility to make available a logic editor similar to the one from the deceased Blender's game engine, because it is a versatile interface for programming logic suitable for non-programmers and it is even used nowadays in the UPBGE project.

Although the target userbase for myappmaker are people with little to no programming experience, integrating regular Python programming in the app is not detrimental. As long as we guarantee great, intuitive, effective interfaces for non-technical users to make apps, there is no harm in also making available common programmer tools where these users can take their first steps into "regular" programming and as a result have even more control over the apps they are making.


## myappmaker basic design

As the name of this section implies, we won't be presenting a full design for now, nor list all intended features. That is so because at this point in time myappmaker didn't even left the drawing board yet and much is still to be decided as each of its interfaces/panels are developed, integrated and tested.

Instead, we'll present many of its initial characteristics and approaches used to build it as well as its elements. That is, everything that is needed to support its usage described earlier in this chapter.

In fact, detailing specific design points too much is even avoided, unless deemed helpful, since there's no guarantee many of these details are even viable when it comes to fit them all together in the final design/configuration of myappmaker.


### GUI framework and licensing

Myappmaker will be programmed in PySide (version 6), rather than PyQT. That's because both Python bindings to the Qt framework have the same capabilities anyway, but PySide are the official bindings to it. On top of that, both libraries are similar enough that if needed, switching between them in the future or even adding an abstraction layer so both can be used is possible.

Regarding licensing for PyQT vs PySide software, the differences between them are not relevant to this project, since we intend to share myappmaker's source, that is, dedicate it to the public domain. Such differences are only relevant when one intend to distribute closed-source software made the libraries. In such cases, PySide is still a tad more permissive, as explained by [Martin Fitzpatrick](https://www.pythonguis.com/faq/pyqt5-vs-pyside2/):

> The key difference in the two versions — in fact the entire reason PySide2 exists — is licensing. PyQt5 is available under a GPL or commercial license, and PySide2 under a LGPL license.
> 
> If you are planning to release your software itself under the GPL, or you are developing software which will not be distributed, the GPL requirement of PyQt5 is unlikely to be an issue. However, if you plan to distribute your software without distributing the source you will either need to purchase a commercial license from Riverbank for PyQt5 or use PySide2.
> 
> The LGPL license does not require you to share the source code of your own applications, even if they are bundled with PySide2. You only need to ensure that the source code covered by the LGPL is made available, including modifications you have made to it, if any. In normal use there will not be any modifications and the standard distributions of PySide2/Qt5 source code will already cover this for you.


### Design of different panels/interfaces

The different panels described in the previous section on myappmaker's usage will be presented in a PySide application. Most of them will contain regular widgets using common classes like QWidgets with the associated layouts to manage their positioning. These will be the panels containing controls and settings for the various facets of app building.

Other interfaces/panels containing graphics, logic and behaviour represent the app itself, rather than the ones containing controls and settings. Such interfaces/panels representing the app, like the canvas, the block coding interface, and (maybe) the logic editor, will be presented as shapes or stylized drawings made with the QGraphics framework, instead of more common PySide classes.

The QGraphics framework provides a very powerful 2D vector graphics interface with scenes containing shapes and paths like SVG. This makes it a lot easier to export these interfaces to SVG at will in order to share the corresponding info online. That is, the user will be able to freely export things like:

- interfaces designed on myappmaker's canvas,
- code blocks made in the block coding interface,
- and logic made in the logic editor (if it is included in the final design)

...as SVG files.


### Data model

Myappmaker will store all of its data, assets and code as individual files gathered in a single zip file with an .appf (application files) extension.

This is a commom practices in many software projects like files from the Microsoft office suite and Blender 3D.

Having all files associated with an application project bundled together as a single .zip file is much more convenient and provides full portability of the project. The Godot game engine doesn't even store its projects as a single .zip file, but rather as a whole folder whose contents are managed via Godot itself.

Although not a concern at the first phases of development, over time I'd also like to ensure that such data model is also compatible with version control with git. However, it is more of a nice-to-have, since a lot of extra consideration must be given to the possibility because of its various implications, including how intuitive it would be for non-programmers to use it.
