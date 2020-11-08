---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194580"
---
# New-AzMigrateNicMapping

## Áttekintés
Olyan objektumot hoz létre, amellyel frissíthető a hálózati adapterek tulajdonságai a replikált kiszolgálóról.

## SZINTAXISA

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## Leírás
A New-AzMigrateNicMapping parancsmag létrehoz egy leképezést az áttelepíteni kívánt kiszolgálóhoz tartozó forrás NIC-hez.
Ez az objektum bemenetként van megadva a Set-AzMigrateServerReplication parancsmagban a hálózati adapter és a replikált kiszolgálók tulajdonságainak frissítéséhez.

## Példák

### 1. példa: NIC-objektum létrehozása
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

NIC Update objektum létrehozása

## PARAMÉTEREK

### -NicI
A frissítendő NIC AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicIP
A hálózati adapterhez használni kívánt IP-címet adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSelectionType
Azt adja meg, hogy a frissíteni kívánt hálózati adapter az elsődleges, a másodlagos vagy a nincs áttelepítve érték lesz-e.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSubnet
Annak a virtuális hálózati adapternek a hálózati adapterének a neve, amelyhez a kiszolgálót át kell telepíteni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IVMwareCbtNicInput

## MEGJEGYZI

ALIASOK

## KAPCSOLÓDÓ HIVATKOZÁSOK

