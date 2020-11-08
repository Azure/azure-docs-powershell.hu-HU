---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016449"
---
# Remove-AzureStorSimpleStorageAccountCredential

## Áttekintés
Törli a meglévő tárolási fiók hitelesítő adatait.

## SZINTAXISA

### IdentifyByName
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureStorSimpleStorageAccountCredential** parancsmag törli a meglévő tárolási fiók hitelesítő adatait.
Adjon meg egy fiókot név szerint, vagy használja a **Get-AzureStorSimpleStorageAccountCredential** parancsmagot a törölni kívánt **StorageAccountCredential** -objektum beszerzéséhez.

## Példák

### 1. példa: a tárolási fiók hitelesítő adatainak eltávolítása
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

Ez a parancs eltávolítja a ContosoStorage07 nevű tárterület-fiókhoz tartozó hitelesítő adatokat.
Ez a parancs az *erő* paramétert adja meg.
A parancsmag a hitelesítő adatok megadását kérő üzenet nélkül távolítja el a hitelesítő adatokat.

### 2. példa: a tárolási fiók hitelesítő adatainak eltávolítása a csővezeték-kezelő használatával
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

Ez a parancs a **Get-AzureStorSimpleStorageAccountCredential** parancsmaggal kapja meg a ContosoStorage07 nevű tárolási fiókot, majd átadja az adott objektumot az aktuális parancsmagnak.
Az aktuális parancsmag eltávolítja az adott tárolási fiók hitelesítő adatait.
Ez a parancs a *WaitForComplete* paramétert adja meg.
A parancsmag nem adja vissza a vezérlőt addig, amíg el nem fejezi az eltávolítási műveletet.

## PARAMÉTEREK

### -Force
Azt jelzi, hogy ez a parancsmag nem kér megerősítést.

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

### -SAC
A hitelesítő adatokat **StorageAccountCredential** objektumként adja meg az eltávolításhoz.
Ha **StorageAccountCredential** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleStorageAccountCredential** parancsmagot.

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Annak a tárterület-fióknak a nevét adja meg, amelyet törölni szeretne.

```yaml
Type: String
Parameter Sets: IdentifyByName
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
Ez a parancsmag a csővezeték segítségével fogadja el a **StorageAccountCredential** -objektumokat.

## KIMENETEK

### TaskStatusInfo
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[Új – AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Set-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


