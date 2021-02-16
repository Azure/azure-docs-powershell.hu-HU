---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149026"
---
# <span data-ttu-id="e2a39-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="e2a39-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="e2a39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a39-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a39-103">A felhőszolgáltatás szerepkörpéldányának futásidővel kapcsolatos állapotáról olvassa be az adatokat.</span><span class="sxs-lookup"><span data-stu-id="e2a39-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="e2a39-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2a39-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e2a39-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2a39-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a39-106">A felhőszolgáltatás szerepkörpéldányának futásidővel kapcsolatos állapotáról olvassa be az adatokat.</span><span class="sxs-lookup"><span data-stu-id="e2a39-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="e2a39-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2a39-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a39-108">1. példa: Példánynézet részleteinek lekérte a felhőbeli szolgáltatás szerepkörpéldányát</span><span class="sxs-lookup"><span data-stu-id="e2a39-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="e2a39-109">Ez a parancsmag a ContosOrg nevű erőforráscsoporthoz tartozó ContosoCS nevű felhőszolgáltatás ContosoFrontEnd_IN_0 példányának példánynézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="e2a39-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="e2a39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2a39-110">PARAMETERS</span></span>

### <span data-ttu-id="e2a39-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="e2a39-111">-CloudServiceName</span></span>
<span data-ttu-id="e2a39-112">.</span><span class="sxs-lookup"><span data-stu-id="e2a39-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a39-113">-DefaultProfile</span></span>
<span data-ttu-id="e2a39-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2a39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a39-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a39-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2a39-116">.</span><span class="sxs-lookup"><span data-stu-id="e2a39-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a39-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="e2a39-117">-RoleInstanceName</span></span>
<span data-ttu-id="e2a39-118">A szerepkörpéldány neve.</span><span class="sxs-lookup"><span data-stu-id="e2a39-118">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a39-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2a39-119">-SubscriptionId</span></span>
<span data-ttu-id="e2a39-120">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e2a39-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2a39-121">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e2a39-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a39-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a39-122">CommonParameters</span></span>
<span data-ttu-id="e2a39-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a39-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a39-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2a39-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a39-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2a39-125">INPUTS</span></span>

## <span data-ttu-id="e2a39-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2a39-126">OUTPUTS</span></span>

### <span data-ttu-id="e2a39-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="e2a39-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="e2a39-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2a39-128">NOTES</span></span>

<span data-ttu-id="e2a39-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e2a39-129">ALIASES</span></span>

## <span data-ttu-id="e2a39-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2a39-130">RELATED LINKS</span></span>

