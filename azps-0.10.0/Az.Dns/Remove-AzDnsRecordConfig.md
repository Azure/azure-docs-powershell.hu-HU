---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844009"
---
# Remove-AzDnsRecordConfig

## Áttekintés
Eltávolítja a DNS-rekordokat egy helyi rekordtípus-objektumból.

## SZINTAXISA

### Egy
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### AAAA
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### NS
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### MX
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### PTR
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### TXT
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### SRV
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### CNAME
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## Leírás
A **Remove-AzDnsRecordConfig** parancsmag a Domain Name System (DNS) rekordot egy rekorddal távolítja el.
A **Recordset** objektum kapcsolat nélküli objektum, és a változtatások nem változtatják meg a DNS-válaszokat addig, amíg a Set-AzDnsRecordSet parancsmagot nem futtatja, hogy továbbra is a Microsoft Azure DNS szolgáltatásra váltson.

Ha el szeretne távolítani egy rekordot, a rekordtípus minden mezőjének pontosan egyeznie kell.
A SOA rekordok nem vehetők fel és nem távolíthatók el.
A rendszer automatikusan létrehozza a SOA-rekordokat, amikor létrejön egy DNS-zóna, és automatikusan törlődik a DNS-zóna törlésekor.

A **rekordhalmaz** -objektumot paraméterként vagy a pipeline operátor segítségével átadhatja erre a parancsmagra.

## Példák

### 1. példa: rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

Ez a példa egy meglévő rekordtípus rekordjainak eltávolítását adja meg.
Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

### 2. példa: az AAAA rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

Ez a példa eltávolítja az AAAA-rekordot egy meglévő rekorddal.
Ha ez a rekord csak a rekordban van, akkor az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

### 3. példa: CNAME rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

Ez a példa eltávolítja a CNAME rekordot egy meglévő rekordból.
Mivel a CNAME rekord legfeljebb egy rekordban szerepelhet, az eredmény egy üres rekord.

### 4. példa: MX rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

Ebben a példában egy MX rekord törlődik egy meglévő rekordból.
A "@" rekord a zóna APEX nevű rekordjait jelzi.
Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

### Példa 5: a NÉVKISZOLGÁLÓI rekordok eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

Ez a példa eltávolítja a NÉVKISZOLGÁLÓI rekordokat egy meglévő rekordból.
Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

### Példa 6: a PTR rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

Ez a példa eltávolítja a PTR rekordot egy meglévő rekordból.
Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

### 7. példa: SRV rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

Ez a példa eltávolítja az SRV rekordot egy meglévő rekorddal.
Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

### 8. példa: TXT rekord eltávolítása a rekordból
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

Ez a példa eltávolítja a TXT rekordot egy meglévő rekordból.
Ha ez az egyetlen rekord a rekordban, az eredmény egy üres rekord.
Ha teljes egészében el szeretné távolítani a rekordot, olvassa el az Eltávolítás – AzDnsRecordSet című témakört.

## PARAMÉTEREK

### -CNAME
Egy kanonikus név (CNAME rekord) tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: CNAME
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
Parameter Sets: MX
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
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
A névkiszolgálói (NS) rekordok névkiszolgálói rekordjait adja meg.

```yaml
Type: String
Parameter Sets: NS
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
Parameter Sets: SRV
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
Parameter Sets: MX
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
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
A Pointer (PTR) rekord cél tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordSet
Megadja az eltávolítandó rekordot tartalmazó **Recordset** objektumot.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Target (cél)
Az SRV rekordok célját adja meg.

```yaml
Type: String
Parameter Sets: SRV
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
Parameter Sets: TXT
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
Parameter Sets: SRV
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

### Microsoft. Azure. Command. DNS. DnsRecordSet
Ezt a parancsmagot a **DnsRecordSet** -objektum pipe-ra kapcsolhatja.
Ez a rekord kapcsolat nélküli képviselete, és a frissítés nem módosítja a DNS-válaszokat addig, amíg a set-AzDnsRecordSet nem futtatja.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet
Ez a parancsmag a módosított **Recordset** objektumot számítja ki.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
