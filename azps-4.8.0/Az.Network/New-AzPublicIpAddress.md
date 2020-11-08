---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 3bfed7f4c980ab246f4e38d500860ccd4e2ef09f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024607"
---
# New-AzPublicIpAddress

## Áttekintés
Nyilvános IP-címet hoz létre.

## SZINTAXISA

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzPublicIpAddress** PARANCSMAG nyilvános IP-címet hoz létre.

## Példák

### Példa 1: új nyilvános IP-cím létrehozása
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva. A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva. Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó).

### 2. példa: nyilvános IP-cím létrehozása fordított FQDN-vel
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. A-ReverseFqdn paraméterrel az Azure létrehoz egy DNS-PTR rekordot (fordított) az erőforráshoz rendelt nyilvános IP-címhez, mutatva a parancsban megadott $customFqdn. Előfeltételként a $customFqdn (Say webapp.contoso.com) DNS-CNAME rekordot (címkeresési) kell mutatnia a $dnsPrefix. $location. cloudapp.azure.com.

### 3. példa: új nyilvános IP-cím létrehozása a IpTag
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva. A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz, mert a-AllocationMethod a "statikus" értékkel van meghatározva. Ha a beállítás értéke "dinamikus", a rendszer csak akkor kapja meg a nyilvános IP-címet, ha elindítja (vagy hozza létre) a kapcsolódó erőforrást (például VM vagy terheléselosztó). A Iptag az erőforráshoz társított címkéket használja. A Iptag megadható New-AzPublicIpTag és átadva a-IpTags.

### Példa 4: új nyilvános IP-cím létrehozása előtagból
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

A parancs létrehoz egy új nyilvános IP-cím típusú erőforrást. Létrejön egy DNS-rekord a $dnsPrefix. $location. cloudapp.azure.com az erőforrás nyilvános IP-címére mutatva. A rendszer azonnal hozzárendeli a nyilvános IP-címet az erőforráshoz a megadott publicIpPrefix.
Ezt a lehetőséget csak a "standard" SKU és a "Static" AllocationMethod támogatja.

## PARAMÉTEREK

### -AllocationMethod
Azt a módszert adja meg, amellyel a nyilvános IP-címet kioszthatja.
A paraméter elfogadható értékei: static vagy Dynamic.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
A parancsmag futtatása a háttérben

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DomainNameLabel
Egy nyilvános IP-cím relatív DNS-nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -IdleTimeoutInMinutes
Az üresjárati időtúllépést adja meg percben kifejezve.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAddressVersion
Az IP-cím verziószámát adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
IpTag lista.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Azt a régiót adja meg, amelybe nyilvános IP-címet szeretne létrehozni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak a nyilvános IP-címnek a nevét adja meg, amelyet a parancsmag hoz létre.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpPrefix
Azt a PSPublicIpPrefix adja meg, amelyből a nyilvános IP-címet le szeretné foglalni.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amelybe nyilvános IP-címet szeretne létrehozni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseFqdn
Egy teljesen minősített tartománynevet ad meg (FQDN).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
A nyilvános IP-cím neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### System. String

### Microsoft. Azure. commands. Network. models. PSPublicIpTag []

### Microsoft. Azure. commands. Network. models. PSPublicIpPrefix

### System. Int32

### System. string []

### System. Collections. Hashtable

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSPublicIpAddress

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Set-AzPublicIpAddress](./Set-AzPublicIpAddress.md)
