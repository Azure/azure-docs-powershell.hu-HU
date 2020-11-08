---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015551"
---
# Get-AzureStorSimpleStorageAccountCredential

## Áttekintés
Hitelesítő adatokkal kapja meg a tárolási fiókokat.

## SZINTAXISA

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorSimpleStorageAccountCredential** parancsmag hitelesítő adatokat kap a tárolási fiókokhoz.
Ez a parancsmag a szolgáltatásban vagy egy névvel ellátott **StorageAccountCredential** konfigurált összes **StorageAccountCredential** -objektumot beilleszti.

## Példák

### Példa 1: az erőforrás összes hitelesítő adatainak beolvasása
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

Ez a parancs az aktuális erőforrás tárolási fiókjaihoz elérhető hitelesítő adatokat kapja meg.

### 2. példa: a hitelesítő adatok beszerzése egy adott tárolási fiókhoz
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

Ez a parancs beolvassa a ContosoCloudStorage nevű tárolási fiókhoz tartozó tárolási fiók hitelesítő adatait.

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

### -StorageAccountName
Annak a tároló fióknak a nevét adja meg, amelyhez hitelesítő adatokat szeretne kapni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### StorageAccountCredential, IList\<StorageAccountCredential\>
Ez a parancsmag egy **StorageAccountCredential** -objektumot ad eredményül, ha a *StorageAccountName* paramétert adja meg, vagy ha nem adja meg ezt a paramétert, akkor az a **IList \<StorageAccountCredential\>** objektumot adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Remove-AzureStorSimpleStorageAccountCredential](./Remove-AzureStorSimpleStorageAccountCredential.md)

[Set-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)


