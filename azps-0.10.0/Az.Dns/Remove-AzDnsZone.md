---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: bc77e2c69f285f0acab0bed8e6a40592374ebd18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842386"
---
# Remove-AzDnsZone

## Áttekintés
Eltávolítja a DNS-zónát egy erőforráscsoporthoz.

## SZINTAXISA

### Mezők
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Objektum
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzDnsZone** parancsmag véglegesen törli a DNS-zónát egy adott erőforráscsoport-csoportból.
A zónában található összes rekord is törlődik.

A **dnsZone** -objektumokat átadhatja a *Name* paraméterrel vagy a pipeline operátor segítségével, illetve megadhatja a *ZoneName* és a *ResourceGroupName* paramétert is.

A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.

Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).
Ez védelmet nyújt a zónák egyidejű változásaihoz.
Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.

## Példák

### 1. példa: zóna eltávolítása
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Ez a parancs eltávolítja a myzone.com nevű zónát a MyResourceGroup nevű erőforráscsoport-csoportból.

## PARAMÉTEREK

### -Force
Ez a paraméter érvénytelenítve van ennél a parancsmagnál.
A program eltávolítja a jövőbeli kiadásokban.

Ha meg szeretné állapítani, hogy ez a parancsmag kéri-e a megerősítést, használja a *Confirm* paramétert.

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

### -Name (név)
A parancsmag által eltávolított DNS-zóna nevét adja meg.
Meg kell adnia a *ResourceGroupName* paramétert is.

Azt is megteheti, hogy a *zóna* paraméterrel megadhatja a DNS-zónát.

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

### -Átír
Ha a zónát egy **dnsZone** -objektummal (a csővezetéken vagy a *Zone* paraméteren keresztül) adja meg, akkor a zóna nem törlődik, ha az Azure DNS-ben módosította a helyi **dnsZone** objektum beolvasása után (csak a DNS-zóna erőforrása, a zóna rekordjait tartalmazó műveletek a zónán belül nem).
Ez védelmet nyújt a zónák egyidejű változásaihoz.

Ezt a *felülírási* paraméter használatával lehet letiltani, amely a megegyező változásoktól függetlenül törli a zónát.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az eltávolítandó zónát tartalmazó erőforráscsoport nevét adja meg.
Meg kell adnia a *ZoneName* paramétert is.

Azt is megteheti, hogy megadhatja a DNS-zónát egy **dnsZone** objektummal, amelyet a csővezetéken vagy a *Zone* paraméteren keresztül adott meg.

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
A törlendő DNS-zónát adja meg.
Az átadott **dnsZone** objektum a csővezetéken keresztül is áthaladhat.

Azt is megteheti, hogy megadhatja a törölni kívánt DNS-zónát a *ZoneName* és a *ResourceGroupName* paraméter segítségével.

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
Ezt a parancsmagot a **dnsZone** -objektum pipe-ra kapcsolhatja.

## KIMENETEK

### Nincs
Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI
A DNS-zóna törlésének potenciálisan nagy hatása miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést, ha a $ConfirmPreference Windows PowerShell-változó a nincs értéktől eltérő értékkel rendelkezik.

Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést. 

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsZone](./Get-AzDnsZone.md)

[Új – AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
