---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478945"
---
# <span data-ttu-id="8d3ad-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="8d3ad-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="8d3ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="8d3ad-103">Azon külső erőforrások kapcsolati állapotát kapja meg, amelyektől az Api Management szolgáltatás a felhőszolgáltatáson belülről függ.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="8d3ad-104">Ez a dns-kiszolgálókat is a CloudService által láthatóként adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="8d3ad-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d3ad-105">SYNTAX</span></span>

### <span data-ttu-id="8d3ad-106">ByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d3ad-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d3ad-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="8d3ad-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d3ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d3ad-108">DESCRIPTION</span></span>
<span data-ttu-id="8d3ad-109">Az API-kezelési szolgáltatás hálózati állapotának lekérte</span><span class="sxs-lookup"><span data-stu-id="8d3ad-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="8d3ad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d3ad-110">EXAMPLES</span></span>

### <span data-ttu-id="8d3ad-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d3ad-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="8d3ad-112">Annak a különböző erőforrásoknak a kapcsolati állapotát kapja meg, amelyektől az ApiManagement szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="8d3ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d3ad-113">PARAMETERS</span></span>

### <span data-ttu-id="8d3ad-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="8d3ad-114">-ApiManagementObject</span></span>
<span data-ttu-id="8d3ad-115">A PsApiManagement példánya.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="8d3ad-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d3ad-117">-DefaultProfile</span></span>
<span data-ttu-id="8d3ad-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d3ad-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8d3ad-119">-Location</span></span>
<span data-ttu-id="8d3ad-120">Az API-kezelési szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-120">Location of the API Management Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d3ad-121">-Name</span></span>
<span data-ttu-id="8d3ad-122">Az API-kezelés neve.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-122">Name of API Management.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d3ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d3ad-124">Annak az erőforráscsoportnak a neve, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-124">Name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3ad-125">CommonParameters</span></span>
<span data-ttu-id="8d3ad-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3ad-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d3ad-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3ad-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d3ad-128">INPUTS</span></span>

### <span data-ttu-id="8d3ad-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d3ad-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="8d3ad-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8d3ad-130">System.String</span></span>

## <span data-ttu-id="8d3ad-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d3ad-131">OUTPUTS</span></span>

### <span data-ttu-id="8d3ad-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="8d3ad-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="8d3ad-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d3ad-133">NOTES</span></span>

## <span data-ttu-id="8d3ad-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d3ad-134">RELATED LINKS</span></span>
