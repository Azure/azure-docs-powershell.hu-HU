---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015520"
---
# New-AzureStorSimpleDeviceVolumeContainer

## Áttekintés
Kötet tárolót hoz létre.

## SZINTAXISA

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleDeviceVolumeContainer** parancsmag létrehoz egy kötet tárolót.
Az új mennyiségi tárolóhoz társítania kell egy tárolási fiók hitelesítő adatait.
A **Get-AzureStorSimpleStorageAccountCredential** parancsmaggal szerezhet be tárolási fiók hitelesítő adatait.

## Példák

### Példa 1: tároló létrehozása
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

Ez a parancs a **Get-AzureStorSimpleStorageAccountCredential** parancsmag használatával kapja meg a ContosoAccount nevű fiókhoz tartozó tárolási fiók hitelesítő adatait.
A parancs a pipeline operátor segítségével továbbítja a hitelesítő adatokat az aktuális parancsmagnak.
Ez a parancsmag az adott parancsmag hitelesítő adataival hozza létre a Container08 nevű tárolót a Contoso63-AppVm nevű eszközön.
Ez a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.
A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.

## PARAMÉTEREK

### -BandWidthRateInMbps
A sávszélesség sebességének meghatározása másodpercenként (Mbps).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Annak a StorSimple-eszköznek a nevét adja meg, amelybe a kötet tárolóját létre szeretné hozni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionEnabled
Azt jelzi, hogy engedélyezi-e a titkosítást.

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

### -EncryptionKey
A titkosítási kulcsot adja meg.

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

### -PrimaryStorageAccountCredential
A hitelesítő adatokat **StorageAccountCredential** objektumként adja meg az új mennyiségi tárolóhoz való társításhoz.
Ha **StorageAccountCredential** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleStorageAccountCredential** parancsmagot.

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -VolumeContainerName
A létrehozandó mennyiségi tároló nevét adja meg.

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

### StorageAccountCredential
Ez a parancsmag egy **PrimaryStorageAccountCredential** -objektumot fogad el a mennyiségi tárolóhoz való társításhoz.

## KIMENETEK

### TaskStatusInfo
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceVolumeContainer](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


