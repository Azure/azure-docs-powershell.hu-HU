---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016259"
---
# Import-AzureStorSimpleLegacyApplianceConfig

## Áttekintés
Importál egy konfigurációs fájlt.

## SZINTAXISA

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **import-AzureStorSimpleLegacyApplianceConfig** parancsmag importálja a konfigurációs fájlt a régi készülékről.
A fájl a mennyiségi tárolókkal, a biztonsági irányelvekkel és az Azure StorSimple szolgáltatáshoz tartozó tárolási fiók hitelesítő adataival kapcsolatos információkat tartalmazza.
Ez a parancsmag a régi készülék konfigurációs metaadatait számítja ki.

## Példák

### 1. példa: konfigurációs fájl importálása
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

Ezzel a paranccsal importálhatja a konfigurációs fájlt a megadott elérési úttal.
A parancs a fájl visszafejtéséhez a kulcsot tartalmazza.

## PARAMÉTEREK

### -ConfigDecryptionKey
A régi készülék konfigurációjának visszafejtési kulcsát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigFilePath
A beolvasott konfigurációs fájl abszolút elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Egy Azure-profilt ad meg.

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

### -TargetDeviceName
A megcélzott eszköz nevét adja meg a portálon bemutatott módon.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### LegacyApplianceConfiguration
Ez a parancsmag a konfiguráció részleteit számítja ki.
A **LegacyApplianceConfiguration** objektum a következő információkat tartalmazza: konfigurációs azonosító, mennyiségi tárolók, hozzáférés-szabályozási rekordok, biztonsági házirendek, sávszélesség-beállítások, mennyiségi tárolók, a tárolási fiók hitelesítő adatai és a kötetek.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Importálás – AzureStorSimpleLegacyVolumeContainer](./Import-AzureStorSimpleLegacyVolumeContainer.md)


