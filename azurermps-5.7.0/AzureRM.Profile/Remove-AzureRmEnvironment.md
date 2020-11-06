---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502527"
---
# <span data-ttu-id="dbaf7-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="dbaf7-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="dbaf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbaf7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaf7-103">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbaf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbaf7-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbaf7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbaf7-105">DESCRIPTION</span></span>
<span data-ttu-id="dbaf7-106">A Remove-AzureRmEnvironment parancsmag eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadat-információkat.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="dbaf7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dbaf7-107">EXAMPLES</span></span>

### <span data-ttu-id="dbaf7-108">Példa 1: tesztkörnyezet létrehozása és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dbaf7-108">Example 1: Creating and removing a test environment</span></span>
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

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

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
```

<span data-ttu-id="dbaf7-109">Ez a példa bemutatja, hogyan hozhat létre környezetet a AzureRmEnvironment használatával, és hogy hogyan törölheti a környezetet a Remove-AzureRmEnvironment használatával.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="dbaf7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbaf7-110">PARAMETERS</span></span>

### <span data-ttu-id="dbaf7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaf7-111">-DefaultProfile</span></span>
<span data-ttu-id="dbaf7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbaf7-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbaf7-113">-Name</span></span>
<span data-ttu-id="dbaf7-114">Az eltávolítandó környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="dbaf7-115">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="dbaf7-115">-Scope</span></span>
<span data-ttu-id="dbaf7-116">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="dbaf7-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dbaf7-117">-Confirm</span></span>
<span data-ttu-id="dbaf7-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbaf7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbaf7-119">-WhatIf</span></span>
<span data-ttu-id="dbaf7-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbaf7-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbaf7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaf7-122">CommonParameters</span></span>
<span data-ttu-id="dbaf7-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbaf7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbaf7-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbaf7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaf7-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbaf7-125">INPUTS</span></span>

### <span data-ttu-id="dbaf7-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="dbaf7-126">None</span></span>
<span data-ttu-id="dbaf7-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dbaf7-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbaf7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbaf7-128">OUTPUTS</span></span>

### <span data-ttu-id="dbaf7-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="dbaf7-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="dbaf7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbaf7-130">NOTES</span></span>

## <span data-ttu-id="dbaf7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbaf7-131">RELATED LINKS</span></span>

[<span data-ttu-id="dbaf7-132">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="dbaf7-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="dbaf7-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="dbaf7-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="dbaf7-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="dbaf7-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

