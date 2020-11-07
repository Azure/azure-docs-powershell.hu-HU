---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 21e02077e7c2644c622a3f290a82fa26d7d6fc64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669771"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## Áttekintés
A virtuális hálózati hivatkozás eltávolítása egy erőforrás-csoportból.

## SZINTAXISA

### Mezők (alapértelmezett)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzPrivateDnsVirtualNetworkLink** parancsmag véglegesen törli a privát tartománynévrendszer (DNS) hivatkozását egy adott erőforráscsoport számára.
A **PSPrivateDnsVirtualNetworkLink** -objektumokat átadhatja a *hivatkozás* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja *a* *ZoneName* és a *ResourceGroupName* paramétert is.
A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.
Ha a hivatkozást egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a csővezetéken vagy a *hivatkozás* paraméteren keresztül átadva) adja meg, a hivatkozás nem törlődik, ha az Azure Private DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását. Ez védelmet nyújt a zónák egyidejű változásaihoz. Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.

## Példák

### Példa 1: hivatkozás eltávolítása
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

Ez a parancs eltávolítja a MyResourceGroup nevű erőforráscsoport mylink csatolt myzone.com nevű hivatkozást.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
A virtuális hálózati kapcsolat objektum eltávolítása.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A törlendő hivatkozás nevét adja meg.
Meg kell adnia a *ResourceGroupName* és a *ZoneName* paramétert is.
Másik lehetőségként *a hivatkozás paramétert* használva is megadhatja a hivatkozást.

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

### -Átír
Ha a zónát egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a pipeline vagy a *hivatkozás* paraméterrel átadva) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását.
Ez védelmet nyújt a zónák egyidejű változásaihoz.
Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.

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
A művelet eredményének (logikai) elvégzéséhez használható a virtuális hálózat törlése hivatkozás a csővezetéken lejjebb.

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
Az eltávolítandó hivatkozást tartalmazó erőforráscsoport nevét adja meg.
Meg kell adnia a *ZoneName* és a *Name* paramétert is.
Azt is megteheti, hogy megadhatja a DNS-zónát egy **PSPrivateDnsVirtualNetworkLink** objektummal, amelyet a csővezetéken vagy a *hivatkozás* paraméteren keresztül adott meg.

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
A hivatkozás ARM erőforrás-AZONOSÍTÓját adja meg.

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

### -ZoneName
Annak a magánhálózati DNS-zónának a neve, amelyhez a hivatkozás társítva van.
Meg kell adnia a *ResourceGroupName* és a *Name* paramétert is.
Másik lehetőségként *a hivatkozás paramétert* használva is megadhatja a hivatkozást.

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

### Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink

### System. String

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[Új – AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
