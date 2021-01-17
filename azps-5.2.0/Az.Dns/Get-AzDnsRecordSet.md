---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346901"
---
# Get-AzDnsRecordSet

## SYNOPSIS
DNS-rekordkészletet kap.

## SZINTAXIS

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

## LEÍRÁS
A **Get-AzDnsRecordSet** parancsmag a megadott névvel és típussal megadott DNS-rekordot kapja a megadott zónában.
Ha nem adja meg a *Name* vagy *a RecordType* paramétert, ez a parancsmag a zónában megadott típusú összes rekordkészletet visszaadja.
Ha a *RecordType* paramétert adja meg, de a *Name* paramétert nem, ez a parancsmag a megadott rekordtípus összes rekordkészletét visszaadja.
A folyamat operátorával **dnsZone-objektumot** is átadhat ennek a parancsmagnak, vagy  átadhatja a **DnsZone-objektumokat** zóna paraméterként, vagy másik lehetőségként név szerint is megadhatja a zónát és az erőforráscsoportot.

## PÉLDÁK

### 1. példa: Meghatározott nevű és típusú rekordkészletek lekérte
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Ez a parancs a megadott erőforráscsoportban és zónában a www nevű A rekordkészletet kapja meg, majd a rekordot a $RecordSet tárolja.
Mivel a *Name és* *a RecordType* paraméter meg van adva, csak egy **RecordSet-objektumot** ad vissza a visszaadott érték.

### 2. példa: Adott típusú rekordkészletek lekérte
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Ez a parancs a MyResourceGroup nevű erőforráscsoport myzone.com nevű zónában az A rekordkészletek összes rekordkészletét beállítja, majd az $RecordSets változóban tárolja őket.

### 3. példa: Az összes rekordkészlet lekérte egy zónába
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Ez a parancs a MyResourceGroup nevű erőforráscsoport zónájában található myzone.com tömböt, majd a $RecordSets tárolja.

### 4. példa: Az összes rekordkészlet begyűjtése egy zónába dnsZone-objektum használatával
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Ez a példa egyenértékű a fenti 3. példával.
A zóna ezúttal zónaobjektum használatával van megadva.

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

### -Name
A lekért **RecordSet** nevét adja meg.
Ha nem adja meg a *Name* paramétert, a visszaadott érték a megadott típusú összes rekordkészletet visszaadja.

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
A parancsmag által lekért DNS-rekord típusát határozza meg.
Érvényes értékek: 
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT Ha nem adja meg a *RecordType* paramétert, a Name paramétert is ki kell *kihagyni.* Ez a parancsmag a zóna összes rekordkészletét visszaadja (az összes névből és típusból).

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
A zónanevet a *ZoneName* paraméter használatával is meg kell adni.
Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy **DnsZone-objektumot** *ad* át.

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

### -Zone
Azt a DNS-zónát adja meg, amely a parancsmag által behozott rekordkészletet tartalmazza.
Másik lehetőségként a *ZoneName* és az *ResourceGroupName* paramétert használva is megadhatja a zónát.

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
Annak a DNS-zónának a neve, amely a behozni kívánt rekordot tartalmazza.
A zónát tartalmazó erőforráscsoportot is meg kell adni az *ResourceGroupName* paraméter használatával.
Másik lehetőségként megadhatja a zónát és az erőforráscsoportot úgy, hogy a Zone paramétert használva egy DNS Zone-objektumot *ad* át.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## KIMENETEK

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


