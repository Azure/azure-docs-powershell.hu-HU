---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935017"
---
# Remove-AzDnsZone

## SYNOPSIS
Eltávolít egy DNS-zónát egy erőforráscsoportból.

## SZINTAXIS

### Mezők
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Remove-AzDnsZone** parancsmag véglegesen töröl egy DNS-zónát egy adott erőforráscsoportból.
A zónában található összes rekordkészlet is törlődik.
A **DnsZone-objektumokat** átadhatja a Name paraméterrel vagy a folyamat műveleti jelével, vagy másik lehetőségként megadhatja a *ZoneName* és *az ResourceGroupName* paramétert. 
A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.
Amikor **dnsZone-objektummal** adja meg a zónát  (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **DnsZone-objektum** beolvasása óta (csak a DNS-zóna erőforrásának módosításain végrehajtott műveletek számítanak változásnak, a zónán belüli rekordkészletek műveletei azonban nem).
Ez védelmet nyújt a párhuzamos zónaváltozások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.

## PÉLDÁK

### 1. példa: Zóna eltávolítása
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Ez a parancs eltávolítja a myzone.com myResourceGroup nevű erőforráscsoportból.

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
A parancsmag által eltávolított DNS-zóna neve.
Az *ResourceGroupName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a DNS-zónát a *Zone paraméter* használatával.

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

### -Felülírás
Amikor **dnsZone-objektummal** adja meg a zónát  (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem törlődik, ha az Azure DNS-ben módosult a helyi **DnsZone-objektum** beolvasása óta (csak a DNS-zóna erőforrásának módosításain végrehajtott műveletek számítanak változásnak, a zónán belüli rekordkészletek műveletei azonban nem).
Ez védelmet nyújt a párhuzamos zónaváltozások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely törli a zónát, függetlenül az egyidejű módosításoktól.

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

### -ResourceGroupName
Az eltávolítható zónát tartalmazó erőforráscsoport neve.
A *ZoneName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a DNS-zónát egy **DnsZone-objektum** használatával, amely vagy a folyamaton, vagy a Zone paraméteren *keresztül adható* meg.

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
A törlendni kívánt DNS-zóna.
A **átadott DnsZone-objektum** a folyamaton keresztül is áthaladhat.
Másik lehetőségként megadhatja a törölni kívánt DNS-zónát a *ZoneName* és *az ResourceGroupName* paraméter használatával.

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

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK
A DNS-zóna törlésének potenciálisan nagy hatása miatt ez a parancsmag alapértelmezés szerint megerősítést kér, ha a $ConfirmPreference Windows PowerShell-változó értéke a Nincs értéktől különböző.
Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatás előtt.
Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést. 

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
