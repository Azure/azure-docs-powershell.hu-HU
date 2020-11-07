---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671750"
---
# <span data-ttu-id="f243e-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f243e-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="f243e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f243e-102">SYNOPSIS</span></span>
<span data-ttu-id="f243e-103">Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="f243e-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="f243e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f243e-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f243e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f243e-105">DESCRIPTION</span></span>
<span data-ttu-id="f243e-106">A Remove-AzureRmEnvironment parancsmag eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadat-információkat.</span><span class="sxs-lookup"><span data-stu-id="f243e-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="f243e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f243e-107">EXAMPLES</span></span>

### <span data-ttu-id="f243e-108">Példa 1: tesztkörnyezet létrehozása és eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f243e-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="f243e-109">Ez a példa bemutatja, hogyan hozhat létre környezetet a AzureRmEnvironment használatával, és hogy hogyan törölheti a környezetet a Remove-AzureRmEnvironment használatával.</span><span class="sxs-lookup"><span data-stu-id="f243e-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="f243e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f243e-110">PARAMETERS</span></span>

### <span data-ttu-id="f243e-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f243e-111">-Name</span></span>
<span data-ttu-id="f243e-112">Az eltávolítandó környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f243e-112">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="f243e-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f243e-113">-Confirm</span></span>
<span data-ttu-id="f243e-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f243e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f243e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f243e-115">-WhatIf</span></span>
<span data-ttu-id="f243e-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f243e-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f243e-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f243e-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f243e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f243e-118">CommonParameters</span></span>
<span data-ttu-id="f243e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f243e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f243e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f243e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f243e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f243e-121">INPUTS</span></span>

## <span data-ttu-id="f243e-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f243e-122">OUTPUTS</span></span>

### <span data-ttu-id="f243e-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f243e-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="f243e-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f243e-124">NOTES</span></span>

## <span data-ttu-id="f243e-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f243e-125">RELATED LINKS</span></span>

[<span data-ttu-id="f243e-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f243e-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="f243e-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f243e-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="f243e-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f243e-128">Set-AzureRMEnvironment</span></span>]()

