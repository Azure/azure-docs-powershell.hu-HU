---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368911"
---
# Get-AzVmssVM

## SYNOPSIS
Egy VMSS virtuális gép tulajdonságait kapja meg.

## SZINTAXIS

### DefaultParameter (alapértelmezett)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzVmssVM** parancsmag egy virtuális gép méretkészletének (VMSS) modellnézetét és példánynézetét kapja meg.
A modellnézet a virtuális gép felhasználó által megadott tulajdonságai.
A példánynézet a virtuális gép példányszintű állapota.
Adja meg *az Állapot* paramétert úgy, hogy csak a virtuális gép példánynézetét adja meg.

## PÉLDÁK

### 1. példa: VMSS virtuális gép tulajdonságainak lekérte
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Ez a parancs a VMSS virtuális gép tulajdonságait kapja meg, amely a Group0001 nevű erőforráscsoporthoz tartozik.
Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modellnézetét kapja meg.

### 2. példa: A VMSS virtuális gép modellnézet-tulajdonságainak lekérte
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Ez a parancs a VMSS virtuális gép tulajdonságait kapja meg, amely a Group002 nevű erőforráscsoporthoz tartozik.
A parancs a változóban tárolt példányazonosítót $ID, amelyhez a modellnézetet meg kell kapnia.

### 3. példa: A VMSS virtuális gép példánynézet-tulajdonságainak lekérte
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Ez a parancs a VMSS virtuális gép tulajdonságait kapja meg, amely a Group002 nevű erőforráscsoporthoz tartozik.
Mivel a parancs a *InstanceView* kapcsoló paramétert adja meg, a parancsmag a virtuális gép példánynézetét kapja meg.
A parancs a példányazonosítót abban a változóban $ID, amelyhez meg kell kapnia a példánynézetet.

## PARAMETERS

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

### -InstanceId
Azt a példányazonosítót adja meg, amelynek a modellnézetét le kell kapnia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Azt jelzi, hogy ez a parancsmag csak a virtuális gép példánynézetét kapja meg.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A VMSS erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
A VMSS nevének fakása.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVms](./Get-AzVmss.md)


