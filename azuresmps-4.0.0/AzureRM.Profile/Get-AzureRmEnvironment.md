---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 960a7f61ba181f267b264b27991f33a7b522c4e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491168"
---
# <span data-ttu-id="ff041-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff041-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="ff041-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff041-102">SYNOPSIS</span></span>
<span data-ttu-id="ff041-103">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ff041-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="ff041-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff041-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff041-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff041-105">DESCRIPTION</span></span>
<span data-ttu-id="ff041-106">A Get-AzureRmEnvironment parancsmag az Azure Services egy példányának végpontját és metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ff041-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="ff041-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff041-107">EXAMPLES</span></span>

### <span data-ttu-id="ff041-108">Példa 1: a AzureCloud környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ff041-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name                                              : AzureCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.windows.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.azure.com/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=254433
ServiceManagementUrl                              : https://management.core.windows.net/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301775
ResourceManagerUrl                                : https://management.azure.com/
SqlDatabaseDnsSuffix                              : .database.windows.net
StorageEndpointSuffix                             : core.windows.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : trafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.azure.net
AzureDataLakeStoreFileSystemEndpointSuffix        : azuredatalakestore.net
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix : azuredatalakeanalytics.net
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.net
```

<span data-ttu-id="ff041-109">Ez a példa azt szemlélteti, hogy miként szerezheti be a végpontokat és a metaadatokat a AzureCloud (alapértelmezett) környezetekhez.</span><span class="sxs-lookup"><span data-stu-id="ff041-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="ff041-110">2. példa: a AzureChinaCloud környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ff041-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="ff041-111">Ebben a példában az látható, hogy miként szerezheti be a AzureChinaCloud-környezet végpontjait és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="ff041-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="ff041-112">3. példa: a AzureUSGovernment környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ff041-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name                                              : AzureUSGovernment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.usgovcloudapi.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.usgovcloudapi.net/
ManagementPortalUrl                               : https://manage.windowsazure.us
ServiceManagementUrl                              : https://management.core.usgovcloudapi.net/
PublishSettingsFileUrl                            : https://manage.windowsazure.us/publishsettings/index
ResourceManagerUrl                                : https://management.usgovcloudapi.net/
SqlDatabaseDnsSuffix                              : .database.usgovcloudapi.net
StorageEndpointSuffix                             : core.usgovcloudapi.net
ActiveDirectoryAuthority                          : https://login-us.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

<span data-ttu-id="ff041-113">Ebben a példában az látható, hogy miként szerezheti be a AzureUSGovernment-környezet végpontjait és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="ff041-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="ff041-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff041-114">PARAMETERS</span></span>

### <span data-ttu-id="ff041-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff041-115">-Name</span></span>
<span data-ttu-id="ff041-116">A beszerzéshez használandó Azure-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff041-116">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff041-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff041-117">CommonParameters</span></span>
<span data-ttu-id="ff041-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff041-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff041-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff041-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff041-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff041-120">INPUTS</span></span>

## <span data-ttu-id="ff041-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff041-121">OUTPUTS</span></span>

### <span data-ttu-id="ff041-122">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff041-122">PSAzureEnvironment</span></span>

## <span data-ttu-id="ff041-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff041-123">NOTES</span></span>

## <span data-ttu-id="ff041-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff041-124">RELATED LINKS</span></span>

[<span data-ttu-id="ff041-125">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff041-125">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="ff041-126">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff041-126">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="ff041-127">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff041-127">Set-AzureRMEnvironment</span></span>]()

