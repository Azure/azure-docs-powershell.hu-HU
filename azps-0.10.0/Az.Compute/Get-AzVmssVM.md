---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 43c6f96556cb283ef21f24df00d6a6ddb9c5397a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844542"
---
# Get-AzVmssVM

## Áttekintés
A VMSS virtuális gép tulajdonságait kapja meg.

## SZINTAXISA

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

## Leírás
A **Get-AzVmssVM** parancsmag a Virtual Machine Scale set (VMSS) virtuális gép modell nézetét és példány nézetét kapja meg.
A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.
A példány nézet a virtuális gép példány szintjének állapota.
Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.

## Példák

### Példa 1: VMSS virtuális gép tulajdonságainak beszerzése
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Ez a parancs a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS virtuális gép tulajdonságait kapja meg.
Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.

### 2. példa: a VMSS virtuális gép modell nézetének tulajdonságainak beszerzése
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Ez a parancs a Group002 nevű erőforráscsoport VMSS004 tartozó VMSS virtuális gép tulajdonságait kapja meg.
A parancs a minta nézetet tartalmazó változóban tárolt példány AZONOSÍTÓját kapja meg $ID.

### 3. példa: VMSS virtuális gép példány nézetének tulajdonságainak beszerzése
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Ez a parancs a Group002 nevű erőforráscsoport VMSS004 tartozó VMSS virtuális gép tulajdonságait kapja meg.
Mivel a parancs a *InstanceView* kapcsoló paramétert adja meg, a parancsmag a virtuális gép példány nézetét kapja.
A parancs a példány nézethez tartozó változóban tárolt példány AZONOSÍTÓját kapja meg $ID.

## PARAMÉTEREK

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

### -InstanceId
Annak a példánynak az AZONOSÍTÓját adja meg, amelynek a modell nézetét be szeretné szerezni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A VMSS erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Faj: a VMSS neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


