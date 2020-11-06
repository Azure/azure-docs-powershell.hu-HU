---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 01ded3d4e9d77edac39e7c632f46d6e7ecf9eeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493267"
---
# Get-AzureBatchRemoteLoginSettings

## Áttekintés
A számítási csomópont távoli bejelentkezési beállításait kapja meg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Azonosító (alapértelmezett)
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureBatchRemoteLoginSettings** parancsmag a virtuális gépek infrastruktúra-alapú készletében a számítási csomópont távoli bejelentkezési beállításait kapja.

## Példák

### Példa 1: távoli bejelentkezési beállítások beszerzése a készlet összes csomópontjára
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Az első parancs a **Get-AzureRmBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.
A parancs a következő parancsban a $Context változó környezetét tárolja.

A második parancs a **Get-AzureBatchComputeNode** segítségével az azonosító ContosoPool tartalmazó készlet minden számítási csomópontját bekapja.
A parancs a csővezeték-kezelő használatával továbbítja az egyes számítógép-csomópontokat az aktuális parancsmagnak.
A parancs minden számítási csomóponthoz megkapja a távoli bejelentkezési beállításokat.

### 2. példa: egy csomópont távoli bejelentkezési beállításainak beszerzése
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Az első parancs beolvassa az előfizetéshez tartozó hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét, majd a $Context változóban tárolja.

A második parancs beolvassa a számítási csomópont távoli bejelentkezési beállításait, amely az azonosító ContosoPool tartalmazó készletben a megadott azonosítót tartalmazza.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** beolvasásához használja az Get-AzureRmBatchAccountKeys parancsmagot.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
A számítási csomópontot **PSComputeNode** objektumként adja meg, amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.
A számítási csomópont objektum beolvasásához használja az Get-AzureBatchComputeNode parancsmagot.

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyhez a távoli bejelentkezési beállításokat be szeretné szerezni.
amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
A virtuális gépet tartalmazó készlet AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### BatchAccountContext
A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről

### PSComputeNode
A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### PSRemoteLoginSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[Get-AzureBatchRemoteDesktopProtocolFile](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[Azure-köteg parancsmagok](./AzureRM.Batch.md)


