---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 37cd1f7b00cbfae6421b5dab06ce87c0f462434c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670898"
---
# Get-AzDnsRecordSet

## Áttekintés
Megkapja a DNS-rekord halmazát.

## SZINTAXISA

### Mezők
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objektum
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDnsRecordSet** parancsmag a megadott névvel és típussal kapja meg a DNS-rekordot a megadott zónában.
Ha nem adja meg a *név* -vagy *RecordType* paramétert, ez a parancsmag a megadott típusú rekord összes rekordját visszaadja a zónában.
Ha a *RecordType* paramétert adja meg, a *Name* paramétert azonban nem, ez a parancsmag a megadott rekordtípus összes rekordját adja eredményül.
A pipeline operátor segítségével átadhatja a **dnsZone** -objektumokat erre a parancsmagra, vagy átadhatja a **dnsZone** -objektumot a *zóna* paraméterének, vagy másik lehetőségként a zóna és az erőforráscsoport név szerint is megadható.

## Példák

### 1. példa: a bejegyzéstípusok beolvasása megadott névvel és típussal
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Ez a parancs a Record Type (rekord) típusú rekordot kapja meg a megadott erőforráscsoport és zóna mezőben, majd a $RecordSet változóban tárolja.
Mivel a *név* -és *RecordType* paraméterek meg vannak adva, csak egy **rekordhalmaz** -objektum van visszaadva.

### 2. példa: megadott típusú bejegyzéstípusok beszerzése
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Ez a parancs a Record Type (A-es) myzone.com egy sorát kapja meg a MyResourceGroup nevű erőforráscsoport nevű zónában, majd a $RecordSets változóban tárolja őket.

### 3. példa: a zóna minden rekordjának beolvasása
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Ez a parancs a MyResourceGroup nevű myzone.com nevű zónában minden rekord halmazát beolvassa, majd a $RecordSets változóban tárolja.

### Példa 4: egy zóna összes rekordjának beolvasása DnsZone objektum használatával
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Ez a példa a fenti 3 példával egyenértékű.
Ebben az esetben a zóna zóna objektummal van megadva.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
A beolvasott **rekordhalmaz** nevét adja meg.
Ha nem adja meg a *Name* paramétert, a függvény a megadott típusú összes rekordot adja vissza.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
A parancsmag által kapott DNS-rekord típusát adja meg.
Az érvényes értékek a következők: 
- Egy
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT: Ha nem adja meg a *RecordType* paramétert, akkor a *Name* paramétert is el kell hagynia. Ezzel a parancsmaggal a zóna minden rekordját visszaadja (minden név és típus).

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A DNS-zónát tartalmazó erőforráscsoportot adja meg.
A zóna nevét a *ZoneName* paraméter használatával is meg kell adni.
Másik lehetőségként megadhatja a zóna és az erőforráscsoport értékét egy **dnsZone** -objektum átadásával a *Zone* paraméter használatával.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
Azt a DNS-zónát adja meg, amely a parancsmag által beolvasott rekordot tartalmazza.
Azt is megteheti, hogy a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a zónát.

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

### -ZoneName
A beolvasott rekordot tartalmazó DNS-zóna nevét adja meg.
A zónát tartalmazó erőforráscsoportot is meg kell adni a *ResourceGroupName* paraméter használatával.
Azt is megteheti, hogy megadhatja a zóna és az erőforráscsoport értékét a DNS Zone objektum átadásával a *Zone* paraméterrel.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DNS. DnsZone

### System. null ' 1 [[Microsoft. Azure. Management. DNS. models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


