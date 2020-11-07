---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844033"
---
# Get-AzDnsRecordSet

## Áttekintés
Megkapja a DNS-rekord halmazát.

## SZINTAXISA

### Mezők
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### Objektum
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
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

### -Name (név)
A beolvasott **rekordhalmaz** nevét adja meg.
Ha nem adja meg a *Name* paramétert, a függvény a megadott típusú összes rekordot adja vissza.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
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
- TXT

Ha nem adja meg a *RecordType* paramétert, akkor a *Name* paramétert is el kell hagynia. Ezzel a parancsmaggal a zóna minden rekordját visszaadja (minden név és típus).

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

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
Type: String
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
A beolvasott rekordot tartalmazó DNS-zóna nevét adja meg.
A zónát tartalmazó erőforráscsoportot is meg kell adni a *ResourceGroupName* paraméter használatával.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. DNS. DnsZone
Ezt a parancsmagot a **dnsZone** -objektum pipe-ra kapcsolhatja.
A **dnsZone** objektum azt a zónát képviseli, amelyben a **Recordset** objektum keresve van.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet
Ez a parancsmag egy vagy több olyan objektumot ad eredményül, amely a talált rekordok halmazát képviseli.
A *név* és a *RecordType* paraméter megadása esetén a program legfeljebb egy **rekordhalmazt** ad vissza, máskülönben több **rekordhalmazt** ad vissza tömbként.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


