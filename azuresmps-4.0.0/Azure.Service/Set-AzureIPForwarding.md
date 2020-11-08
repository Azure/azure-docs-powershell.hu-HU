---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015956"
---
# Set-AzureIPForwarding

## Áttekintés
Engedélyezi vagy tiltja az IP-továbbítást.

## SZINTAXISA

### EnableIaaSIPForwardingParamSet
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### DisableIaaSIPForwardingParamSet
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnableSlotIPForwardingParamSet
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### DisableSlotIPForwardingParamSet
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureIPForwarding** parancsmag engedélyezi vagy letiltja az IP-továbbítást egy virtuális gépen, platformként a szolgáltatásban (Péter), illetve egy virtuális gép vagy Péter szerepkörhöz tartozó hálózati adaptert.

## Példák

### 1. példa: az IP-továbbítás engedélyezése virtuális gépen
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.
Az aktuális parancsmag engedélyezi a virtuális gép IP-továbbítását.

### 2. példa: a virtuális gép IP-továbbításának letiltása
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.
Az aktuális parancsmag letiltja a virtuális gép IP-továbbítását.

## PARAMÉTEREK

### -Letiltása
Jelzi, hogy ez a parancsmag letiltja az IP-továbbítást.

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Engedélyezés
Azt jelzi, hogy ez a parancsmag engedélyezi az IP-továbbítást.

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterfaceName
Annak a hálózati adapternek a nevét adja meg, amelyen a parancsmag az IP-továbbítást állítja be.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Annak a Péter-szerepnek a nevét adja meg, amelyen a parancsmag az IP-továbbítást állítja be.

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Egy felhőalapú szolgáltatás nevét adja meg.
A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A Péter-bővítőhelyet adja meg.
A Péter szerepkör, amelynek a parancsmagja a továbbítást állítja be, a paraméter által megadott bővítőhelyet adja meg.
Az érvényes értékek a következők:

- Production
- Átmeneti tárolásra szolgáló

Az alapértelmezett érték a termelés.

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Annak a virtuális gépnek az objektumát adja meg, amelyen a parancsmag az IP-továbbítást állítja be.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureIPForwarding](./Get-AzureIPForwarding.md)
