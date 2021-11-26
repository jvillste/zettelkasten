Humans interact with computers through controllers.

# controller attributes
- number of axes
- half axis / whole axis: pressure on surface can only be appled to one direction
- axis length: fixed / variable infinite. Touch screen has fixed axis lengths, mouse has variable axis lengths depending on the available surface area. A rotary encoder has one infinite axis
- relativity: reltaive / absolute. Relative controller only senses change. Mouse is relative, touch screen is absolute.
- rezolution: binary / analog
- persistency: Does the controller return to some state when you do not apply force on it anymore. Persistent controllers: mouse, modwheel. Transient controllers: pitch bend, keyboard, joystick.
- jumpability: jumpable / non jumpable. Can the controller state be set without going through intermediate states? Touch screen is jumpable, joystick is continous. All relative controllers are non jumpable.
- composability: is the controller usually used as a combination of multiple controllers. Keyboard has always multiple keys. A touch screen can support multitouch or single touch.

# input interpretation attributes
- derivative: position / speed / acceleration
- origin stability: Joystick controller on touch screen can have variable origin. Varialbe origin is useful with rotary encoders.
- linearity: pen tablet pressure is often interpretted in a nonlinear way. Mouse pointer movements are linear.

# controllers
## mouse
- two variable length whole axes
- analog
- persistent
- non jumpable

## keyboard key
- one fixed length half axis
- binary
- transient
- jumpable

## joystick
- two fixed length half axes
- analog
- transient
- absolute
- non jumpable

## single touch screen touch
- two fixed length whole axes
- analog
- transient
- absolute
- jumpable

## potentiometer
- one fixed length whole axis
- analog
- persistent
- absolute
- non jumpable

## rotary encoder
- one infinite length whole axis
- analog
- persistent
- relative
- non jumpable

See [Encoder vs Potentiometer - How to Choose | Arrow.com](https://www.arrow.com/en/research-and-events/articles/encoder-vs-potentiometer-how-to-choose)

# Are we missing some useful controller type?