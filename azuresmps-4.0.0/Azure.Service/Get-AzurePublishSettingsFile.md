---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015633"
---
# Get-AzurePublishSettingsFile

## Áttekintés
Az Azure-előfizetés közzétételi beállítások fájljának letöltése.

## SZINTAXISA

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzurePublishSettingsFile** parancsmag letölti az előfizetéshez tartozó közzétételi beállítások fájlt a fiókjába.
Ha befejeződött a parancs, az **import-PublishSettingsFile** parancsmaggal megadhatja, hogy a fájl beállításai elérhetők legyenek a Windows PowerShellben.

Ha az Azure-fiókját elérhetővé szeretné tenni a Windows PowerShellben, használhatja a közzétételi beállításokat tartalmazó fájlt vagy az **Add-AzureAccount** parancsmagot.
A beállítási fájlok közzététele lehetővé teszi, hogy a munkamenetet előre felkészítse, így a parancsfájlok és a háttérben végzett feladatok felügyelet nélkül is használhatók.
Nem minden szolgáltatás támogatja a közzétételi beállítások fájljait.
A **AzureResourceManager** modul például nem támogatja a közzétételi beállítások fájljait.

A **Get-AzurePublishSettingsFile** futtatásakor megnyílik az alapértelmezett böngésző, és kéri, hogy lépjen be az Azure-fiókjába, jelölje ki az előfizetést, és válassza ki a fájl rendszerhelyét a közzétételi beállítások fájlhoz.
Ezután letölti az előfizetéshez tartozó közzétételi beállítások fájlt a kijelölt fájlba.

A "közzétételi beállítások fájl" egy. publishsettings fájlnév-kiterjesztésű XML-fájl.
A fájl olyan kódolt tanúsítványt tartalmaz, amely felügyeleti hitelesítő adatokat biztosít az Azure-előfizetésekhez.

**Biztonsági Megjegyzés:** A közzétételi beállítások fájljai az Azure-előfizetések és-szolgáltatások felügyeletéhez használt hitelesítő adatokat tartalmazzák.
Ha a rosszindulatú felhasználók hozzáférhetnek a közzétételi beállítási fájlhoz, szerkeszthetik, hozhatják létre és törölhetik az Azure-szolgáltatásokat.
Biztonsági szempontból célszerű lehet menteni a fájlt a letöltések vagy a dokumentumok mappa egy helyére, majd az **import-AzurePublishSettingsFile** parancsmag használatával importálja a beállításokat.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: a közzétételi beállítások fájl letöltése
```
PS C:\> Get-AzurePublishSettingsFile
```

Ez a parancs megnyitja az alapértelmezett böngészőt, csatlakozik a Windows Azure-fiókjához, majd letölti a fiókjához tartozó. publishsettings fájlt.

### 2. példa: a tartomány megadása
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Ez a parancs letölti a contoso.com tartományban lévő fiókhoz tartozó közzétételi beállítások fájlt.
Ha az Azure-ba egy Microsoft-fiók helyett szervezeti fiókkal jelentkezik be, használja a **tartomány** paramétert tartalmazó parancsot.

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.
Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Realm
A szervezeti AZONOSÍTÓban lévő szervezetet adja meg.
Ha például az Azure as-be jelentkezik be admin@contoso.com , a **tartomány** paraméter értéke contoso.com.
Akkor használja ezt a paramétert, ha szervezeti AZONOSÍTÓval jelentkezik be az Azure-portálra.
Ez a paraméter a Microsoft-fiók (például outlook.com-vagy live.com-fiók) használata esetén nem szükséges.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Nincs vagy System. Boolean
A *PassThru* paraméter használatakor ez a parancsmag logikai értéket ad eredményül.
Ellenkező esetben ez a parancsmag nem adja vissza a kimenetet

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureAccount](./Add-AzureAccount.md)

[Importálás – AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


