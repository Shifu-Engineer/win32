---
title: Elements
description: Elements
ms.assetid: 2fce7855-9d38-4d3b-aac1-9c0e0021af7e
keywords:
- Windows DVD Maker,elements
- DVD Maker,elements
- programming reference,Windows DVD Maker elements
- reference for Windows DVD Maker,elements
- Windows DVD Maker,transitions
- DVD Maker,transitions
- transitions,elements
- Windows DVD Maker,buttons
- DVD Maker,buttons
- Windows DVD Maker,menus
- DVD Maker,menus
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Elements

This section documents all the elements in the custom XML file used to create custom transitions, buttons, and menu styles for Windows DVD Maker. You can view a sample XML file for Windows DVD Maker in [Samples](samples.md).

**Important** XML file parsing in Windows DVD Maker is case sensitive.



| Element                                                                                     | Description                                                                                                                                                       |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Alpha**](alpha-element.md)                                                              | Defines the transparency of the specified object.                                                                                                                 |
| [**BackgroundZoom**](backgroundzoom.md)                                                    | Indicates whether to zoom the input video image to fill the screen or to letterbox or pillarbox it.                                                               |
| [**BoundingRect**](boundingrect.md)                                                        | Defines the location and size of the specified text object.                                                                                                       |
| [**ButtonLocations (Child of MainMenu)**](buttonlocations--child-of-mainmenu.md)           | Specifies the normalized (with respect to a screen with a 16:9 aspect ratio) position and dimensions of the menu buttons on the main menu.                        |
| [**ButtonLocations (Child of NotesMenu)**](buttonlocations--child-of-notesmenu.md)         | Specifies the normalized (with respect to a screen with a 16:9 aspect ratio) position and dimensions of the button on the notes menu.                             |
| [**ButtonLocations (Child of ScenesMenu2)**](buttonlocations--child-of-scenesmenu2.md)     | Specifies the normalized (with respect to a screen with a 16:9 aspect ratio) position and dimensions of the menu buttons on a scene menu with two scene buttons.  |
| [**ButtonLocations (Child of ScenesMenu4)**](buttonlocations--child-of-scenesmenu4.md)     | Specifies the normalized (with respect to a screen with a 16:9 aspect ratio) position and dimensions of the menu buttons on a scene menu with four scene buttons. |
| [**ButtonLocations (Child of ScenesMenu6)**](buttonlocations--child-of-scenesmenu6.md)     | Specifies the normalized (with respect to a screen with a 16:9 aspect ratio) position and dimensions of the menu buttons on a scene menu with six scene buttons.  |
| [**ButtonSelection**](buttonselection.md)                                                  | Indicates whether the button has a subpicture part that is used to indicate that it has been selected ("pressed").                                                |
| [**ButtonText**](buttontext.md)                                                            | Causes a text media node to be created if the button name specified in the *value* parameter exists.                                                              |
| [**Color**](color.md)                                                                      | The color of the source.                                                                                                                                          |
| [**Duration**](duration.md)                                                                | Specifies the duration of the parent menu or transition.                                                                                                          |
| [**DVDButton**](dvdbutton.md)                                                              | The boundary tag for the individual button object.                                                                                                                |
| [**DVDButtonDLL**](dvdbuttondll.md)                                                        | The boundary tag for a single button object.                                                                                                                      |
| [**DVDButtons**](dvdbuttons.md)                                                            | The boundary tag for the custom DVD buttons section of the XML file.                                                                                              |
| [**DVDMenuStyle**](dvdmenustyle.md)                                                        | The boundary tag for the individual menu style object.                                                                                                            |
| [**DVDMenuStyleDLL**](dvdmenustyledll.md)                                                  | The boundary tag for a single DVD menu style object.                                                                                                              |
| [**DVDMenuStyles**](dvdmenustyles.md)                                                      | The boundary tag for the custom DVD menu styles section of the XML file.                                                                                          |
| [**DVDTransition**](dvdtransition.md)                                                      | The boundary tag for the individual DVD transition object.                                                                                                        |
| [**DVDTransitionDLL**](dvdtransitiondll.md)                                                | The boundary tag for a single DVD transition object.                                                                                                              |
| [**DVDTransitions**](dvdtransitions.md)                                                    | The boundary tag for the custom DVD transitions section of the XML file.                                                                                          |
| [**EntranceDuration**](entranceduration.md)                                                | Defines the duration of the entrance effect for the specified text media node.                                                                                    |
| [**EntranceEffect**](entranceeffect.md)                                                    | Defines the entrance effect for the specified text media node.                                                                                                    |
| [**EntrancePosition**](entranceposition.md)                                                | Defines the entrance position of the specified text media node.                                                                                                   |
| [**ExitDuration**](exitduration.md)                                                        | Defines the duration of the exit effect for the specified text media node.                                                                                        |
| [**ExitEffect**](exiteffect.md)                                                            | Defines the exit effect for the specified text media node.                                                                                                        |
| [**ExitPosition**](exitposition.md)                                                        | Defines the exit position of the specified text media node.                                                                                                       |
| [**Font**](font.md)                                                                        | Specifies the font to be used by this menu style.                                                                                                                 |
| [**FontSize**](fontsize.md)                                                                | Specifies the size of text.                                                                                                                                       |
| [**FrontColor1**](frontcolor1.md)                                                          | Specifies the color of the text in this menu style.                                                                                                               |
| [**FXFile**](fxfile.md)                                                                    | Points to an .fx file that contains the pixel and vertex shaders used in the button style.                                                                        |
| [**Graph (Child of MainMenu)**](graph--child-of-mainmenu.md)                               | Defines the pipeline graph for the main menu.                                                                                                                     |
| [**Graph (Child of MainToNotesTransition)**](graph--child-of-maintonotestransition.md)     | Defines the pipeline graph for the transition between the main menu and the notes menu.                                                                           |
| [**Graph (Child of MainToScenesXTransition)**](graph--child-of-maintoscenesxtransition.md) | Defines the pipeline graph for the DVD transition to scenes menus.                                                                                                |
| [**Graph (Child of NotesMenu)**](graph--child-of-notesmenu.md)                             | Defines the pipeline graph for the notes menu.                                                                                                                    |
| [**Graph (Child of ScenesMenuX)**](graph--child-of-scenesmenux.md)                         | Defines the pipeline graph for the scenes menus.                                                                                                                  |
| [**Graph (Child of ToMainTransition)**](graph--child-of-tomaintransition.md)               | Defines the pipeline graph for the DVD transition into the main menu (the "opening" transition).                                                                  |
| [**GroupName**](groupname.md)                                                              | Specifies the category into which this menu style should be placed in the Windows DVD Maker UI.                                                                   |
| [**HorizontalAlignment**](horizontalalignment.md)                                          | Indicates the horizontal alignment of the specified text object.                                                                                                  |
| [**Input**](input.md)                                                                      | Creates a source (media node) in the pipeline graph.                                                                                                              |
| [**InputStartOffset**](inputstartoffset.md)                                                | Defines the time offset at which to start a source.                                                                                                               |
| [**InsetVideoZoom**](insetvideozoom.md)                                                    | Indicates whether to zoom the inset video image to fill the screen or to letterbox or pillarbox it.                                                               |
| [**IsBold**](isbold.md)                                                                    | Specifies whether the text should be boldfaced.                                                                                                                   |
| [MainMenu](mainmenu.md)                                                                    | Describes the main menu of the DVD.                                                                                                                               |
| [MainPosition](mainposition.md)                                                            | Defines the normalized position of the text when it is not "entering" or "exiting" the viewport.                                                                  |
| [MainToNotesTransition](maintonotestransition.md)                                          | Defines the transition displayed between the main menu and the notes menu.                                                                                        |
| [MainToScenes2Transition](maintoscenes2transition.md)                                      | Defines the transition displayed between the main menu and a two-button scene menu.                                                                               |
| [MainToScenes4Transition](maintoscenes4transition.md)                                      | Defines the transition displayed between the main menu and a four-button scene menu.                                                                              |
| [MainToScenes6Transition](maintoscenes6transition.md)                                      | Defines the transition displayed between the main menu and a six-button scene menu.                                                                               |
| [MenuEndTime](menuendtime.md)                                                              | Specifies the time index at which to end a source.                                                                                                                |
| [Menus](menus.md)                                                                          | Defines both required and optional menus, as well as any optional transitions.                                                                                    |
| [MenuStartTime](menustarttime.md)                                                          | Specifies the time index at which to start a source.                                                                                                              |
| [MinAutoFontSize](minautofontsize.md)                                                      | Defines the automatic minimum font size for the specified text object.                                                                                            |
| [NavigationButton](navigationbutton.md)                                                    | Causes a media node to be created that renders a scene button.                                                                                                    |
| [NavigationButtonTFXToken](navigationbuttontfxtoken.md)                                    | Specifies the globally unique identifier (GUID) of the navigation button style to be used by this menu style.                                                     |
| [NextMenuButton](nextmenubutton.md)                                                        | Specifies the location and size of the "Next Menu" button.                                                                                                        |
| [NotesMenu](notesmenu.md)                                                                  | Defines the "Notes" menu of the DVD.                                                                                                                              |
| [NumInputs](numinputs.md)                                                                  | Specifies the number of inputs required by the media node.                                                                                                        |
| [Offset](offset.md)                                                                        | Defines a three-dimensional (3-D) translation for the specified object.                                                                                           |
| [Param](param.md)                                                                          | Defines parameters for the specified DVD transition.                                                                                                              |
| [ParentMenuButton](parentmenubutton.md)                                                    | Specifies the location and size of the "Parent Menu" button.                                                                                                      |
| [PlayButton](playbutton.md)                                                                | Specifies the location and size of the "Play" button.                                                                                                             |
| [PlayButtonText](playbuttontext.md)                                                        | Specifies the text used for this menu style's "Play" button.                                                                                                      |
| [Point](point.md)                                                                          | Specifies the values of the parameter at specific times.                                                                                                          |
| [PreviousMenuButton](previousmenubutton.md)                                                | Specifies the location and size of the "Previous Menu" button.                                                                                                    |
| [Properties (Child of Token)](properties--child-of-token.md)                               | Specifies the properties of the media node.                                                                                                                       |
| [Properties (Child of Text)](properties--child-of-text.md)                                 | Specifies the properties of the text media node.                                                                                                                  |
| [Properties (Child of ButtonText)](properties--child-of-buttontext.md)                     | Specifies the properties of the button text media node.                                                                                                           |
| [Properties (Parent of Color)](properties--parent-of-color.md)                             | Specifies the properties of the media node.                                                                                                                       |
| [Properties (Child of SceneButton)](properties--child-of-scenebutton.md)                   | Specifies the properties of the scene button.                                                                                                                     |
| [Properties (Child of NavigationButton)](properties--child-of-navigationbutton.md)         | Specifies the properties of the navigation button.                                                                                                                |
| [ResizingTechnique](resizingtechnique.md)                                                  | Specifies the resizing technique for the specified text.                                                                                                          |
| [Rotate](rotate.md)                                                                        | Defines a three-dimensional (3-D) rotation for a specified object.                                                                                                |
| [Scale](scale.md)                                                                          | Specifies the scale factor to apply to the rectangular mesh for the specified media node.                                                                         |
| [Scene1Button](scene1button.md)                                                            | Specifies the location and size of the "Scene 1" button.                                                                                                          |
| [Scene2Button](scene2button.md)                                                            | Specifies the location and size of the "Scene 2" button.                                                                                                          |
| [Scene3Button](scene3button.md)                                                            | Specifies the location and size of the "Scene 3" button.                                                                                                          |
| [Scene4Button](scene4button.md)                                                            | Specifies the location and size of the "Scene 4" button.                                                                                                          |
| [Scene5Button](scene5button.md)                                                            | Specifies the location and size of the "Scene 5" button.                                                                                                          |
| [Scene6Button](scene6button.md)                                                            | Specifies the location and size of the "Scene 6" button.                                                                                                          |
| [SceneButton](scenebutton.md)                                                              | Causes a media node to be created that renders a scene button.                                                                                                    |
| [SceneButtonTFXToken](scenebuttontfxtoken.md)                                              | Specifies the globally unique identifier (GUID) of the scene button style to be used by this menu style.                                                          |
| [ScenesMenu2](scenesmenu2.md)                                                              | Defines a menu that has two or fewer scene buttons.                                                                                                               |
| [ScenesMenu4](scenesmenu4.md)                                                              | Defines a menu that has four or fewer scene buttons.                                                                                                              |
| [ScenesMenu6](scenesmenu6.md)                                                              | Defines a menu that has six or fewer scene buttons.                                                                                                               |
| [Source](source.md)                                                                        | Specifies an individual image source.                                                                                                                             |
| [StaticThumbnail](staticthumbnail.md)                                                      | Specifies an image that represents the button or menu style (depending on the context) in the Windows DVD Maker UI.                                               |
| [Submenu1Button](submenu1button.md)                                                        | Specifies the location and size of the "Submenu1" button.                                                                                                         |
| [Submenu1ButtonText](submenu1buttontext.md)                                                | Specifies the text used for this menu style's "Submenu1" button. This is usually the "Scenes" button.                                                             |
| [Submenu2Button](submenu2button.md)                                                        | Specifies the location and size of the "Submenu2" button. This is usually the "Notes" button.                                                                     |
| [Submenu2ButtonText](submenu2buttontext.md)                                                | Specifies the text used for this menu style's "Submenu2" button. This is usually the "Notes" button.                                                              |
| [Subpicture](subpicture.md)                                                                | Describes the pipeline graph that Windows DVD Maker will use when rendering the subpicture.                                                                       |
| [SubpictureTextures](subpicturetextures.md)                                                | Specifies the source files that will be created when rendering the subpicture.                                                                                    |
| [Technique](technique.md)                                                                  | Specifies the effect technique that the specified button will use.                                                                                                |
| [Text](text.md)                                                                            | Inserts a media node that renders text into the pipeline graph.                                                                                                   |
| [TextTFXToken](texttfxtoken.md)                                                            | Specifies the globally unique identifier (GUID) of a collection of text attributes to be applied to text in this menu style.                                      |
| [Textures](textures.md)                                                                    | Specifies the source files that Windows DVD Maker will create when the button or transition is created (depending on the context).                                |
| [ThumbnailTime](thumbnailtime.md)                                                          | Specifies the time offset into the menu in the Windows DVD Maker user interface (UI) that renders a static preview of the menu style.                             |
| [TitleText](titletext.md)                                                                  | Specifies the text used for this menu style's menu title.                                                                                                         |
| [Token (One Child Element)](token--one-child-element.md)                                   | Creates a media node in the pipeline graph.                                                                                                                       |
| [Token (Three Child Elements)](token--three-child-elements.md)                             | Creates a media node in the pipeline graph.                                                                                                                       |
| [Token (Four Child Elements)](token--four-child-elements.md)                               | Creates a media node in the pipeline graph.                                                                                                                       |
| [ToMainTransition](tomaintransition.md)                                                    | Specifies the transition into the main menu (the "opening" transition) that is displayed when the main menu is displayed for the first time.                      |
| [TransitionsAndEffects](transitionsandeffects.md)                                          | The boundary tag for the entire custom XML file.                                                                                                                  |
| [UsesBackground](usesbackground.md)                                                        | Specifies whether the user will be able to override the specified background source.                                                                              |



 

## Related topics

<dl> <dt>

[**Windows DVD Maker XML Extensibility**](windows-dvd-maker-xml-extensibility.md)
</dt> </dl>

 

 



