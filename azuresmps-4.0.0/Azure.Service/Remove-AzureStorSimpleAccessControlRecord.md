---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016096"
---
# Remove-AzureStorSimpleAccessControlRecord

## Áttekintés
Egy Access-vezérlő rekord törlése a szolgáltatás konfigurációjától

## SZINTAXISA

### IdentifyByName
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureStorSimpleAccessControlRecord** parancsmag egy Access-vezérlő rekordot töröl a szolgáltatás konfigurációjától.

## Példák

### 1. példa: Access-Controlaccess-vezérlő recordaccess-vezérlő eltávolítása
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

Ez a parancs törli a Acr10 nevű Access-vezérlő rekordot.
Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.

### 2. példa: Access-Controlaccess rekordok eltávolítása a pipelineAccess Controlaccess Controlaccess-vezérlő segítségével
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

Ez a parancs a **Get-AzureStorSimpleAccessControlRecord** segítségével beolvassa a Acr10 nevű **AccessControlRecord** , majd a pipeline operátor segítségével átadja az objektumot az aktuális parancsmagnak.
A parancs elindítja azt a műveletet, amely eltávolítja a **AccessControlRecord** objektumot, majd egy **TaskResponse** objektumot ad eredményül.
A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.

## PARAMÉTEREK

### -ACR
Egy törölni kívánt **AccessControlRecord** -objektumot ad meg.
Ha **AccessControlRecord** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleAccessControlRecord** parancsmagot.

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ACRName
A törlendő hozzáférés-szabályozási rekord nevét adja meg.

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

### AccessControlRecord
Ez a parancsmag a **AccessControlRecord** -objektumot fogadja el.
A **AccessControlRecord** -objektumok az alábbi mezőket tartalmazzák: 

- **GlobalId** ( **karakterlánc** ) 
- **InitiatorName** ( **karakterlánc** ) 
- **InstanceId** ( **karakterlánc** ) 
- **Name** ( **karakterlánc** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## KIMENETEK

### TaskStatusInfo, TaskResponse
Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.
Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Új – AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


