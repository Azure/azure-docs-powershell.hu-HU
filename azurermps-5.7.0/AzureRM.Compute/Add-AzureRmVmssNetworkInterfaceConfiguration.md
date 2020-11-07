---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672037"
---
# Add-AzureRmVmssNetworkInterfaceConfiguration

## Áttekintés
Hálózati illesztőfelület-konfiguráció felvétele a VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmag hálózati illesztőfelület-konfigurációt ad hozzá a Virtual Machine Scale set (VMSS) beállításhoz.

## Példák

### Példa 1: hálózati illesztőfelület-konfiguráció felvétele a VMSS
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

Ez a parancs hálózati illesztőfelület-konfigurációt ad a VMSS.

## PARAMÉTEREK

### -DnsSettingsDnsServer
A DNS-kiszolgálók IP-címeinek listája a DNS-beállításokhoz.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Azonosító
A virtuális gép erőforrás-AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpConfiguration
A hálózati felület IP-konfigurációit adja meg.

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A hálózati felület konfigurációjának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkSecurityGroupId
A hálózati biztonsági csoport azonosítója

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

### -Elsődleges
Azt jelzi, hogy a hálózati illesztőfelület-konfigurációból létrehozott hálózati felületek a virtuális gép elsődleges hálózati információs központja (NIC) fogják-e létrehozni.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
A VMSS objektumot adja meg.
Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

###  
Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
