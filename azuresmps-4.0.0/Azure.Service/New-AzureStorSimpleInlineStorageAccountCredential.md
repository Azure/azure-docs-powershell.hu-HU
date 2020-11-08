---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015517"
---
# New-AzureStorSimpleInlineStorageAccountCredential

## Áttekintés
Szövegközi tárterület-azonosító hitelesítő adatait hozza létre.

## SZINTAXISA

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleInlineStorageAccountCredential** parancsmag egy szövegközi, az Azure Storage Account hitelesítőadat-objektumot hoz létre.
Ez a parancsmag egy dummy hitelesítőadat-objektumot hoz létre.
A **New-AzureStorSimpleDeviceVolumeContainer** parancsmagot és az aktuális parancsmagot ugyanazzal a paranccsal használhatja a Windows PowerShell-adatcsatornán keresztül.
A tényleges tárterület-fiók hitelesítőadat-objektuma a kötet tárolójának létrehozása részeként jön létre.

## Példák

### Példa 1: tárolási fiók hitelesítő adatainak létrehozása
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

Ez a parancs létrehozza a tárolási fiók hitelesítő adatait, majd átadja azt a **New-AzureStorSimpleDeviceVolumeContainer** parancsmagnak a pipeline operátor használatával.
Ez a tároló a próbabábu hitelesítő adatait használja a mennyiségi tároló létrehozásához.

## PARAMÉTEREK

### -Végpont
A tárolási fiók Azure Storage végpontját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
A tárterület-fiók kulcsát adja meg egyszerű szövegként.
A rendszer titkosított formátumban továbbítja a kulcsot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
A meglévő tárterület-fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### StorageAccountCredentialResponse
Ez a parancsmag egy **CloudType** -objektumot ad eredményül, amely az alábbi mezőket tartalmazza: 

- **Hostname (állomásnév** )
**Karakterlánc**. 
- **InstanceId**.
**Karakterlánc**. 
- **IsDefault**.
**Logikai** érték. 
- **Tartózkodási hely**.
**Karakterlánc**. 
- **Login (bejelentkezés** )
**Karakterlánc**. 
- **Name (név** )
**Karakterlánc**. 
- **OperationInProgress**.
**OperationInProgress**. 
- **Jelszavas**.
**Karakterlánc**. 
- **PasswordEncryptionCertThumbprint**.
**Karakterlánc**. 
- **UseSSL**.
**Logikai** érték. 
- **VolumeCount**.
**Egész szám**.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Új – AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)


