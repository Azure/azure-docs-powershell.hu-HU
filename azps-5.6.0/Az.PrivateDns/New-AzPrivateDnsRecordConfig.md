---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: b07e04d542b172d535f715fda82387d06234c15a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921658"
---
# New-AzPrivateDnsRecordConfig

## SYNOPSIS
Létrehoz egy új privát DNS-rekord helyi objektumot.

## SZINTAXIS

### A (alapértelmezett)
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AAAA
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### MX
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PTR
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TXT
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CNAME
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A New-AzPrivateDnsRecordConfig helyi PSPrivateDnsRecord objektumot hoz létre. Az objektumok tömbje a New-AzPrivateDnsRecordSet PrivateDnsRecord paraméterrel adható meg a rekordkészletben létrehozandó rekordok megadásához.

## PÉLDÁK

### 1. példa: A típusú Rekordkészlet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com. A rekordkészlet "A" típusú, és TTL-t (1 óra) (3600 másodperc) tart. Egyetlen privát DNS-rekordot tartalmaz.

### 2. példa: AAAA típusú rekordkészlet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com. A rekordkészlet AAAA típusú, és TTL-t (1 óra) (3600 másodperc) tart. Egyetlen privát DNS-rekordot tartalmaz. Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.

### 3. példa: CNAME típusú RecordSet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

Ebben a példában egy www nevű Rekordkészletet hoz létre a myzone.com. A rekordkészlet CNAME típusú, és TTL-t (1 óra) (3600 másodperc) tart. Egyetlen privát DNS-rekordot tartalmaz. Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.

### 4. példa: MX típusú Rekordkészlet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

Ez a parancs létrehoz egy www nevű RecordSetet a privát zóna myzone.com. A rekordkészlet MX típusú, és TTL-t (1 óra) (3600 másodperc) tart. Egyetlen privát DNS-rekordot tartalmaz. Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.

### 5. példa: PTR típusú Rekordkészlet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

Ez a parancs létrehoz egy 4 nevű RecordSetet a 3.2.1.in-addr.arpa privát zónában. A rekordkészlet PTR típusú, és TTL-t (1 óra) (3600 másodperc) tart. Egyetlen privát DNS-rekordot tartalmaz. Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.

### 6. példa: SRV típusú Rekordkészlet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

Ez a parancs létrehoz egy _sip._tcp nevű RecordSetet a myzone.com. A rekordkészlet típusa SRV, és TTL-1 óra (3600 másodperc) típusú. Egyetlen privát DNS-rekordot tartalmaz, amely a 2001.2.3.4-es IP-címre mutat. A szolgáltatás (sip) és a protokoll (tcp) a rekordkészlet nevének részeként van megadva, nem pedig a rekordadatok részeként. Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.

### 7. példa: TXT típusú RecordSet létrehozása
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

Ez a parancs létrehoz egy RecordSet nevű szöveget a privát zóna myzone.com. A rekordkészlet a TXT típusú, és TTL értéke 1 óra (3600 másodperc). Egyetlen privát DNS-rekordot tartalmaz. Ha csak egy sorból vagy több rekordból pn_PowerShell_short rekordkészletet, akkor a rekordhalmaz létrehozásához lásd az 1. példát.

## PARAMETERS

### -Cname
Az összeadni képes CNAME rekord canonical neve.
Nem lehet a zóna nevéhez képest.
Nem lehet befejezési pont

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
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

### -Exchange
A hozzáadni megfelelő MX rekord levelezési szolgáltatója.
Nem lehet a zóna nevéhez képest.
Nem lehet befejezési pont

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv4Address
Az A rekord IPv4-címe.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv6Address
Az AAAA rekord hozzáadni használt IPv6-címe.

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
A hozzáadni megfelelő SRV rekord portszáma.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Preference
A hozzáadni kiválasztott MX rekord beállításértéke.

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
A hozzáadni célként megadott SRV rekord.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ptrdname
A hozzáadni megfelelő PTR-rekord cél állomása.
Nem lehet a zóna nevéhez képest.
Nem lehet befejezési pont

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target
Az hozzáadni cél állomása az SRV rekordhoz.
Nem lehet a zóna nevéhez képest.
Nem lehet befejezési pont

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Érték
Az összeadni megfelelő TXT rekord szöveges értéke.

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
Az összeadni megfelelő SRV rekord súlyértéke.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
