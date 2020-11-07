---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671434"
---
# Remove-AzBlueprintAssignment

## Áttekintés
Tervrajz-hozzárendelés eltávolítása az előfizetésből

## SZINTAXISA

### DeleteBlueprintAssignmentByName (alapértelmezett)
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteBlueprintAssignmentByObject
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Előfizetéshez rendelt tervrajz eltávolítása

## Példák

### Példa 1
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

A megadott előfizetésből megadott név alapján megadott Blueprint-hozzárendelés eltávolítása. A parancsmag a parancs végrehajtása előtt kérni fogja a megerősítést.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -InputObject
Terv hozzárendelés-objektuma.

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Terv hozzárendelésének neve.

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru Description}}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Előfizetés azonosítója: a terv-hozzárendelés üzembe helyezése.

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. commands. Blueprint. models. PSBlueprintAssignment []

## KIMENETEK

### System. Object (rendszer. objektum)
## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
