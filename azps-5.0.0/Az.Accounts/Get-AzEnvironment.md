---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186295"
---
# <span data-ttu-id="6a202-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a202-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="6a202-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a202-102">SYNOPSIS</span></span>
<span data-ttu-id="6a202-103">Az Azure Services egy példányának végpontját és metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a202-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="6a202-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a202-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a202-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a202-105">DESCRIPTION</span></span>
<span data-ttu-id="6a202-106">A Get-AzEnvironment parancsmag az Azure Services egy példányának végpontját és metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="6a202-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="6a202-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a202-107">EXAMPLES</span></span>

### <span data-ttu-id="6a202-108">Példa 1: a AzureCloud környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a202-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="6a202-109">Ez a példa azt szemlélteti, hogy miként szerezheti be a végpontokat és a metaadatokat a AzureCloud (alapértelmezett) környezetekhez.</span><span class="sxs-lookup"><span data-stu-id="6a202-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="6a202-110">2. példa: a AzureChinaCloud környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a202-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="6a202-111">Ebben a példában az látható, hogy miként szerezheti be a AzureChinaCloud-környezet végpontjait és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="6a202-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="6a202-112">3. példa: a AzureUSGovernment környezetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a202-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="6a202-113">Ebben a példában az látható, hogy miként szerezheti be a AzureUSGovernment-környezet végpontjait és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="6a202-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="6a202-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a202-114">PARAMETERS</span></span>

### <span data-ttu-id="6a202-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a202-115">-DefaultProfile</span></span>
<span data-ttu-id="6a202-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a202-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a202-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a202-117">-Name</span></span>
<span data-ttu-id="6a202-118">A beszerzéshez használandó Azure-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a202-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="6a202-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a202-119">CommonParameters</span></span>
<span data-ttu-id="6a202-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a202-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a202-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a202-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a202-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a202-122">INPUTS</span></span>

### <span data-ttu-id="6a202-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6a202-123">System.String</span></span>

## <span data-ttu-id="6a202-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a202-124">OUTPUTS</span></span>

### <span data-ttu-id="6a202-125">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a202-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="6a202-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a202-126">NOTES</span></span>

## <span data-ttu-id="6a202-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a202-127">RELATED LINKS</span></span>

[<span data-ttu-id="6a202-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a202-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="6a202-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a202-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="6a202-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a202-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
