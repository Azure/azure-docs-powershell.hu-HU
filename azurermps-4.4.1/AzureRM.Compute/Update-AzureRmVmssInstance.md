---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 1d7655a78ee2abe00b69d485c35b73cee91ee420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672708"
---
# Update-AzureRmVmssInstance

## Áttekintés
Elindítja a VMSS példány manuális frissítését.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az Update-AzureRmVmssInstance parancsmag a megadott virtuálisgép-készlet (VMSS-példány) kézi frissítését indítja el.
Ezt a beállítást akkor használja a rendszer, ha a VMSS-méretarány beállítása beállítás manuális értékre van állítva.

## Példák

### Példa 1: a VMSS példány frissítésének megkezdése
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

Ez a parancs elindítja a VMScaleSet001 nevű VMSS frissítését, amelynek a példány azonosítója 0.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Karakterláncként adja meg a frissítendő példány AZONOSÍTÓját vagy azonosítóit.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A VMSS erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Annak a VMSS-példánynak a nevét adja meg, amelyet a parancsmag frissít.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.

A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

###  
Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


