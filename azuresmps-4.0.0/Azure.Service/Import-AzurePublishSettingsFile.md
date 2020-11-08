---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016261"
---
# Import-AzurePublishSettingsFile

## Áttekintés
Importálja a közzétételi beállításokat tartalmazó fájlt, amely lehetővé teszi az Azure-fiókok kezelését a Windows PowerShellben.

## SZINTAXISA

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **import-AzurePublishSettingsFile** parancsmag olyan közzétételi beállításokat tartalmazó fájlt (*. publishsettings) importál, amely információkat tartalmaz az Azure-fiókokról, és az előfizetési adatfájlt menti a számítógépre.
A parancsmag befejezésekor az Azure-fiókok kezelése a Windows PowerShellben végezhető el.

Mielőtt futtatná az **importálási AzurePublishSettingsFile** , futtassa a **Get-AzurePublishSettingsFile** , amely letölti és menti a közzétételi beállításokat tartalmazó fájlt, így importálhatja.

Ha az Azure-fiókját elérhetővé szeretné tenni a Windows PowerShellben, használhatja a közzétételi beállításokat tartalmazó fájlt vagy az **Add-AzureAccount** parancsmagot.
A beállítási fájlok közzététele lehetővé teszi, hogy a munkamenetet előre felkészítse, így a parancsfájlok és a háttérben végzett feladatok felügyelet nélkül is használhatók.
Nem minden szolgáltatás támogatja a közzétételi beállítások fájljait.
A **AzureResourceManager** modul például nem támogatja a közzétételi beállítások fájljait.

**Biztonsági Megjegyzés:** A közzétételi beállítások fájljai olyan felügyeleti tanúsítványokat tartalmaznak, amelyek kódoltak, de nem titkosítottak.
Ha a rosszindulatú felhasználók hozzáférhetnek a közzétételi beállítási fájlhoz, az Azure-szolgáltatások szerkeszthetők, hozhatók létre és törölhetők.
Biztonsági szempontból célszerű lehet menteni a fájlt a letöltések vagy a dokumentumok mappa egy helyére, majd az **import-AzurePublishSettingsFile** parancsmag használatával importálja a beállításokat.

## Példák

### 1. példa: fájl importálása
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

A parancs a "C:\Temp\MyAccount.publishsettings" fájlt importálja.

## PARAMÉTEREK

### -Környezet
Azure-környezetet ad meg.

Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.
A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.
További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -PublishSettingsFile
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Nincs
Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI
* A "közzétételi beállítások fájl" egy. publishsettings fájlnév-kiterjesztésű XML-fájl. A fájl olyan kódolt tanúsítványt tartalmaz, amely felügyeleti hitelesítő adatokat biztosít az Azure-előfizetésekhez. A fájl importálása után törölje azt a biztonsági kockázatok elkerülése érdekében.
* Az "előfizetés-adatfájl" olyan XML-fájl, amelyet a számítógépére biztonságosan lehet menteni. Alapértelmezés szerint a rendszer a központi felhasználói profilba menti a fájlt ($home/AppData/Roaming).

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Az Azure PowerShell telepítése és beállítása](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


