---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467742"
---
# New-AzDnsRecordSet

## SYNOPSIS
Létrehoz egy DNS-rekordkészletet.

## SZINTAXIS

### Mezők (alapértelmezett)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzDnsRecordSet** parancsmag létrehoz egy új DNS-rekordkészletet, amely a megadott névvel és a megadott zónába ír be.
A **RecordSet** objektum azonos nevű és típusú DNS-rekordok készlete.
Ne feledje, hogy a név a zónához képest van, nem pedig a teljesen minősített név.
A *DnsRecords* paraméter a rekordkészlet rekordjait adja meg.
Ez a paraméter a New-AzDnsRecordConfig használatával felépített DNS-rekordok tömbje.
A folyamat operátorával **dnsZone-objektumot** is átadhat ennek a parancsmagnak, vagy  átadhatja a **DnsZone-objektumokat** zóna paraméterként, vagy másik lehetőségként név szerint is megadhatja a zónát.
A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.
Ha már létezik egy megfelelő **RecordSet** (ugyanaz a  név és rekordtípus), meg kell adnia a Felülírás paramétert, ellenkező esetben a parancsmag nem hoz létre új **RecordSetet.**

## PÉLDÁK

### 1. példa: A típusú Rekordkészlet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.
A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Egyetlen DNS-rekordot tartalmaz.

### 2. példa: AAAA típusú rekordkészlet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.
A rekordkészlet AAAA típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Egyetlen DNS-rekordot tartalmaz.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 3. példa: CNAME típusú RecordSet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ebben a példában egy www **nevű Rekordkészletet** hoz létre a myzone.com.
A rekordkészlet CNAME típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Egyetlen DNS-rekordot tartalmaz.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 4. példa: MX típusú Rekordkészlet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a parancs létrehoz egy www **nevű Rekordkészletet** a zóna myzone.com.
A rekordkészlet MX típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Egyetlen DNS-rekordot tartalmaz.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 5. példa: NS típusú rekordkészlet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a parancs létrehoz egy ns1 **nevű Rekordkészletet** a zóna myzone.com.
A rekordkészlet NS típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Egyetlen DNS-rekordot tartalmaz.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 6. példa: PTR típusú Rekordkészlet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Ez a parancs létrehoz egy 4 **nevű RecordSetet** a 3.2.1.in-addr.arpa zónában.
A rekordkészlet PTR típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Egyetlen DNS-rekordot tartalmaz.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 7. példa: SRV típusú RecordSet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a parancs létrehoz egy _sip._tcp nevű **RecordSetet** a zóna myzone.com.
A rekordkészlet típusa SRV, és TTL 1 óra (3600 másodperc) típusú.
Egyetlen DNS-rekordot tartalmaz, amely a 2001.2.3.4-es IP-címre mutat.
A szolgáltatás (sip) és a protokoll (tcp) a rekordkészlet nevének részeként van megadva, nem pedig a rekordadatok részeként.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 8. példa: TXT típusú RecordSet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a parancs létrehoz egy **RecordSet** nevű szöveget a zóna myzone.com.
A rekordkészlet a TXT típusú, és TTL értéke 1 óra (3600 másodperc).
Egyetlen DNS-rekordot tartalmaz.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 9. példa: RecordSet létrehozása a zóna csúcsán
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ezzel a paranccsal **rekordkészletet** hoz létre a zónarekordok myzone.com.
Ehhez a rekordkészlet neve "@" (a dupla idézőjelekkel együtt) lesz megadva.
A CNAME rekordok nem hozhatók létre a zóna csúcsán.
Ez a DNS-szabványok kényszere; nem korlátozza az Azure DNS-t.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 10. példa: Helyettesítő karakteres rekordkészlet létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a parancs létrehoz egy * nevű **Rekordkészletet** a zóna myzone.com.
Ez egy helyettesítő karakteres rekordkészlet.
Ha egy **rekordhalmazt** csak egy sor pn_PowerShell_short, vagy több rekordot tartalmaz egy rekordkészletet, tekintse meg az 1. példát.

### 11. példa: Üres rekordkészlet létrehozása
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Ez a parancs létrehoz egy www **nevű Rekordkészletet** a zóna myzone.com.
A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart.
Ez egy üres rekordkészlet, amely helyőrzőként működik, amelyhez később rekordokat adhat hozzá.

### 12. példa: Rekordkészlet létrehozása és az összes megerősítés mellőzése
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Ezzel a paranccsal **rekordkészletet hoz létre.**
A *Felülírás* paraméter gondoskodik arról, hogy ez a rekordkészlet felülírja az azonos nevű és típusú meglévő rekordkészleteket (a rekordkészlet meglévő rekordjai elvesznek).
A *Confirm* paraméter értéke $False a megerősítést kérő üzenet.

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

### -DnsRecords
A rekordkészletbe foglalandó DNS-rekordok tömbje.
A dns-rekordobjektumok létrehozásához New-AzDnsRecordConfig a New-AzDnsRecordConfig parancsmagot.
További információt a példákban talál.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadata
A RecordSethez társítandó metaadatok tömbje.
A metaadatok olyan névérték-párok használatával vannak megadva, amelyek kivonattáblákként vannak megadva, például @{"dept"="vásárlás";" env"="production"}.

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

### -Name
A létrehozni szükséges **RecordSet** nevét adja meg.

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

### -Felülírás
Azt jelzi, hogy ez a parancsmag felülírja a megadott **RecordSetet,** ha már létezik.

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

### -RecordType
A létrehozni szükséges DNS-rekord típusát határozza meg.
Érvényes értékek:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- A TXT SOA rekordok a zóna létrehozásakor automatikusan létrejönnek, és nem állíthatók be manuálisan.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A DNS-zónát tartalmazó erőforráscsoportot adja meg.
A zónanév megadásához *a ZoneName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy DNS Zone-objektumot *ad* át.

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Alias Target Resource Id.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
A DNS RecordSet időkorrekta (TTL) megadása.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Azt a DnsZone-t adja meg, amelyben létre kell hoznia a **RecordSet rekordkészletet.**
Másik lehetőségként a *ZoneName* és az *ResourceGroupName* paramétert használva is megadhatja a zónát.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Annak a zónának a nevét adja meg, amelyben létre kell hoznia a **RecordSet rekordkészletet.**
A zónát tartalmazó erőforráscsoportot is meg kell adnia az *ResourceGroupName* paraméterrel.
Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy DNS Zone-objektumot *ad* át.

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
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

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## KIMENETEK

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## MEGJEGYZÉSEK
A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.
A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.
Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatás előtt.
Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
