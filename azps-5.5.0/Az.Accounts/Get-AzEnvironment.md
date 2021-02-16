---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157715"
---
# <span data-ttu-id="bd391-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bd391-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="bd391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd391-102">SYNOPSIS</span></span>
<span data-ttu-id="bd391-103">Végpontok és metaadatok lekérte az Azure-szolgáltatások egy példányát.</span><span class="sxs-lookup"><span data-stu-id="bd391-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="bd391-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd391-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd391-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd391-105">DESCRIPTION</span></span>
<span data-ttu-id="bd391-106">A Get-AzEnvironment parancsmag végpontokat és metaadatokat kap az Azure-szolgáltatások egy példányához.</span><span class="sxs-lookup"><span data-stu-id="bd391-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="bd391-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd391-107">EXAMPLES</span></span>

### <span data-ttu-id="bd391-108">1. példa: Az AzureCloud környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="bd391-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="bd391-109">Az alábbi példa bemutatja, hogyan lehet lekértékérték az AzureCloud -környezet végpontját és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="bd391-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="bd391-110">2. példa: Az AzureChinaCloud környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="bd391-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="bd391-111">Az alábbi példa bemutatja, hogyan lehet lekérte a végpontokat és a metaadatokat az AzureChinaCloud környezethez.</span><span class="sxs-lookup"><span data-stu-id="bd391-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="bd391-112">3. példa: Az AzureUSGovernment környezet levétele</span><span class="sxs-lookup"><span data-stu-id="bd391-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="bd391-113">Az alábbi példa bemutatja, hogy miként lehet lekérte az AzureUSGovernment környezet végpontját és metaadatait.</span><span class="sxs-lookup"><span data-stu-id="bd391-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="bd391-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd391-114">PARAMETERS</span></span>

### <span data-ttu-id="bd391-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd391-115">-DefaultProfile</span></span>
<span data-ttu-id="bd391-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd391-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd391-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bd391-117">-Name</span></span>
<span data-ttu-id="bd391-118">A lekért Azure-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd391-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="bd391-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd391-119">CommonParameters</span></span>
<span data-ttu-id="bd391-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd391-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd391-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd391-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd391-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd391-122">INPUTS</span></span>

### <span data-ttu-id="bd391-123">System.String</span><span class="sxs-lookup"><span data-stu-id="bd391-123">System.String</span></span>

## <span data-ttu-id="bd391-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd391-124">OUTPUTS</span></span>

### <span data-ttu-id="bd391-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bd391-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="bd391-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd391-126">NOTES</span></span>

## <span data-ttu-id="bd391-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd391-127">RELATED LINKS</span></span>

[<span data-ttu-id="bd391-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bd391-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="bd391-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bd391-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="bd391-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="bd391-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

