---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015929"
---
# New-AzureDeployment

## Áttekintés
Egy szolgáltatásból hozza létre a telepítőt.

## SZINTAXISA

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureDeployment** parancsmag egy olyan szolgáltatásból hoz létre Azure-telepítőt, amely a webes szerepköröket és a munkatársi szerepköröket tartalmazza.
Ez a parancsmag egy csomagfájl (. cspkg) és egy szolgáltatás-konfigurációs fájl (. cscfg) alapján hoz létre központi üzembe helyezést.
Adjon meg egy olyan nevet, amely egyedi a központi telepítő környezeten belül.

A **New-AzureVM** parancsmaggal az Azure virtuális gépeken alapuló központi telepítőt hozhat létre.

## Példák

### Példa 1: központi telepítő létrehozása
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

A parancs a ContosoPackage. cspkg nevű csomagon alapuló, a ContosoConfiguration. cscfg nevű konfigurációt hoz létre.
A parancs a központi telepítő címkéjét adja meg.
Nem adja meg a nevet.
Ez a parancsmag létrehoz egy GUID-azonosítót névként.

### 2. példa: a központi telepítő létrehozása bővítmény-konfiguráció alapján
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

Ezzel a paranccsal létrehozhatja a termelést a csomag és a konfiguráció alapján.
A parancs a ContosoExtensionConfig. cscfg nevű bővítmény-konfigurációt adja meg.
Ez a parancsmag a nevet és a címkét AZONOSÍTÓkat hoz létre.

## PARAMÉTEREK

### -Configuration
A szolgáltatás konfigurációs fájljának teljes elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DoNotStart
Azt adja meg, hogy ez a parancsmag nem indítja el a telepített példányt.

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

### -ExtensionConfiguration
A bővítmények konfigurációs objektumainak tömbjét adja meg.

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
A bevezetéshez a címke nevét adja meg.
Ha nem ad meg címkét, ez a parancsmag GUID-ot használ.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A telepítő nevét adja meg.
Ha nem ad meg nevet, ez a parancsmag GUID-ot használ.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package (csomag)
Egy. cspkg fájl elérési útját vagy URI-azonosítóját adja meg ugyanazon az előfizetésen vagy projekten belül.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -Szolgáltatásnév
A központi üzembe helyezés Azure-szolgáltatásának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Azt a környezetet adja meg, ahol ez a parancsmag hozza létre a központi telepítőt.
Érvényes értékek: staging és termelés.
Az alapértelmezett érték a termelés.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TreatWarningsAsError
Itt adhatja meg, hogy a figyelmeztető üzenetek hibásak-e.
Ha ezt a paramétert adja meg, figyelmeztető üzenet jelzi, hogy a telepítő sikertelen lesz.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Move-AzureDeployment](./Move-AzureDeployment.md)

[Új – AzureVM](./New-AzureVM.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


