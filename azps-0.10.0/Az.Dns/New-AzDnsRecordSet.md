---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: 0327837f6e28d7147892669bd77b1aa78747a5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844006"
---
# New-AzDnsRecordSet

## Áttekintés
DNS-rekordot hoz létre.

## SZINTAXISA

### Mezők
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzDnsRecordSet** PARANCSMAG új DNS-rekordot hoz létre a megadott névvel és típussal a megadott zónában.
A **rekordhalmaz** -objektum a DNS-rekordok halmaza, azonos névvel és típussal.
Ne feledje, hogy a név a zónához viszonyítva nem a teljesen minősített név.

A *DnsRecords* paraméter a rekordtípus rekordjait adja meg.
Ez a paraméter a DNS-rekordok egy sorát veszi igénybe, amelyet a New-AzDnsRecordConfig-ban építettek.

A pipeline operátor segítségével átadhatja a **dnsZone** -objektumot erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, illetve a zóna név szerint is megadható.

A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.

Ha egy megfelelő **rekordhalmaz** már létezik (ugyanaz a név és a rekordtípus), meg kell adnia a *felülírási* paramétert, különben a parancsmag nem hoz létre új **rekordhalmazt** .

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

### 9. példa: rekordhalmaz létrehozása a Zone APEX-on
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

A parancs létrehoz egy **rekordhalmazt** a zóna myzone.com csúcsán (vagy gyökerénél).
Ehhez a rekordtípus neve "@" (a dupla idézőjelekkel együtt) van megadva.

Nem hozhatók létre CNAME rekordok a zóna csúcsán.
Ez a DNS-szabványok kényszere; Az Azure DNS-t nem korlátozhatja.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 10 példa: helyettesítőkarakter-rekord létrehozása
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

A parancs létrehozza a * nevű **rekordhalmazt** a Zone myzone.com.
Ez egy helyettesítőkarakter-rekord.

Ha olyan **rekordhalmazt** szeretne létrehozni, amely csak egy pn_PowerShell_short, vagy több rekordot tartalmazó rekorddal szeretne létrehozni, olvassa el a példa 1 értéket.

### 11-es példa: üres rekord létrehozása
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

A parancs a www nevű **rekordhalmazt** hoz létre a Zone myzone.com.
A Record set a Type A és 1 óra (3600 másodperc) ÉLETTARTAMa.
Ez egy üres rekord, amely helyőrzőként működik, majd később rekordokat adhat hozzájuk.

### 12-es példa: a rekordtípus létrehozása és az összes megerősítés tiltása
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

A parancs létrehozza a **rekordhalmazt**.
A *felülírási* paraméter biztosítja, hogy a rekord felülírja a meglévő, azonos nevű és típusú rekordokat (az adott rekordban meglévő rekordok elvesznek).
A *Confirm* paraméter $false értékkel letiltja a megerősítési üzenetet.

## PARAMÉTEREK

### -DnsRecords
A rekordban szerepeltetni kívánt DNS-rekordok tömbjét adja meg.
A New-AzDnsRecordConfig parancsmaggal DNS-rekord objektumokat hozhat létre.
További információért olvassa el a példákat.

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Ez a paraméter érvénytelenítve van ennél a parancsmagnál.
A program eltávolítja a jövőbeli kiadásokban.

Ha meg szeretné állapítani, hogy a parancsmag kéri-e a comfirmation, használja a *Confirm* paramétert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
A rekordhalmazhoz társítani kívánt metaadatok tömbjét adja meg.
A metaadatok a hash-táblázatként megjelölt név-érték párokkal, például @ (@ {"név" = "dept"; "Érték" = "Shopping"}, @ {"név" = "env"; "Value" = "termelés"})

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A létrehozandó **rekordhalmaz** nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Átír
Jelzi, hogy ez a parancsmag felülírja a megadott **rekordhalmazt** , ha már létezik.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordType
A létrehozandó DNS-rekord típusát adja meg.

Az érvényes értékek a következők:

- Egy
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT

A SOA rekordok automatikusan létrejönnek a zóna létrehozásakor, és nem hozhatók létre manuálisan.

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A DNS-zónát tartalmazó erőforráscsoportot adja meg.
A zóna nevének megadásához meg kell adnia a *ZoneName* paramétert is.

Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TTL (TTL)
A DNS-rekordhalmaz élettartamának (TTL) értékét adja meg.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
Annak a DnsZone a meghatározása, amelyben a **rekordhalmazt** létre szeretné hozni.
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

### -ZoneName
Annak a zónának a nevét adja meg, amelybe a **rekordhalmazt** létre szeretné hozni.
Meg kell adnia a zónát tartalmazó erőforráscsoportot is a *ResourceGroupName* paraméter használatával.

Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. DNS. DnsZone
Ezt a parancsmagot a DnsZone-objektum pipe-ra kapcsolhatja.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet
Ez a parancsmag egy **Recordset** objektumot ad eredményül.

## MEGJEGYZI
A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.
A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.

Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[Új – AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
