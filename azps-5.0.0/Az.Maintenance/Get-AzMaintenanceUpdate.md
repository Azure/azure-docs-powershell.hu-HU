---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187353"
---
# <span data-ttu-id="f59ff-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="f59ff-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="f59ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f59ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f59ff-103">A függőben lévő karbantartási frissítések beszerzése az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="f59ff-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="f59ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f59ff-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f59ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f59ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f59ff-106">A függőben lévő karbantartási frissítések beszerzése az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="f59ff-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="f59ff-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f59ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f59ff-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f59ff-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="f59ff-109">A függőben lévő karbantartási frissítések beszerzése az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="f59ff-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="f59ff-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f59ff-110">PARAMETERS</span></span>

### <span data-ttu-id="f59ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59ff-111">-DefaultProfile</span></span>
<span data-ttu-id="f59ff-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f59ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59ff-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f59ff-113">-ProviderName</span></span>
<span data-ttu-id="f59ff-114">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="f59ff-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="f59ff-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f59ff-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ff-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f59ff-117">-ResourceName</span></span>
<span data-ttu-id="f59ff-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f59ff-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ff-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f59ff-119">-ResourceParentName</span></span>
<span data-ttu-id="f59ff-120">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f59ff-120">The parent resource name.</span></span>

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

### <span data-ttu-id="f59ff-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f59ff-121">-ResourceParentType</span></span>
<span data-ttu-id="f59ff-122">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f59ff-122">The parent resource type.</span></span>

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

### <span data-ttu-id="f59ff-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f59ff-123">-ResourceType</span></span>
<span data-ttu-id="f59ff-124">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f59ff-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59ff-125">CommonParameters</span></span>
<span data-ttu-id="f59ff-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f59ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59ff-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f59ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59ff-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f59ff-128">INPUTS</span></span>

### <span data-ttu-id="f59ff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f59ff-129">System.String</span></span>

## <span data-ttu-id="f59ff-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f59ff-130">OUTPUTS</span></span>

### <span data-ttu-id="f59ff-131">Microsoft. Azure. Management. Maintenance. models. Update</span><span class="sxs-lookup"><span data-stu-id="f59ff-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="f59ff-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f59ff-132">NOTES</span></span>

## <span data-ttu-id="f59ff-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f59ff-133">RELATED LINKS</span></span>
