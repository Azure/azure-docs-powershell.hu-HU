---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015950"
---
# Set-AzureSubscription

## Áttekintés
Azure-előfizetés módosítása

## SZINTAXISA

### UpdateSubscriptionByIdParameterSetName (alapértelmezett)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureSubscription** parancsmag az Azure-előfizetés objektum tulajdonságait hozza létre és módosítja.
Ezzel a parancsmaggal olyan Azure-előfizetésben dolgozhat, amely nem az alapértelmezett előfizetése, illetve módosíthatja az aktuális tárterület-fiókot.
Az aktuális és az alapértelmezett előfizetésekről a **Select-AzureSubscription** parancsmag című témakörben olvashat bővebben.

Ez a parancsmag Azure-előfizetéses objektumon működik, és nem a tényleges Azure-előfizetése.
Azure-előfizetés létrehozásához és létrehozásához keresse fel az [Azure portált](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .

Ez a parancsmag azokat az előfizetési adatfájlokat módosítja, amelyeket a **Add-AzureAccount** vagy az **import-AzurePublishSettingsFile** parancsmaggal létrehozott, ha Azure-fiókot szeretne felvenni a Windows powershellbe.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: meglévő subscription1 módosítása
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

Ez a példa a ContosoEngineering nevű előfizetés tanúsítványát módosítja.

### 2. példa: a szolgáltatás végpontjának módosítása
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

Ez a parancs hozzáadja vagy módosítja az ContosoEngineering-előfizetés egyéni szolgáltatási végpontját.

### 3. példa: tulajdonságérték törlése
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

A parancs a tanúsítvány és a ResourceManagerEndpoint tulajdonság értékét NULL értékűre ($Null) állítja be.
Ezzel a beállítással a többi beállítás módosítása nélkül törölheti a tulajdonságok értékét.

### 4. példa: alternatív előfizetési adatfájl használata
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

Ez a parancs megváltoztatja a ContosoFinance-előfizetés jelenlegi tárolási fiókját a ContosoStorage01.
A parancs a **SubscriptionDataFile** paraméterrel módosítja az adatC:\Azure\SubscriptionData.xml-előfizetés adatfájlban lévő adattípust.
A **set-AzureSubscription** alapértelmezés szerint az alapértelmezett előfizetési adatfájlt használja a központi felhasználói profilban.

## PARAMÉTEREK

### -Tanúsítvány
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Környezet
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
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

### -ResourceManagerEndpoint
Az Azure Resource Manager-adatok végpontját adja meg, például a fiókhoz társított erőforráscsoportok adatait.
Az Azure Resource Managerről az [Azure Resource Manager parancsmagok](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) és a [Windows PowerShell használata az erőforrás-kezelővel](https://go.microsoft.com/fwlink/?LinkID=394767)  című témakörben olvashat bővebben https://go.microsoft.com/fwlink/?LinkID=394767) .

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

### -ServiceEndpoint
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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
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

### Nincs vagy System. Boolean
A *PassThru* paraméter használatakor ez a parancsmag logikai értéket ad eredményül.
Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Importálás – AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Select-AzureSubscription](./Select-AzureSubscription.md)


