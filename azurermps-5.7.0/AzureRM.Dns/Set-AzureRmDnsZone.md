---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493132"
---
# Set-AzureRmDnsZone

## Áttekintés
Frissíti egy DNS-zóna tulajdonságait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Mezők (alapértelmezett)
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FieldsObjects
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmDnsZone** parancsmag frissíti a megadott DNS-zónát az Azure DNS szolgáltatásban.
Ez a parancsmag nem frissíti a rekordokat a zónában.

Átadhatja a **dnsZone** -objektumokat paraméterként vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.

A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.

Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását. Ez védelmet nyújt az egyidejű módosítások számára. Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.

## Példák

### Példa 1: DNS-zóna frissítése
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

Az első parancs a megadott erőforráscsoporthoz tartozó myzone.com nevű zónát kapja, majd a $Zone változóban tárolja.

A második parancs frissíti az $Zone címkéit.

A végleges parancs véglegesíti a módosítást.

### 2. példa: a zóna címkék frissítése
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Ez a parancs frissíti a myzone.com nevű zóna címkéit anélkül, hogy először explicit módon kapja meg a zónát.

### 3. példa: privát zóna társítása virtuális hálózattal az AZONOSÍTÓjának megadásával
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

Ez a parancs az AZONOSÍTÓjának megadásával társítja a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet.

### Példa 4: privát zóna virtuális hálózattal való társítása a hálózati objektum megadásával.
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

Ez a parancs a magánhálózati DNS-zóna myprivatezone.com a virtuális hálózati myvnet a regisztrációs hálózatként társítja úgy, hogy a Set-AzureRmDnsZone parancsmag által képviselt virtuális hálózati objektumot átadja $vnet változónak.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
A frissítendő DNS-zóna nevét adja meg.

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Átír
Ha egy DNS-zónát objektumként (a Zone objektummal vagy a csővezetéken keresztül) továbbít át, az nem frissül, ha az Azure DNS-ben módosította a helyi DnsZone objektum beolvasását. Ez védelmet nyújt az egyidejű módosítások számára. Ezt a működést a *felülírási* paraméterrel elvégezheti, amely az egyidejű módosításoktól függetlenül frissíti a zónát.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
Azoknak a virtuális hálózatoknak a listája, amelyek regisztrálják a Virtual Machine-állomásnevek rekordjait ebben a DNS-zónában, csak a privát zónákhoz.

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
Azoknak a virtuális hálózati azonosítóknak a listája, amelyek a virtuális gép állomásnevek rekordjait a DNS-zónában regisztrálják, csak a privát zónákhoz.

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
A virtuális hálózatok listája, amelyekkel megoldhatja a DNS-zóna rekordjait, csak a privát zónákhoz.

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
Azon virtuális hálózati azonosítók listája, amelyek képesek a DNS-zónában lévő rekordok megoldására, csak a privát zónákhoz.

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
A frissítendő zónát tartalmazó erőforráscsoport nevét adja meg.
Meg kell adnia a ZoneName paramétert is.

Azt is megteheti, hogy a zónát egy DnsZone-objektummal, a *Zone* paraméterrel vagy a csővezetékkel is megadhatja.

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
A frissítendő DNS-zónát adja meg.

Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
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

### Microsoft. Azure. Command. DNS. DnsZone
Ezt a parancsmagot a DnsZone-objektum pipe-ra kapcsolhatja.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsZone
Ez a parancsmag egy DnsZone-objektumot ad eredményül, amely a frissített DNS-zónát egy új ETAG jelképezi.

## MEGJEGYZI
A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.
A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.

Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[Új – AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)
