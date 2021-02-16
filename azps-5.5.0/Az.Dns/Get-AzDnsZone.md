---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204158"
---
# Get-AzDnsZone

## SYNOPSIS
DNS-zónát kap.

## SZINTAXIS

### Alapértelmezett (alapértelmezett)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzDnsZone** parancsmag egy DNS-zónát kap a megadott erőforráscsoportból.
Ha megadja a *Name paramétert,* egyetlen **DnsZone-objektumot** ad vissza.
Ha nem adja meg a *Name* paramétert, a visszaadott érték egy tömb, amely a megadott erőforráscsoport összes zónáját tartalmazza.
A **DnsZone objektummal** frissítheti a zónát, például **RecordSet-objektumokat** adhat hozzá.

## PÉLDÁK

### 1. példa: Zóna lekérte
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Ebben a példában a megadott erőforráscsoportból myzone.com a DNS-zóna nevét, majd a $Zone tárolja.

### 2. példa: Erőforráscsoport összes zónája
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Ez a példa a megadott erőforráscsoport összes DNS-zónáját beveszi, majd a $Zones tárolja.

### 3. példa: Az előfizetés összes zónája
```
PS C:\> $Zones = Get-AzDnsZone
```

Ez a példa beveszi az aktuális Azure-előfizetés összes DNS-zónáját, majd tárolja őket a $Zones változóban.

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
A lekért DNS-zóna neve.
Ha nem ad meg értéket a *Name* paraméternek, ez a parancsmag a megadott erőforráscsoport összes DNS-zónáját beveszi.
Ha a *ResourceGroupName* paramétert is kihagyja, ez a parancsmag az aktuális Azure-előfizetés összes DNS-zónáját megkapja.

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
Annak az erőforráscsoportnak a neve, amely a behozni kívánt DNS-zónát tartalmazza.
Ha nem adja meg az *ResourceGroupName* paramétert, akkor a *Name* paramétert is ki kell kihagyni.
Ebben az esetben ez a parancsmag az aktuális Azure-előfizetés összes DNS-zónáját beveszi.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Dns.DnsZone

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
