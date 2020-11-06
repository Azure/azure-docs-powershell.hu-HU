---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495795"
---
# <span data-ttu-id="a33ce-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a33ce-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="a33ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a33ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a33ce-103">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a33ce-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a33ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a33ce-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a33ce-105">DESCRIPTION</span></span>
<span data-ttu-id="a33ce-106">A Get-AzureRmEnvironment parancsmag az Azure Services egy példányának végpontját és metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="a33ce-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a33ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a33ce-107">EXAMPLES</span></span>

### <span data-ttu-id="a33ce-108">Példa 1: a AzureCloud környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a33ce-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="a33ce-109">Ez a példa azt szemlélteti, hogy miként szerezheti be a végpontokat és a metaadatokat a AzureCloud (alapértelmezett) környezetekhez.</span><span class="sxs-lookup"><span data-stu-id="a33ce-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="a33ce-110">2. példa: a AzureChinaCloud környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a33ce-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

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

<span data-ttu-id="a33ce-111">Ebben a példában az látható, hogy miként szerezheti be a AzureChinaCloud-környezet végpontjait és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="a33ce-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="a33ce-112">3. példa: a AzureUSGovernment környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a33ce-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="a33ce-113">Ebben a példában az látható, hogy miként szerezheti be a AzureUSGovernment-környezet végpontjait és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="a33ce-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="a33ce-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a33ce-114">PARAMETERS</span></span>

### <span data-ttu-id="a33ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33ce-115">-DefaultProfile</span></span>
<span data-ttu-id="a33ce-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a33ce-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33ce-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a33ce-117">-Name</span></span>
<span data-ttu-id="a33ce-118">A beszerzéshez használandó Azure-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a33ce-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33ce-119">CommonParameters</span></span>
<span data-ttu-id="a33ce-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a33ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33ce-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a33ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33ce-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33ce-122">INPUTS</span></span>

### <span data-ttu-id="a33ce-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a33ce-123">System.String</span></span>

## <span data-ttu-id="a33ce-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33ce-124">OUTPUTS</span></span>

### <span data-ttu-id="a33ce-125">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a33ce-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a33ce-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a33ce-126">NOTES</span></span>

## <span data-ttu-id="a33ce-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a33ce-127">RELATED LINKS</span></span>

[<span data-ttu-id="a33ce-128">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a33ce-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="a33ce-129">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a33ce-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="a33ce-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a33ce-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

