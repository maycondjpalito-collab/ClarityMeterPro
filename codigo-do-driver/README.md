# Código-fonte do dispositivo de áudio "Clarity Meter Pro"

O app Clarity Meter Pro instala um dispositivo de áudio virtual (`ClarityMeterPro.driver`).
Ele é um **programa separado** do app e é compilado a partir do **BlackHole 0.6.0**, de
[Existential Audio Inc.](https://github.com/ExistentialAudio/BlackHole), **sem nenhuma alteração** no código.

Este componente é distribuído sob a **GNU GPL v3** ([`LICENSE-GPL3.txt`](LICENSE-GPL3.txt)).
Esta pasta contém o código-fonte completo dele, para cumprir a licença.

O app e os plug-ins do Clarity Meter Pro são software próprio e conversam com este dispositivo
apenas como um dispositivo de áudio comum do macOS.

## Como compilar

Mudam só o nome, o fabricante e os canais, definidos na linha de compilação:

```bash
mkdir -p ClarityMeterPro.driver/Contents/MacOS ClarityMeterPro.driver/Contents/Resources
clang -bundle -O2 \
  -DkDriver_Name='"ClarityMeterPro"' -DkHas_Driver_Name_Format=0 \
  -DkDevice_Name='"Clarity Meter Pro"' -DkDevice2_Name='"Clarity Meter Pro Mirror"' \
  -DkPlugIn_BundleID='"br.claritymeterpro.driver"' -DkManufacturer_Name='"Palitomix"' \
  -DkPlugIn_Icon='"AppIcon.icns"' -DkNumber_Of_Channels=2 \
  BlackHole.c -framework CoreAudio -framework CoreFoundation -framework Accelerate \
  -o ClarityMeterPro.driver/Contents/MacOS/ClarityMeterProDriver
```

`ClarityMeterPro.driver/Contents/Info.plist`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0"><dict>
<key>CFBundleDevelopmentRegion</key><string>English</string>
<key>CFBundleExecutable</key><string>ClarityMeterProDriver</string>
<key>CFBundleIdentifier</key><string>br.claritymeterpro.driver</string>
<key>CFBundleInfoDictionaryVersion</key><string>6.0</string>
<key>CFBundleName</key><string>ClarityMeterPro</string>
<key>CFBundlePackageType</key><string>BNDL</string>
<key>CFBundleShortVersionString</key><string>1.0</string>
<key>CFBundleVersion</key><string>1</string>
<key>CFPlugInFactories</key><dict><key>a4f1c2de-7b53-4c8e-9d21-5e3b8c6a1f70</key><string>BlackHole_Create</string></dict>
<key>CFPlugInTypes</key><dict><key>443ABAB8-E7B3-491A-B985-BEB9187030DB</key><array><string>a4f1c2de-7b53-4c8e-9d21-5e3b8c6a1f70</string></array></dict>
</dict></plist>
```

Instalação: copie `ClarityMeterPro.driver` para `/Library/Audio/Plug-Ins/HAL/` e rode `sudo killall coreaudiod`.
