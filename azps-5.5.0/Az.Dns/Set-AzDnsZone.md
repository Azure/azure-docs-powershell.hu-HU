---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153219"
---
# Set-AzDnsZone

## SYNOPSIS
Frissíti egy DNS-zóna tulajdonságait.

## SZINTAXIS

### Mezők (alapértelmezett)
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FieldsObjects
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.
Ez a parancsmag nem frissíti a zónában található rekordkészleteket.
A **DnsZone-objektumokat** átadhatja paraméterként vagy a folyamat műveleti jelének használatával, vagy másik lehetőségként megadhatja a *ZoneName* és *az ResourceGroupName* paramétert.
A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.
Ha egy DNS-zóna objektumként (a Zone objektum használatával vagy a folyamaton keresztül) halad át, akkor az nem frissül, ha az Azure DNS-ben módosult a helyi DnsZone-objektum lekérése óta. Ez védelmet nyújt az egyidejű módosítások számára. Ezt a viselkedést  letilthatja a Felülírás paraméterrel, amely az egyidejű módosításoktól függetlenül frissíti a zónát.

## PÉLDÁK

### 1. példa: DNS-zóna frissítése
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

Az első parancs lekérte a myzone.com nevű zónát a megadott erőforráscsoportból, majd a $Zone tárolja.
A második parancs frissíti a $Zone.
Az utolsó parancs véglegesen véglegesi a változtatást.

### 2. példa: Zóna címkéinek frissítése
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Ez a parancs anélkül frissíti az myzone.com zóna címkéit, hogy először explicit módon bevené a zónát.

### 3. példa: Privát zóna társítása virtuális hálózathoz az azonosító megadásával
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

Ez a parancs a személyes DNS-zóna myprivatezone.com a myvnet virtuális hálózathoz regisztrációs hálózatként társítja az azonosító megadásával.

### 4. példa: Privát zóna társítása virtuális hálózathoz a hálózati objektum megadásával.
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

Ez a parancs regisztrációs hálózatként társítja a myprivatezone.com dns-zónazónát a myvnet virtuális hálózattal úgy, hogy a $vnet változó által képviselt virtuális hálózati objektumot továbbítja a Set-AzDnsZone parancsmagnak.

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
A frissítenie kell DNS-zóna nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Felülírás
Ha egy DNS-zóna objektumként (a Zone objektum használatával vagy a folyamaton keresztül) halad át, akkor az nem frissül, ha az Azure DNS-ben módosult a helyi DnsZone-objektum lekérése óta. Ez védelmet nyújt az egyidejű módosítások számára. Ezt a viselkedést  letilthatja a Felülírás paraméterrel, amely az egyidejű módosításoktól függetlenül frissíti a zónát.

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

### -RegistrationVirtualNetwork
A virtuális hálózatok listája, amelyek a virtuális gép állomásneveit regisztrálják ebben a DNS-zónában, csak privát zónákhoz érhetők el.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
A virtuális hálózati adatok azon listája, amelyek a virtuális gép állomásnevének rekordjait regisztrálják ebben a DNS-zónában, csak privát zónákhoz érhetők el.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
Az ebben a DNS-zónában lévő rekordok feloldására képes virtuális hálózatok listája, amelyek csak privát zónákban érhetők el.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
Az ebben a DNS-zónában lévő rekordok feloldására képes virtuális hálózati adatok listája, amelyek csak privát zónákban érhetők el.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amely a frissíteni kívánt zónát tartalmazza.
A ZoneName paramétert is meg kell adnia.
Másik lehetőségként megadhatja a zónát egy DnsZone-objektummal a *Zone* paraméterrel vagy a folyamattal.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Kulcsérték-párok kivonattábla formájában. Például: @{key0="érték0";key1=$null;key2="érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Megadja a frissítenie kell a DNS-zónát.
Másik lehetőségként a *ZoneName* és az *ResourceGroupName* paramétert használva is megadhatja a zónát.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Collections.Hashtable

### System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### Microsoft.Azure.Commands.Dns.DnsZone

## KIMENETEK

### Microsoft.Azure.Commands.Dns.DnsZone

## MEGJEGYZÉSEK
A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.
A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.
Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatás előtt.
Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
