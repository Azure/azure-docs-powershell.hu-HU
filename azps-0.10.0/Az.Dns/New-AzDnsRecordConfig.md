---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: 0bc25aecae445ba18634df578de590f514640c07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844010"
---
# New-AzDnsRecordConfig

## Áttekintés
Új DNS-rekord helyi objektum létrehozása

## SZINTAXISA

### Egy
```
New-AzDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### AAAA
```
New-AzDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### NS
```
New-AzDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### MX
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### PTR
```
New-AzDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### Txt
```
New-AzDnsRecordConfig -Value <String> [<CommonParameters>]
```

### SRV
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### CName
```
New-AzDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## Leírás
A **New-AzDnsRecordConfig** parancsmag létrehoz egy helyi **DnsRecord** objektumot.
A *DnsRecords* paraméterrel megadhatja, hogy milyen rekordok kerüljenek az New-AzDnsRecordSet parancsmagba a rekordban létrehozandó rekordok megadásához.

## Példák

### 1. példa: az A típusú rekordhalmaz létrehozása
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

Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.
A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz.

### 2. példa: AAAA típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.
A Record set AAAA típusú, és 1 óra 1 óra (3600 másodperc) TTL-értékkel rendelkezik.
Egyetlen DNS-rekordot tartalmaz.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 3. példa: CNAME típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Ez a példa létrehoz egy www nevű **rekordhalmazt** a Zone myzone.com.
A Record set CNAME típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 4. példa: MX típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.
A Record set MX típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### Példa 5: NS típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

A parancs létrehoz egy ns1 nevű **rekordhalmazt** a Zone myzone.com.
A Record set NS típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 6. példa: PTR típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

A parancs létrehoz egy 4 nevű **rekordhalmazt** a 3.2.1.in-addr. arpa zónában.
A Record set a PTR típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 7. példa: SRV típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

A parancs létrehoz egy _sip. _tcp nevű **rekordhalmazt** a Zone myzone.com.
A Record set SRV típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz, amely az IP-cím 2001.2.3.4 mutat.

A szolgáltatás (SIP) és a protokoll (TCP) a rekordtípus neve részeként van megadva, nem részeként a rekord adatainak.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 8. példa: TXT típusú rekordhalmaz létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

A parancs létrehozza a myzone.com nevű **rekordhalmazt** .
A Record set TXT típusú, és 1 óra 1 óra (3600 másodperc) ÉLETTARTAMa.
Egyetlen DNS-rekordot tartalmaz.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

## PARAMÉTEREK

### -CNAME
Egy kanonikus név (CNAME rekord) tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exchange
A levelezési Exchange-kiszolgáló nevét adja meg egy MX rekordhoz.

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Egy rekord IPv4-címét adja meg.

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Az AAAA rekordok IPv6-címét adja meg.

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
A névkiszolgálói (NS) rekordok névkiszolgálói nevének megadása.

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
A szolgáltatás (SRV) rekordhoz tartozó portot adja meg.

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preferencia
Az MX rekordok beállítását adja meg.

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Prioritás
Az SRV rekordok prioritását adja meg.

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
A Pointer-erőforrás (PTR) rekord cél tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Target (cél)
Az SRV rekordok célját adja meg.

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value (érték)
A TXT rekord értékét adja meg.

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight (súly)
Az SRV rekordok vastagságát adja meg.

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordBase

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Új – AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordConfig](./Remove-AzDnsRecordConfig.md)
