---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015883"
---
# Publish-AzureServiceProject

## Áttekintés
Az aktuális szolgáltatás közzététele a Windows Azure-ban

## SZINTAXISA

### PublishFromServiceDefinition (alapértelmezett)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Közzététel – AzureServiceProject** parancsmag közzéteszi az aktuális szolgáltatást a felhőben.
Megadhatja a közzétételi konfigurációt (például az **előfizetést** , a **StorageAccountName** , a **helyet** , a **bővítőhelyet** ) a parancssorban vagy a **set-AzureServiceProject** parancsmagon keresztül.

## Példák

### Példa 1: szolgáltatási projekt közzététele alapértelmezett értékekkel
```
PS C:\> Publish-AzureServiceProject
```

Ez a példa közzéteszi az aktuális szolgáltatást a jelenlegi szolgáltatás beállításaival és az Azure aktuális közzétételi profiljának használatával.

### 2. példa: központi telepítőcsomag létrehozása
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

Ez a példa létrehoz egy telepítőcsomag (. cspkg) fájlt a címtárszolgáltatásban, és nem teszi közzé a Windows Azure-ban.

## PARAMÉTEREK

### -AffinityGroup
Azt a affinitási csoportot adja meg, amelyet használni szeretne a szolgáltatásban.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configuration
A szolgáltatás konfigurációs fájlját adja meg.
Ha ezt a paramétert adja meg, adja meg a *csomag* paramétert.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
A központi telepítő nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Launch (indítás)
Megnyit egy böngészőablakot, amelyen megtekintheti az alkalmazást a telepítés után.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Az a terület, ahol az alkalmazást üzemeltetni fogja.
A lehetséges értékek a következők: 
  
- Bárhonnan Ázsia
- Bárhol Európában
- Bárhol vagyunk
- Kelet-ázsiai
- Kelet-amerikai
- Közép-amerikai Észak-amerikai
- Észak-Európa
- Dél-Közép-amerikai
- Dél-ázsiai
- Nyugat-Európa
- Nyugat-amerikai
 
Ha nincs megadva hely, a program az utolsó híváshoz megadott helyet fogja használni a **AzureServiceProject** . Ha még nincs megadva tartózkodási hely, a hely véletlenszerűen lesz kiválasztva az "Észak-Közép-amerikai" és "Dél-Közép-amerikai" helyről.

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Package (csomag)
A telepítendő csomagfájl meghatározása.
Adjon meg egy olyan helyi fájlt, amely. cspkg fájlnévkiterjesztéssel vagy a csomagot tartalmazó blob-AZONOSÍTÓval rendelkezik.
Ha ezt a paramétert adja meg, ne adja meg a *szolgáltatásnév* paramétert.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Itt adhatja meg a Windows Azure-ra való közzétételkor a szolgáltatáshoz használni kívánt nevet.
A név határozza meg a címke azon részét a cloudapp.net altartományban, amellyel a szolgáltatás a Windows Azure-ban (azaz **név**. cloudapp.net) van tárolva.
A szolgáltatás közzétételekor megadott nevek felülírják a szolgáltatás létrehozásakor megadott nevet.
(Lásd a **New-AzureServiceProject** parancsmagot).

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A szolgáltatáshoz használni kívánt telepítő-bővítőhely.
A lehetséges értékek "staging" és "termelés".
Ha nem ad meg bővítőhelyet, a rendszer az utolsó hívás Set-AzureDeploymentSlot-ban megadott bővítőhelyet használja.
Ha még nincs megadva bővítőhely, a program a "termelés" bővítőhelyet használja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Annak a Windows Azure Storage-fióknak a nevét adja meg, amelyet a szolgáltatás közzétételekor kell használni.
Ezt az értéket csak a szolgáltatás közzétételéhez használja a program.
Ha ez a paraméter nincs megadva, a program az utolsó **set-AzureServiceProject** parancs értékét adja eredményül.
Ha egyetlen tárterület sem volt megadva, a rendszer a szolgáltatás nevét tartalmazó tárterület-fiókot fogja használni.
Ha nincs ilyen tárolási fiók, a parancsmag megkísérel létrehozni egy újat.
Ha azonban egy másik előfizetésben megtalálható a szolgáltatás nevéhez tartozó tárolási fiók, a kísérlet sikertelen lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


