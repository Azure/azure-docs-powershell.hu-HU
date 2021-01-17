---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466675"
---
# Remove-AzPrivateDnsZone

## SYNOPSIS
Eltávolít egy privát DNS-zónát egy erőforráscsoportból.

## SZINTAXIS

### Mezők (alapértelmezett)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Remove-AzPrivateDnsZone** parancsmag véglegesen töröl egy privát DNS-zónát egy adott erőforráscsoportból.
A zónában található összes rekordkészlet is törlődik.
A **PrivateDnsZone-objektumokat** a *PrivateZone* paraméterrel vagy a folyamat műveleti jelével, illetve a *Name* and *ResourceGroupName* paraméter megadásával is átadhatja.
A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.
Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **PrivateDnsZone** objektum beolvasása óta (csak a DNS-zóna erőforrásszámán végrehajtott műveletek módosulnak, a rekordkészletek műveletei a zónán belül nem).
Ez védelmet nyújt a párhuzamos zónaváltozások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.

## PÉLDÁK

### 1. példa: Privát zóna eltávolítása
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Ez a parancs eltávolítja a myzone.com myResourceGroup nevű erőforráscsoportból.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Name
A parancsmag által eltávolított privát DNS-zóna neve.
Az *ResourceGroupName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a DNS-zónát a *Zone paraméter* használatával.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Felülírás
Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **PrivateDnsZone** objektum beolvasása óta (csak a DNS-zóna erőforrásszámán végrehajtott műveletek módosulnak, a rekordkészletek műveletei a zónán belül nem).
Ez védelmet nyújt a párhuzamos zónaváltozások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
A művelet eredményének (logikai) a folyamaton belül távolabbi privát zóna törlésére használható.

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

### -PrivateZone
A törölni kívánt privát zónaobjektum.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Az eltávolítható zónát tartalmazó erőforráscsoport neve.
A *ZoneName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a DNS-zóna értékét egy **PrivateDnsZone** objektummal, amely vagy a folyamaton, vagy a Zone paraméteren keresztül *továbbítható.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Private DNS Zone ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

### System.String

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
