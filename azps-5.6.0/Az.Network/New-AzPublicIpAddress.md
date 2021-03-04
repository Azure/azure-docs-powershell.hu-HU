---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: b3ea1ab3bbe3edbc72b81c25817af40e9e5fc2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921729"
---
# New-AzPublicIpAddress

## SYNOPSIS
Nyilvános IP-címet hoz létre.

## SZINTAXIS

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzPublicIpAddress** parancsmag létrehoz egy nyilvános IP-címet.

## PÉLDÁK

### 1. példa: Új nyilvános IP-cím létrehozása
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

Ez a parancs új nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat. A rendszer azonnal hozzárendel egy nyilvános IP-címet ehhez az erőforráshoz, mivel a -AllocationMethod "Static" (Statikus) értékként van megadva. Ha a "Dinamikus" értéket adja meg, akkor a nyilvános IP-címeket csak akkor kapja meg a rendszer, amikor elindítja (vagy létrehozza) a társított erőforrást (például vm vagy load balancer).

### 2. példa: Nyilvános IP-cím létrehozása fordított FQDN-sel
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

Ez a parancs új nyilvános IP-címforrást hoz létre. A -ReverseFqdn paraméterrel az Azure létrehoz egy DNS PTR-rekordot (visszakeresés) az erőforráshoz hozzárendelt nyilvános IP-címhez, amely a $customFqdn megadott rekordra mutat. Előfeltételeként a $customFqdn (például webapp.contoso.com) dns CNAME rekordnak (forward-lookup) kell lennie, amely a $dnsPrefix.$location.cloudapp.azure.com címre mutat.

### 3. példa: Új nyilvános IP-cím létrehozása iptaggal
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

Ez a parancs új nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat. A rendszer azonnal hozzárendel egy nyilvános IP-címet ehhez az erőforráshoz, mivel a -AllocationMethod "Static" (Statikus) értékként van megadva. Ha a "Dinamikus" értéket adja meg, akkor a nyilvános IP-címeket csak akkor kapja meg a rendszer, amikor elindítja (vagy létrehozza) a társított erőforrást (például vm vagy load balancer). Az Ip-címke az erőforráshoz társított címkékhez használatos. Az IP-cím megadva a New-AzPublicIpTag és az -IpTags protokollon keresztül bemenetként is át lehet adni.

### 4. példa: Új nyilvános IP-cím létrehozása előtagból
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

Ez a parancs új nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat. A rendszer azonnal hozzárendel egy nyilvános IP-címet ehhez az erőforráshoz a megadott publicIpPrefix értékből.
Ez a lehetőség csak a "Standard" termékváltozat és a "Statikus" TerhelésiMethod esetén támogatott.

### 5. példa: Új globális nyilvános IP-cím létrehozása
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

Ez a parancs egy új globális nyilvános IP-címforrást hoz létre. Létrejön egy DNS-rekord a $dnsPrefix.$location.cloudapp.azure.com webhelyhez, amely az erőforrás nyilvános IP-címére mutat. Az erőforráshoz azonnal hozzárendel egy globális nyilvános IP-címet.
Ez a lehetőség csak a "Standard" termékváltozat és a "Statikus" TerhelésiMethod esetén támogatott.

## PARAMETERS

### -AllocationMethod
Megadja, hogy milyen módszerrel osztja ki a nyilvános IP-címet.
A paraméter elfogadható értékei a következőek: Statikus vagy dinamikus.

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
Parancsmag futtatása a háttérben

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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
A nyilvános IP-címek relatív DNS-nevét adja meg.

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
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

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
Az üresjárati időkorrekt percben adja meg.

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
Az IP-cím verzióját adja meg.

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
IpTag-lista.

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

### -Location
Azt a régiót adja meg, amelyben nyilvános IP-címet kell létrehozni.

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

### -Name
A parancsmag által létrehozott nyilvános IP-cím neve.

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
Azt a PSPublicIpPrefixet adja meg, amelyből kiosztja a nyilvános IP-címet.

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
Annak az erőforráscsoportnak a nevét adja meg, amelyben nyilvános IP-címet kell létrehozni.

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
Egy fordított, teljesen minősített tartománynevet (FQDN) ad meg.

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

### -Termékváltozat
A nyilvános IP-termékváltozat neve.

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

### -Tag
Kulcsérték-párok kivonattábla formájában. Például: @{key0="érték0";key1=$null;key2="érték2"}

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

### -Tier
A nyilvános IP-termékváltozatréteg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]

### Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix

### System.Int32

### System.String[]

### System.Collections.Hashtable

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Set-AzPublicIpAddress](./Set-AzPublicIpAddress.md)
