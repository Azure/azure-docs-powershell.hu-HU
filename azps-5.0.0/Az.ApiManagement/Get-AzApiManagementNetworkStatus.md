---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302207"
---
# <span data-ttu-id="444e5-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="444e5-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="444e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="444e5-102">SYNOPSIS</span></span>
<span data-ttu-id="444e5-103">A kapcsolat állapotát a külső erőforrásokra kapja, amelyeken az API-kezelési szolgáltatás a felhőalapú szolgáltatástól függ.</span><span class="sxs-lookup"><span data-stu-id="444e5-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="444e5-104">Ez a funkció a DNS-kiszolgálókat is megjeleníti a CloudService látható módon.</span><span class="sxs-lookup"><span data-stu-id="444e5-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="444e5-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="444e5-105">SYNTAX</span></span>

### <span data-ttu-id="444e5-106">ByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="444e5-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="444e5-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="444e5-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="444e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="444e5-108">DESCRIPTION</span></span>
<span data-ttu-id="444e5-109">Az API-kezelési szolgáltatás hálózati állapotát kapja meg</span><span class="sxs-lookup"><span data-stu-id="444e5-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="444e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="444e5-110">EXAMPLES</span></span>

### <span data-ttu-id="444e5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="444e5-111">Example 1</span></span>
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

<span data-ttu-id="444e5-112">Az ApiManagement szolgáltatástól függ, hogy milyen kapcsolati állapotot kap a különböző erőforrásokhoz.</span><span class="sxs-lookup"><span data-stu-id="444e5-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="444e5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="444e5-113">PARAMETERS</span></span>

### <span data-ttu-id="444e5-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="444e5-114">-ApiManagementObject</span></span>
<span data-ttu-id="444e5-115">A PsApiManagement példánya.</span><span class="sxs-lookup"><span data-stu-id="444e5-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="444e5-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="444e5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="444e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444e5-117">-DefaultProfile</span></span>
<span data-ttu-id="444e5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="444e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444e5-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="444e5-119">-Location</span></span>
<span data-ttu-id="444e5-120">Az API-kezelési szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="444e5-120">Location of the API Management Service.</span></span>

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

### <span data-ttu-id="444e5-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="444e5-121">-Name</span></span>
<span data-ttu-id="444e5-122">Az API-kezelés neve.</span><span class="sxs-lookup"><span data-stu-id="444e5-122">Name of API Management.</span></span>

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

### <span data-ttu-id="444e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="444e5-124">Annak az erőforráscsoportnek a neve, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="444e5-124">Name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="444e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444e5-125">CommonParameters</span></span>
<span data-ttu-id="444e5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="444e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444e5-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="444e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444e5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="444e5-128">INPUTS</span></span>

### <span data-ttu-id="444e5-129">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="444e5-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="444e5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="444e5-130">System.String</span></span>

## <span data-ttu-id="444e5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="444e5-131">OUTPUTS</span></span>

### <span data-ttu-id="444e5-132">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="444e5-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="444e5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="444e5-133">NOTES</span></span>

## <span data-ttu-id="444e5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="444e5-134">RELATED LINKS</span></span>
