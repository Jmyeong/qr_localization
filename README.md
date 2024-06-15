# qr_localization
Precise Localization with QR_code Package by team factorial	<br/>
This package uses QR_Code for landmarks when implementing pure_localization on cartographer <br/>
This can enhance accuracy of global localization <br/>
Also can do pose estimation with no initial delay (Original cartographer has initial delay for scan matching)

# How to use
# 1. Camera calibration <br/>
Prepare your camera calibration file to "./camera_param" <br/>

# 2. Prepare QR Code <br/>
you have to give index number to each qr_code (1, 2, 3 ...) This must be integer !!! <br/>
