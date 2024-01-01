# 115-1000_Display
本開発品は115系1000番台のメーターパネル表示灯をBVEと連動させるものです。  
単体でも動作が可能ですし、[こちら](https://github.com/GraphTechKEN/MC53_ME38_BVE_VM)との連動が可能です。

> [!TIP]
>- BVE5.8と6の両方に対応
>- Arduino Microを使用します。
>- 他のArduinoが使用できる方は他のものでも構いませんが、今後の機能拡張のためMicroを使用しております^^配線がいびつなのもそのためですご了承ください。

## 製作方法
1. 基板は秋月電子製片面紙エポキシ・ユニバーサル基板　Ａの小タイプ(AE-5)またはサンハヤト製(ICB-97 1.2mm またはICB-97B 1.6mm)を推奨します。
2. 使用マイコンはArduino MicroのArduino純正品です。それ以外では正しく動作しないかピン配置が異なります。ご注意ください。
4. 添付の[回路図通り](115-1000_Display_6.0.0.4.pdf)に[製作](115-1000_Display_6.0.0.4.png)します。
   [回路図](115-1000_Display_6.0.0.4.pdf)と[実態配線図](115-1000_Display_6.0.0.4.7.png)がありますので参考にしてください。
   コネクタ類も参考です。直接配線しても問題はありません。
   ![実態配線図](https://github.com/GraphTechKEN/115-1000_Display/blob/main/115-1000_Display_6.0.0.4.png)

> [!WARNING]
>- 配線が1本でも異なると所望の動作はしません。+24V、+5VとGNDのショートは特に注意してください。
>- 本開発品によるいかなる破損や不具合等が生じても当方はいかなる責任を負いかねますので、ご了承ください。

> [!TIP]
>- Serial1入力(Rx,3番ピン)を[連動基板](https://github.com/GraphTechKEN/MC53_ME38_BVE_VM)のSerial1出力(Tx,2番ピン)、5V(1番ピン同士)とGND(4番ピン同士)とをそれぞれ接続することで、コントローラーと連動が可能になります。
>- メーターパネル単体の連動は、USBで直接行えますが、コントローラーの動作は無効になります。
>- Serial1入力(Rx,3番ピン)：Serial電文を他基板から受信します。

## BVEとの連動方法
> [こちら](https://github.com/GraphTechKEN/SerialOutputEx)を参照してください。
