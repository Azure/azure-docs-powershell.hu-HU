---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: cb077b2bdc6c91ccb3dc1c9099490c1d8bf6bea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012694"
---
# <span data-ttu-id="db01d-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="db01d-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="db01d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db01d-102">SYNOPSIS</span></span>
<span data-ttu-id="db01d-103">Egy felhőszolgáltatás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db01d-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="db01d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db01d-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="db01d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db01d-105">DESCRIPTION</span></span>
<span data-ttu-id="db01d-106">Egy felhőszolgáltatás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db01d-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="db01d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db01d-107">EXAMPLES</span></span>

### <span data-ttu-id="db01d-108">1. példa: Felhőszolgáltatás példánynézetének lekérte</span><span class="sxs-lookup"><span data-stu-id="db01d-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="db01d-109">Ez a parancsmag a ContosoCS nevű felhőszolgáltatás példánynézetét kapja meg, amely a ContosOrg nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="db01d-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="db01d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db01d-110">PARAMETERS</span></span>

### <span data-ttu-id="db01d-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="db01d-111">-CloudServiceName</span></span>
<span data-ttu-id="db01d-112">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="db01d-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="db01d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db01d-113">-DefaultProfile</span></span>
<span data-ttu-id="db01d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db01d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db01d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db01d-115">-ResourceGroupName</span></span>
<span data-ttu-id="db01d-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db01d-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="db01d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db01d-117">-SubscriptionId</span></span>
<span data-ttu-id="db01d-118">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="db01d-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db01d-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="db01d-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db01d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db01d-120">CommonParameters</span></span>
<span data-ttu-id="db01d-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db01d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db01d-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db01d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db01d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db01d-123">INPUTS</span></span>

## <span data-ttu-id="db01d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db01d-124">OUTPUTS</span></span>

### <span data-ttu-id="db01d-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="db01d-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="db01d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db01d-126">NOTES</span></span>

<span data-ttu-id="db01d-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="db01d-127">ALIASES</span></span>

## <span data-ttu-id="db01d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db01d-128">RELATED LINKS</span></span>

