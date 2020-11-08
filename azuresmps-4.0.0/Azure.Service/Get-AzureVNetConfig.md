---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016288"
---
# Get-AzureVNetConfig

## Áttekintés
A jelenlegi előfizetésből kapja meg az Azure virtuális hálózat konfigurációját.

## SZINTAXISA

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureVNetConfig** parancsmag lekéri az aktuális Azure-előfizetés virtuális hálózati konfigurációját.
Ha a *ExportToFile* paramétert adja meg, létrejön egy hálózati konfigurációs fájl.

## Példák

### Példa 1: a jelenlegi Azure-előfizetés virtuális hálózati konfigurációjának beszerzése
```
PS C:\> Get-AzureVNetConfig
```

Ez a parancs az aktuális Azure-előfizetés virtuális hálózati konfigurációját kapja, és megjeleníti.

### 2. példa: az aktuális Azure-előfizetés virtuális hálózati konfigurációjának beszerzése és helyi fájlba mentése
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

Ez a parancs beolvassa az aktuális Azure-előfizetés virtuális hálózati konfigurációját, majd egy helyi fájlba menti.

## PARAMÉTEREK

### -ExportToFile
A beállításokból létrehozandó hálózati konfigurációs fájl elérési útját és fájlnevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-AzureVNetSite](./Get-AzureVNetSite.md)

[Remove-AzureVNetConfig](./Remove-AzureVNetConfig.md)

[Set-AzureVNetConfig](./Set-AzureVNetConfig.md)


