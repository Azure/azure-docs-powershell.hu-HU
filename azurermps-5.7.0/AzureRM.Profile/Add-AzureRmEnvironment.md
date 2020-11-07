---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ef4f5128e92a319cb2b8ca021fc9b86f484d9b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672015"
---
# Add-AzureRmEnvironment

## Áttekintés
Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Név (alapértelmezett)
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ARMEndpoint
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az Add-AzureRmEnvironment parancsmag végpontokat és metaadatokat ad hozzá az Azure Resource Manager parancsmagok számára az Azure Resource Manager új példányához való csatlakozáshoz.
A beépített környezetek AzureCloud és AzureChinaCloud az Azure Resource Manager meglévő nyilvános példányainak megcélzására.

## Példák

### 1. példa: új környezet létrehozása és módosítása
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzureRmEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzureRmEnvironment segítségével változtatjuk meg.

## PARAMÉTEREK

### -ActiveDirectoryEndpoint
Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveDirectoryServiceEndpointResourceId
Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdTenant
Az alapértelmezett Active Directory-bérlőt adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ARMEndpoint
Az Azure Resource Manager végpontja

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix
Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureDataLakeStoreFileSystemEndpointSuffix
Az Azure Data Lake Store FileSystem DNS-utótagja.
Példa: azuredatalake.net

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureKeyVaultDnsSuffix
A fő Vault-szolgáltatások tartománynév-utótagját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureKeyVaultServiceEndpointResourceId
Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyek engedélyezik a Key Vault-szolgáltatások kérését.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataLakeAudience
Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
A credeetnails, a bérlő és az azuretal való kommunikációhoz használt előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAdfsAuthentication
Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphAudience
Az AD gráf végpontját hitelesítő tokenek közönsége.

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
A Graph (Active Directory metadata) kérések URL-címét adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl
A felügyeleti portál URL-címét adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A hozzáadni kívánt környezet nevét adja meg.

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

### -PublishSettingsFileUrl
Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceManagerEndpoint
Az Azure Resource Manager-kérések URL-címét adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope (hatókör)
Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceEndpoint
A Service Management (RDFE) kérések végpontját adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpoint
A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BatchEndpointResourceId
Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureOperationalInsightsEndpoint
Az üzemeltetési keresési lekérdezések elérésének végpontját adja meg. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureOperationalInsightsEndpointResourceId
Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyeknek az üzemeltetési szolgáltatásokra vonatkozó kérelmeket engedélyeztek.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### PSAzureEnvironment
Ez a parancsmag az Azure-példányokkal való kommunikációhoz szükséges végpontok és metaadatok halmazát adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRMEnvironment](./Get-AzureRMEnvironment.md)

[Remove-AzureRMEnvironment](./Remove-AzureRMEnvironment.md)

[Set-AzureRMEnvironment](./Set-AzureRMEnvironment.md)

