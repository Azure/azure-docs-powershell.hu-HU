---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025352"
---
# Get-AzDnsZone

## Áttekintés
DNS-zónát kap.

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzDnsZone** parancsmag a megadott erőforráscsoport tartománynévrendszer (DNS) zónájába kerül.
Ha a *Name* paramétert adja meg, a program egyetlen **dnsZone** objektumot ad vissza.
Ha nem adja meg a *Name* paramétert, a függvény a megadott erőforráscsoport összes zónáját tartalmazó tömböt ad vissza.
A **dnsZone** objektum segítségével frissítheti a zónát, például megadhatja a **rekordhalmaz** objektumait.

## Példák

### Példa 1: zóna beszerzése
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Ebben a példában a myzone.com nevű DNS-zónát kapja meg a megadott erőforráscsoport, majd a $Zone változóban tárolja.

### 2. példa: egy erőforráscsoport összes zónájának beolvasása
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Ez a példa a megadott erőforráscsoport összes DNS-zónáját beilleszti, majd a $Zones változóban tárolja.

### 3. példa: az előfizetésben szereplő összes zóna lekérése
```
PS C:\> $Zones = Get-AzDnsZone
```

Ez a példa beilleszti az összes DNS-zónát az aktuális Azure-előfizetésbe, majd a $Zones változóban tárolja őket.

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
A beszerzéshez használandó DNS-zóna nevét adja meg.
Ha nem ad meg értéket a *Name* paraméterhez, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját megkapja.
Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetésből az összes DNS-zónát megkapja.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A beszerzéshez használt DNS-zónát tartalmazó erőforráscsoport nevét adja meg.
Ha nem adja meg a *ResourceGroupName* , akkor a *Name* paramétert is el kell hagynia.
Ebben az esetben ez a parancsmag a jelenlegi Azure-előfizetésben lévő összes DNS-zónát megkapja.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
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

### System. String

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsZone

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
