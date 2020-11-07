---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671969"
---
# Remove-AzureRmFrontDoor

## Áttekintés
A bejárati ajtó kiegyenlítő eltávolítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByFieldsParameterSet (alapértelmezett)
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmFrontDoor** parancsmag a jelenlegi előfizetés alatt eltávolítja az első ajtót.

## Példák

### 1. példa: a "frontdoor1" szó eltávolítása a jelenlegi előfizetés alatti "rg1" erőforráscsoporthoz
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

A jelenlegi előfizetés alatti "rg1" erőforráscsoport "frontdoor1" eltávolítása.

### 2. példa: a jelenlegi előfizetés alatti "rg1" erőforráscsoport összes FrontDoors eltávolítása.
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

Távolítsa el az összes FrontDoors az erőforráscsoport "rg1" csoportjában az aktuális előfizetésben.

### 3. példa: az összes FrontDoors eltávolítása az aktuális előfizetésből.
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

Az összes FrontDoors eltávolítása a jelenlegi előfizetésből.

### Példa 4: az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

Az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -InputObject
A törlendő bejárati ajtó objektuma.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A törlendő bejárati ajtó neve.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Visszatérési objektum (ha meg van adva)

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

### -ResourceGroupName
Az az erőforráscsoport, amelyhez az első ajtó tartozik.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A törlendő bejárati ajtó erőforrás-azonosítója

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
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

### Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor

### System. String

### System. Management. Automation. SwitchParameter

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
