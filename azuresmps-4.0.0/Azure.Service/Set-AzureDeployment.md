---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016064"
---
# Set-AzureDeployment

## Áttekintés
Módosítja a bevezetések állapotát, konfigurációs beállításait vagy frissítési módját.

## SZINTAXISA

### Frissítés
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Config
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Állapot
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureDeployment** parancsmag az Azure-példányok állapotát, konfigurációs beállításait vagy frissítési módját módosítja.
A telepített példány állapotát a futás vagy a felfüggesztett állapotra is módosíthatja.
Az. cscfg fájlt módosíthatja a központi telepítőben.
Beállíthatja a frissítési módot, és frissítheti a konfigurációs fájlokat.
A **set-AzureWalkUpgradeDomain** parancsmaggal frissítést kezdeményezhet.

## Példák

### Példa 1: a bevezetési állapot módosítása
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

Ez a parancs a ContosoService nevű szolgáltatás üzembe helyezésének állapotát a termelés környezetében állítja be.

### 2. példa: másik konfigurációs fájl hozzárendelése egy központi példányhoz
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

Ez a parancs egy másik konfigurációs fájlt rendel a ContosoService nevű szolgáltatás üzembe helyezéséhez a megállóhelyek környezetében.

### 3. példa: a frissítési mód beállítása automatikusra
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

Ezzel a paranccsal automatikusan beállíthatja a frissítési módot, és megad egy frissítési csomagot és egy új konfigurációs fájlt.

### 4. példa: a bővítmények konfigurációjának telepítése egy szolgáltatásban
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

Ez a parancs a megadott Felhőbeli szolgáltatásban telepíti a bővítmények konfigurációját, és alkalmazza őket a szerepkörökre.

## PARAMÉTEREK

### -Config
Azt adja meg, hogy a parancsmag módosítja-e a telepített példány konfigurációját.

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Configuration
A. cscfg konfigurációs fájlok teljes elérési útját adja meg.
Megadhat egy konfigurációs fájlt a frissítéshez vagy a konfiguráció módosításához.

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionConfiguration
A bővítmények konfigurációs objektumainak tömbjét adja meg.

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Azt jelzi, hogy a parancsmag kényszerített frissítést hajt végre.

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
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

### -Label (címke)
A frissített példány feliratát adja meg.

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Üzemmód
A frissítés üzemmódját adja meg.
Az érvényes értékek a következők: 

- Automatikus 
- Kézi 
- Egyidejű

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewStatus
A bevezetéshez tartozó cél állapotát adja meg.
Az érvényes értékek a következők: futás és felfüggesztve.

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package (csomag)
A frissítési csomagfájl teljes elérési útját adja meg.

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
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
A frissítendő szerepkör nevét adja meg.

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szolgáltatásnév
A központi üzembe helyezés Azure-szolgáltatásának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A módosítani kívánt központi verzió környezetét adja meg.
Érvényes értékek: a termelés és a megállóhelyek.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
Azt adja meg, hogy a parancsmag a telepített példány állapotát módosítja.

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Upgrade
Azt adja meg, hogy az adott parancsmag frissíti a telepítőt.

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
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

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Move-AzureDeployment](./Move-AzureDeployment.md)

[Új – AzureDeployment](./New-AzureDeployment.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureWalkUpgradeDomain](./Set-AzureWalkUpgradeDomain.md)


