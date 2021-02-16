---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146243"
---
# Set-AzPrivateDnsZone

## SYNOPSIS
Frissíti a privát DNS-zónát egy erőforráscsoportból.

## SZINTAXIS

### Mezők (alapértelmezett)
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzPrivateDnsZone** parancsmag véglegesen frissíti a dns-zónát egy adott erőforráscsoportból.
A **PrivateDnsZone-objektumokat** a *PrivateZone* paraméterrel vagy a folyamat műveleti jelével, illetve a *Name* and *ResourceGroupName* paraméter megadásával is átadhatja.
A Confirm paraméter és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.
Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem frissül, ha módosult az Azure DNS-ben a helyi **PrivateDnsZone** objektum beolvasása óta (csak a DNS-zóna erőforrásszámán végrehajtott műveletek változásként, a rekordkészletek műveletei a zónán belül nem).
Ez védelmet nyújt a párhuzamos zónaváltozások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely a egyidejűleg végrehajtott módosításoktól függetlenül frissíti a zónát.

## PÉLDÁK

### 1. példa: Privát zóna frissítése
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

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
A parancsmag által frissülő privát DNS-zóna neve.
Az *ResourceGroupName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a privát DNS-zónát a *Zone paraméter* használatával.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Felülírás
Amikor a zónát **egy PrivateDnsZone-objektummal** adja  meg (amely a folyamaton vagy a Zóna paraméteren keresztül lett átadva), a zóna nem frissül, ha módosult az Azure DNS-ben a helyi **DnsZone-objektum** beolvasása óta (csak a DNS-zóna erőforrásának módosításain végrehajtott műveletek, a zónán belüli rekordkészletek műveletei nem).
Ez védelmet nyújt a párhuzamos zónaváltozások számára.
Ez elrejthető a  Felülírás paraméter használatával, amely a egyidejűleg végrehajtott módosításoktól függetlenül frissíti a zónát.

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

### -PrivateZone
A beállított zónaobjektum.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
A frissíteni kívánt zónát tartalmazó erőforráscsoport neve.
A *ZoneName* paramétert is meg kell adnia.
Másik lehetőségként megadhatja a privát DNS-zónát egy **DnsZone-objektum** használatával, amely vagy a folyamaton, vagy a Zone paraméteren *keresztül adható* meg.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Private DNS Zone ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
A hash table which represents resource tags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

## KIMENETEK

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
