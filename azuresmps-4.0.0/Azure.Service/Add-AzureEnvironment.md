---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015730"
---
# Add-AzureEnvironment

## Áttekintés
Azure-környezetet hoz létre.

## SZINTAXISA

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureEnvironment** parancsmag létrehoz egy új egyéni Azure-fiók környezetet, és a központi felhasználói profilba menti.
A parancsmag egy olyan objektumot ad eredményül, amely az új környezetet jelképezi.
A parancs befejeztével használhatja a környezetet a Windows PowerShellben.

Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.
A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.
További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

A parancsmag csak a **Name** paramétert kötelező megadni.
Ha kihagy egy paramétert, az értéke null ($Null), és a végpontot használó szolgáltatás nem működik megfelelően.
Egy környezeti tulajdonság értékének hozzáadásához vagy módosításához használja a **set-AzureEnvironment** parancsmagot.

Megjegyzés: a környezet módosítása következtében a fiókja sikertelen lehet.
A környezetek általában csak tesztelésre vagy hibaelhárításra kerülnek.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### 1. példa: Azure-környezet hozzáadása
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

Ez a parancs létrehozza a ContosoEnv Azure-környezetet.

## PARAMÉTEREK

### -ActiveDirectoryEndpoint
Az Azure Active Directory-hitelesítés végpontját adja meg az új környezetben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveDirectoryServiceEndpointResourceId
Annak a kezelési API-nek az erőforrás-AZONOSÍTÓját adja meg, amelynek az elérését az Azure Active Directory kezeli.

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

### -AdTenant
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

### -AzureKeyVaultDnsSuffix
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

### -AzureKeyVaultServiceEndpointResourceId
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

### -EnableAdfsAuthentication
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
Az Azure Resource Manager gyűjtemény azon végpontját adja meg, amely az erőforráscsoport-gyűjtemény sablonjait tárolja.
Az Azure Resource groups és a Gallery sablonjairól a Get-AzureResourceGroupGalleryTemplate című súgótémakörben talál további információt https://go.microsoft.com/fwlink/?LinkID=393052 .

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl
Az Azure felügyeleti portál URL-címét adja meg az új környezetben.

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

### -Name (név)
A környezet nevét adja meg.
Ehhez a paraméterhez szükség van.
Ne használja az alapértelmezett környezetek, a AzureCloud és a AzureChinaCloud nevét.

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

### -PublishSettingsFileUrl
A fiók közzétételi beállításainak URL-címét adja meg.
Az Azure közzétételi beállítások fájlja olyan XML-fájl, amely információkat tartalmaz a fiókjával és egy olyan felügyeleti tanúsítvánnyal, amely lehetővé teszi a Windows PowerShell számára az Azure-fiókjába való bejelentkezést az Ön nevében.

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

### -ResourceManagerEndpoint
Az Azure Resource Manager-adatok végpontját adja meg, például a fiókhoz társított erőforráscsoportok adatait.
Az Azure Resource Managerről az [Azure Resource Manager parancsmagok](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) és a [Windows PowerShell használata az erőforrás-kezelővel](https://go.microsoft.com/fwlink/?LinkID=394767)  című témakörben olvashat bővebben https://go.microsoft.com/fwlink/?LinkID=394767) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Az Azure Service végpont URL-címét adja meg.
Az Azure szolgáltatás végpontja azt határozza meg, hogy az alkalmazást a 21Vianet által Kínában üzemeltetett globális Azure platform, illetve egy privát Azure-példány kezeli-e.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
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

### -StorageEndpoint
A tárolási szolgáltatások alapértelmezett végpontját adja meg az új környezetben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
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

### Microsoft. WindowsAzure. commands. Utilities. Common. WindowsAzureEnvironment

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


