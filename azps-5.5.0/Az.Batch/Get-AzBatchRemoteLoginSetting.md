---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205247"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
Távoli bejelentkezési beállításokat kap egy számítási csomóponthoz.

## SZINTAXIS

### Id (Default)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzBatchRemoteLoginSetting** parancsmag távoli bejelentkezési beállításokat kap egy számítási csomóponthoz egy virtuális gép infrastruktúrán alapuló készletében.

## PÉLDÁK

### 1. példa: Távoli bejelentkezési beállítások lekérte a készlet összes csomópontját
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Az első parancs a **Get-AzBatchAccountKey** használatával kap egy kötegfiók környezetét, amely az előfizetés hozzáférési kulcsait tartalmazza.
A parancs a következő parancsban $Context változóban tárolja a környezetét.
A második parancs a **Get-AzBatchComputeNode** használatával bekérte a ContosoPool azonosítójú számítási csomópontokat a készletbe.
A parancs minden egyes számítógépcsomópontot az aktuális parancsmagnak ad át a folyamat műveleti operátorával.
A parancs az egyes számítási csomópontok távoli bejelentkezési beállításait kapja meg.

### 2. példa: Távoli bejelentkezési beállítások lekérte egy csomóponthoz
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Az első parancs egy kötegfiók környezetét kapja meg, amely tartalmazza az előfizetés hozzáférési kulcsait, majd azt a $Context változóban tárolja.
A második parancs annak a számítási csomópontnak a távoli bejelentkezési beállításait kapja meg, amely a ContosoPool azonosítót tartalmazza a megadott azonosítóval.

## PARAMETERS

### -BatchContext
Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.
Az előfizetés hozzáférési kulcsait tartalmazó **BatchAccountContext** fájl beszerzéséhez használja a Get-AzBatchAccountKey parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Egy olyan számítási csomópontot ad meg **PSComputeNode-objektumként,** amelyhez ez a parancsmag távoli bejelentkezési beállításokat kap.
Számítási csomópontobjektum beszerzéséhez használja a Get-AzBatchComputeNode parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Annak a számítási csomópontnak az azonosítója, amelynek a távoli bejelentkezési beállításait meg szeretné kapni.
amelynek a parancsmagja távoli bejelentkezési beállításokat kap.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
A virtuális gépet tartalmazó készlet azonosítója.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Bat. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.Bat. Models.PSRemoteLoginSettings

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Azure Batch-parancsmagok](/powershell/module/Az.Batch/)
