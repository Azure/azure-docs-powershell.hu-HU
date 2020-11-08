---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015787"
---
# Set-AzureVNetConfig

## Áttekintés
Az Azure Cloud-szolgáltatás virtuális hálózati beállításainak frissítése.

## SZINTAXISA

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureVNetConfig** parancsmag frissíti az aktuális Azure-előfizetés hálózati konfigurációját a hálózati konfigurációs fájl (. netcfg) elérési útjának megadásával.
A hálózati konfigurációs fájl a felhőalapú szolgáltatásokhoz tartozó DNS-kiszolgálókat és alhálózatokat definiálja az előfizetésben.

## Példák

### Példa 1: az Azure-előfizetés hálózati konfigurációjának frissítése helyi fájlra
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

Ez a parancs frissíti az aktuális Microsoft Azure-előfizetés hálózati konfigurációját a "c:\temp\MyAzNets.netcfg" helyi fájlban.

### 2. példa: az Azure-előfizetés beállítása, majd a hálózati konfiguráció frissítése
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

Ez a példa beállítja a Microsoft Azure-előfizetést, majd frissíti az előfizetés hálózati konfigurációját a "c:\temp\MyAzNets.netcfg" helyi fájlban definiált konfiguráció használatával.

## PARAMÉTEREK

### -ConfigurationPath
A hálózati konfigurációs fájlok (. netcfg) elérési útját és fájlnevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureVNetConfig](./Get-AzureVNetConfig.md)

[Get-AzureVNetSite](./Get-AzureVNetSite.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)


