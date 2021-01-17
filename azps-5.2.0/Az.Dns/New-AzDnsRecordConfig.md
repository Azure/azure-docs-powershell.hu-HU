---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346889"
---
# New-AzDnsRecordConfig

## SYNOPSIS
Létrehoz egy új DNS-rekord helyi objektumot.

## SZINTAXIS

### A
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Aaaa
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Ns
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Mx
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Ptr
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Txt
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Srv
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Caa
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzDnsRecordConfig** parancsmag helyi **DnsRecord objektumot** hoz létre.
Ezeknek az objektumoknak egy tömbje a New-AzDnsRecordSet *DnsRecords* paramétert használva adható meg a rekordkészletben létrehozandó rekordoknak.

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
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
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

## PARAMETERS

### -CaaFlags
A hozzáadni megfelelő CAA-rekord jelzői. 0 és 255 közötti számnak kell lennie.

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
A hozzáadni megfelelő CAA-rekord címkemezője.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
Az összeadni megfelelő CAA-rekord értékmezője.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cname
Egy canonical name (CNAME) rekord tartománynevét adja meg.

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Exchange
Egy MX rekord levelezési kiszolgálójának nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Egy A rekord IPv4-címét adja meg.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Egy AAAA-rekord IPv6-címét adja meg.

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
A névkiszolgálói (NS) rekord névkiszolgálójának nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
Egy szolgáltatásrekord (SRV) portját adja meg.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preference
Az MX rekord beállítását adja meg.

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Egy SRV rekord prioritását adja meg.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Egy mutatóerőforrás (PTR) céltartománynevét adja meg.

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Target
Egy SRV rekord célértékét határozza meg.

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Érték
Egy TXT rekord értékét adja meg.

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
Az SRV rekord súlyát határozza meg.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.UInt16

### System.Byte

## KIMENETEK

### Microsoft.Azure.Commands.Dns.DnsRecordBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordConfig](./Remove-AzDnsRecordConfig.md)
