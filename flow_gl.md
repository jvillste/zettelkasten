# Flow-gl

## Terms

* Component: a function that returns initial local state and a view.
* View: a function from component local state and view call parameters to a layoutable.
* Layoutable: a data structure and a function from available space to the space that is needed to draw the layoutable.
* Layout: a data structure that contains other layouts and renderables and a function that calculates sizes and positions of those given the available space. A layout is also layoutable.
* Renderable: a data structure that can be rendered by a renderer. Renderables are also layoutables.
* Renderer: a procedure that can render a batch of certain kinds of renderables using for example an OpenGL context.

## Size dependent components

A view is a function from:
* Component local state
* Parameters given from the call site
