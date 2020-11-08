---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015851"
---
# Set-AzureStorSimpleStorageAccountCredential

## Áttekintés
Az Azure Storage Access hitelesítő adatainak frissítése

## SZINTAXISA

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureStorSimpleStorageAccountCredential** parancsmag frissíti a meglévő Azure-tárterület elérési hitelesítő adatait a StorSimple OneSDK parancsmagok általi használatra.
Ha többet szeretne tudni arról, hogy hogyan működnek a StorSimple-parancsmagok a tárolási fiókokkal, tanulmányozza az New-AzureStorSimpleStorageAccountCredential parancsmag súgóját.

## Példák

### Példa 1: hitelesítő adatok módosítása
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

Ez a parancs módosítja a ContosoStorage01 nevű tárolási fiók hitelesítő adatait a továbbiakban nem szükséges SSL.

## PARAMÉTEREK

### -Profil
Egy Azure-profilt ad meg.

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
A tárolási fiók hozzáférési kulcsát adja meg egyszerű szövegként.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
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

### -UseSSL
Azt jelzi, hogy SSL-kapcsolatot kell-e használni a kapcsolathoz az új tárolási fiók hitelesítő adatainak használatakor.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### StorageAccountCredentialResponse, TaskResponse
Ez a parancsmag **StorageAccountCredentialResponse** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.
Ha nem adja meg ezt a paramétert, a parancsmag egy **TaskResponse** -objektumot ad eredményül.
A **StorageAccountCredentialResponse** a következő tulajdonságokat tartalmazzák: 

- **CloudType** ( **CloudType** )
- **Hostname** ( **karakterlánc** )
- **InstanceId** ( **karakterlánc** )
- **IsDefault** ( **logikai** )
- **Hely** ( **karakterlánc** )
- **Login** ( **karakterlánc** )
- **Name** ( **karakterlánc** )
- **OperationInProgress** ( **OperationInProgress** )
- **Password** ( **karakterlánc** )
- **PasswordEncryptionCertThumbprint** ( **karakterlánc** )
- **UseSSL** ( **logikai** )
- **VolumeCount** ( **int** )

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[Új – AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Remove-AzureStorSimpleStorageAccountCredential](./Remove-AzureStorSimpleStorageAccountCredential.md)


