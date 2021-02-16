---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147979"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
Rekordkészlet törlése.

## SZINTAXIS

### Mezők
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Vegyes
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzDnsRecordSet** parancsmag törli a megadott rekordkészletet a megadott zónából.
A zóna csúcsán automatikusan létrehozott SOA- vagy névkiszolgáló-rekordok nem törölhetők.
A **RecordSet-objektumot** ehhez a parancsmaghoz a folyamat műveleti jelét használva vagy paraméterként is át lehet adni.
Ha a **RecordSet-objektum** használata nélkül, név szerint és típus szerint meg tud adni egy rekordot, a zónát **DnsZone-objektumként** kell átadnia ennek a parancsmagnak a folyamat műveleti jelének vagy paraméterének használatával, vagy megadhatja a *ZoneName* és *az ResourceGroupName* paramétert is.
A Confirm paraméter és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.
Amikor rekordkészletet ad meg **Egy RecordSet-objektummal,** a rekordkészlet nem törlődik, ha módosult az Azure DNS-ben a helyi **RecordSet objektum lekérése** óta.
Ez védelmet nyújt az egyidejű módosítások számára.
Ezt letilthatja a  Felülírás paraméter használatával, amely törli a rekordkészletet az egyidejű módosításoktól függetlenül.

## PÉLDÁK

### 1. példa: Rekordkészlet eltávolítása
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Az első parancs megkapja a megadott rekordkészletet, majd a $RecordSet tárolja. A második parancs eltávolítja a rekordkészletet a $RecordSet.

### 2. példa: Rekordkészlet eltávolítása és az összes megerősítés mellőzése
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Az első parancs megkapja a megadott rekordkészletet.
A második parancs törli a rekordkészletet, még akkor is, ha időközben megváltozott.
A megerősítést kérő kérések nincsenek letiltva.

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
Az eltávolítható **RecordSet neve.**
A név szerint beállított rekord megadásakor a DNS-zónát vagy a Zone *paraméter,* illetve *a ZoneName* és *az ResourceGroupName* paraméter használatával kell megadni.
Másik lehetőségként a rekordkészletet a **RecordSet** objektummal is meg lehet adni, és *a RecordSet paraméterrel kell* átadottnak lennie.

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Felülírás
Amikor rekordkészletet ad meg **Egy RecordSet-objektummal,** a rekordkészlet nem törlődik, ha módosult az Azure DNS-ben a helyi **RecordSet objektum lekérése** óta.
Ez védelmet nyújt az egyidejű módosítások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely törli a rekordkészletet, függetlenül az egyidejű módosításoktól.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

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

### -RecordSet
Az **eltávolítható RecordSet-objektumot** adja meg.
Másik lehetőségként a rekordkészletet  meg lehet adni a Name és *a Zone* paraméter, illetve a *Name,* *a ZoneName* és az *ResourceGroupName* paraméter használatával.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
A DNS-rekord típusát határozza meg.
Érvényes értékek:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- A TXT SOA rekordok a zóna törlésekor automatikusan törlődnek.
A SOA rekordok manuálisan nem törölhetők.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azt az erőforráscsoportot adja meg, amely a törlendni **kívánt RecordSet rekordkészletet** tartalmazó DNS-zónát tartalmazza.
Ez a paraméter csak akkor érvényes, ha a rekordkészlet és a DNS-zóna a *Name* and *ZoneName* paraméterrel van megadva.
Másik lehetőségként megadhatja a rekordkészletet a *RecordSet* vagy a *Name* and *Zone paraméterrel.*

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
Azt a DNS-zónát adja meg, amely a **törlendni kívánt RecordSet** rekordkészletet tartalmazza.
Ez a paraméter csak akkor alkalmazható, ha a Rekordkészletet a *Name paraméterrel adja* meg.
Másik lehetőségként megadhatja a rekordkészletet a *RecordSet* vagy a *Name,* *ZoneName* és *ResourceGroupName* paraméterrel.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Annak a zónának a nevét adja meg, amely a **törlendni kívánt Rekordkészletet** tartalmazza.
A Name és  *az ResourceGroupName* paramétert is meg kell adnia.
Másik lehetőségként a rekordkészletet a *RecordSet* paraméterrel, illetve a *Name* and *Zone paraméterrel is meg lehet* adni.

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

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK
A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.
A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.
Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatása előtt.
Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
