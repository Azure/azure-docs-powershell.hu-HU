---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018026"
---
# <span data-ttu-id="70f65-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="70f65-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="70f65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70f65-102">SYNOPSIS</span></span>
<span data-ttu-id="70f65-103">A kapcsolat állapotát a külső erőforrásokra kapja, amelyeken az API-kezelési szolgáltatás a felhőalapú szolgáltatástól függ.</span><span class="sxs-lookup"><span data-stu-id="70f65-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="70f65-104">Ez a funkció a DNS-kiszolgálókat is megjeleníti a CloudService látható módon.</span><span class="sxs-lookup"><span data-stu-id="70f65-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="70f65-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70f65-105">SYNTAX</span></span>

### <span data-ttu-id="70f65-106">ByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70f65-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70f65-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="70f65-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70f65-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="70f65-108">DESCRIPTION</span></span>
<span data-ttu-id="70f65-109">Az API-kezelési szolgáltatás hálózati állapotát kapja meg</span><span class="sxs-lookup"><span data-stu-id="70f65-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="70f65-110">Példák</span><span class="sxs-lookup"><span data-stu-id="70f65-110">EXAMPLES</span></span>

### <span data-ttu-id="70f65-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="70f65-111">Example 1</span></span>
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

<span data-ttu-id="70f65-112">Az ApiManagement szolgáltatástól függ, hogy milyen kapcsolati állapotot kap a különböző erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="70f65-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="70f65-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70f65-113">PARAMETERS</span></span>

### <span data-ttu-id="70f65-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="70f65-114">-ApiManagementObject</span></span>
<span data-ttu-id="70f65-115">A PsApiManagement példánya.</span><span class="sxs-lookup"><span data-stu-id="70f65-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="70f65-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="70f65-116">This parameter is required.</span></span>

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

### <span data-ttu-id="70f65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f65-117">-DefaultProfile</span></span>
<span data-ttu-id="70f65-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70f65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f65-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="70f65-119">-Location</span></span>
<span data-ttu-id="70f65-120">Az API-kezelési szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="70f65-120">Location of the API Management Service.</span></span>

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

### <span data-ttu-id="70f65-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70f65-121">-Name</span></span>
<span data-ttu-id="70f65-122">Az API-kezelés neve.</span><span class="sxs-lookup"><span data-stu-id="70f65-122">Name of API Management.</span></span>

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

### <span data-ttu-id="70f65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f65-123">-ResourceGroupName</span></span>
<span data-ttu-id="70f65-124">Annak az erőforráscsoportnek a neve, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="70f65-124">Name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="70f65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f65-125">CommonParameters</span></span>
<span data-ttu-id="70f65-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70f65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f65-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70f65-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f65-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f65-128">INPUTS</span></span>

### <span data-ttu-id="70f65-129">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="70f65-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="70f65-130">System. String</span><span class="sxs-lookup"><span data-stu-id="70f65-130">System.String</span></span>

## <span data-ttu-id="70f65-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f65-131">OUTPUTS</span></span>

### <span data-ttu-id="70f65-132">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="70f65-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="70f65-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70f65-133">NOTES</span></span>

## <span data-ttu-id="70f65-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70f65-134">RELATED LINKS</span></span>
