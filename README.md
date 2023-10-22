# image-to-rgb565

Download images (or local files) and convert to RGB565, mapping it for use like a header file (.h) with the Arduino TFT_eSPI library and probably others.

# How to use

python image-to-rgb565.py <text file for header with utf-8 encoding> <url http or file> <url http or file> ...

Ex: python image_to_rgb565.py openweathermap.txt https://openweathermap.org/img/wn/01d.png https://openweathermap.org/img/wn/02d.png https://openweathermap.org/img/wn/03d.png https://openweathermap.org/img/wn/04d.png https://openweathermap.org/img/wn/09d.png https://openweathermap.org/img/wn/10d.png https://openweathermap.org/img/wn/11d.png https://openweathermap.org/img/wn/13d.png https://openweathermap.org/img/wn/50d.png > icons.h

PS: list of urls can be generated with:
icons = ['01d', '02d', '03d', '04d', '09d', '10d', '11d', '13d', '50d',
         '01n', '02n', '03n', '04n', '09n', '10n', '11n', '13n', '50n']
for icon in icons:
    print(f"https://openweathermap.org/img/wn/{icon}.png", end=" ")
