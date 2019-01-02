# nRF2401-carbot-joystick

Demonstration 2 wheel differential steering wheel speed control code for the WCRS [carbot](https://github.com/WCRSyyc/carbot) chassis. This takes target wheel speed setting data from an nRF24L01 radio, and used simple acceleration logic to move the power levels toward the specified value.  It also monitors the radio channel, and stops if signal is lost.

The code is heavily commented, and includes a commented out block that can be used for reporting the changing internal state.

This does not implement full featured driving logic. It is intended to provide only enough of the basics for demonstrating safe functionality and debugging. The intent is for the carbot builder to enhance this for their own projects. Providing learning opportunities, including for programming, is part of the goals of the WCRS.

The acceleration and loss of signal logic would normally be beyond the scope of the demonstration code.  However, they were needed for `safe` operation.  The base carbot chassis is not very robust.  The acceleration logic is needed to keep the motors from tearing themselves off when jumping between full power forward to full backward.  Even with the acceleration limiting, the mounts needed reinforcing after running demos for awhile.  The loss of signal enhancement is needed, because early testing encountered a case where something 'broke'.  The car unit ran away, and had to be chased down.
