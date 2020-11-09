---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301271"
---
# Set-AzPrivateDnsVirtualNetworkLink

## Áttekintés
Frissítések/virtuális hálózati kapcsolat bekapcsolása egy privát zónával és egy erőforrás-csoporthoz társítva.

## SZINTAXISA

### Mezők (alapértelmezett)
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Objektum
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzPrivateDnsVirtualNetworkLink** parancsmag frissíti a megadott erőforráscsoport zónájával társított hivatkozást.
A **PSPrivateDnsVirtualNetworkLink** -objektumokat átadhatja a *hivatkozás* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja *a* *ZoneName* és a *ResourceGroupName* paramétert is.
A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.
Ha a zónát egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a pipeline vagy a *hivatkozás* paraméterrel átadva) adja meg, a hivatkozás nem frissül, ha az Azure DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását. Ez védelmet nyújt az egyidejű kapcsolatok változásaihoz. Ezt a *felülírási* paraméter segítségével lehet letiltani, amely a hivatkozásokat az egyidejű módosításoktól függetlenül frissíti.

## Példák

### Példa 1: hivatkozás beállítása
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

Ez a parancs beállítja a IsRegistrationEnabled a mylink nevű hivatkozáshoz a MyResourceGroup nevű erőforráscsoport myzone.com nevű zónájához társítva.

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
A beállítani kívánt virtuális hálózati kapcsolat objektum.

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

### -IsRegistrationEnabled
Logikai érték, amely azt jelzi, hogy engedélyezve van-e a regisztráció a virtuális hálózaton hivatkozás.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a hivatkozásnak a neve, amely a parancsmagot eltávolítja.
Meg kell adnia a *ResourceGroupName* és a *ZoneName* paramétert is.
Azt is megteheti, hogy a *hivatkozás* paraméterrel megadhatja a magánhálózati DNS-hivatkozást.

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
Ha a hivatkozást egy **PSPrivateDnsVirtualNetworkLink** -objektummal (a csővezetéken vagy a *hivatkozás* paraméteren keresztül átadva) adja meg, a hivatkozás nem törlődik, ha az Azure DNS-ben módosította a helyi **PSPrivateDnsVirtualNetworkLink** objektum beolvasását.
Ez védelmet nyújt az egyidejű kapcsolatok változásaihoz.
Ezt a *felülírási* paraméter használatával lehet letiltani, amely a hivatkozásokat az egyidejű módosításoktól függetlenül törli.

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

### -ResourceGroupName
Az eltávolítandó hivatkozást tartalmazó erőforráscsoport nevét adja meg.
Meg kell adnia a *ZoneName* és a *Name* paramétert is.
Azt is megteheti, hogy megadhatja a virtuális hálózati hivatkozást egy **PSPrivateDnsVirtualNetworkLink** objektummal, amelyet a csővezetéken vagy a *hivatkozás* paraméteren keresztül adott meg.

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
Privát DNS-zóna ResourceID.

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

### -Címke
Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneName
A parancsmag által eltávolított DNS-zóna nevét adja meg.
A *Name* és a *ResourceGroupName* paramétert is meg kell adnia.
Azt is megteheti, hogy a *hivatkozás* paraméterrel megadhatja a magánhálózati DNS-hivatkozást.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink

### System. String

## KIMENETEK

### Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsVirtualNetworkLink

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[Új – AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
