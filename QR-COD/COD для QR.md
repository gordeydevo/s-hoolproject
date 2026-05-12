import qrcode



url = "https://disk.yandex.ru/i/XaZqmDcRfFsQJg"



qr = qrcode.QRCode(

&#x20;   version=1,

&#x20;   error\_correction=qrcode.constants.ERROR\_CORRECT\_L,

&#x20;   box\_size=10,

&#x20;   border=4,

)

qr.add\_data(url)

qr.make(fit=True)



img = qr.make\_image(fill\_color="black", back\_color="white")



img.save("yandex\_disk\_qr.png")



print("QR-код сохранён как 'yandex\_disk\_qr.png'")

