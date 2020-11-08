---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016352"
---
# Get-AzureEnvironment

## Áttekintés
Azure-környezetek beolvasása

## SZINTAXISA

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureEnvironment** parancsmag a Windows powershellhez elérhető Azure-környezetet kapja.

Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.
A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.
További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

A **Get-AzureEnvironment** parancsmag nem az Azure-ról származó környezetekre, hanem az előfizetési adatfájlból kapja a környezetét.
Ha az előfizetési adatfájl elavult, futtassa a **Add-AzureAccount** vagy az **import-PublishSettingsFile** parancsmagot a frissítéséhez.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: az összes környezet beszerzése
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Ez a parancs a Windows PowerShellhez elérhető összes környezetet bekapja.

### 2. példa: környezet beszerzése név alapján
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

Ez a példa a AzureCloud környezetet kapja.

### 3. példa: a minden környezet összes tulajdonságának lekérése
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Ez a parancs a környezet minden tulajdonságát beolvassa.

A parancs a **Get-AzureEnvironment** parancsmagot használja az Azure-környezetek ehhez a fiókhoz való beolvasásához.
Ezután a **foreach-Object** parancsmagot használja a **Get-AzureEnvironment** parancs futtatásához az egyes környezetekben a **Name** paraméterrel.
A **Name** paraméter értéke az egyes környezetek **EnvironmentName** tulajdonsága.

Paraméterek nélkül a **Get-AzureEnvironment** csak a környezet kijelölt tulajdonságait kapja meg.

## PARAMÉTEREK

### -Name (név)
Csak a megadott környezetet kapja meg.
Írja be a környezet nevét.
A paraméter értéke megkülönbözteti a kis-és nagybetűket.
A helyettesítő karakterek nem engedélyezettek.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### System. Management. Automation. PSCustomObject
Alapértelmezés szerint a **Get-AzureEnvironment** egy egyéni objektumot ad eredményül.

### Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureEnvironment
Amikor a **Get-AzureEnvironment** a **Name** paraméterrel futtatja, a  **WindowsAzureEnvironment** -objektumot adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Importálás – AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


