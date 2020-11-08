---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181645"
---
# <span data-ttu-id="2f1a4-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="2f1a4-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="2f1a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1a4-103">A függőben lévő karbantartási frissítések beszerzése az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="2f1a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f1a4-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f1a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f1a4-105">DESCRIPTION</span></span>
<span data-ttu-id="2f1a4-106">A függőben lévő karbantartási frissítések beszerzése az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="2f1a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f1a4-107">EXAMPLES</span></span>

### <span data-ttu-id="2f1a4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f1a4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="2f1a4-109">A függőben lévő karbantartási frissítések beszerzése az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="2f1a4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f1a4-110">PARAMETERS</span></span>

### <span data-ttu-id="2f1a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1a4-111">-DefaultProfile</span></span>
<span data-ttu-id="2f1a4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f1a4-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="2f1a4-113">-ProviderName</span></span>
<span data-ttu-id="2f1a4-114">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="2f1a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1a4-115">-ResourceGroupName</span></span>
<span data-ttu-id="2f1a4-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="2f1a4-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2f1a4-117">-ResourceName</span></span>
<span data-ttu-id="2f1a4-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-118">The resource name.</span></span>

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

### <span data-ttu-id="2f1a4-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="2f1a4-119">-ResourceParentName</span></span>
<span data-ttu-id="2f1a4-120">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-120">The parent resource name.</span></span>

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

### <span data-ttu-id="2f1a4-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="2f1a4-121">-ResourceParentType</span></span>
<span data-ttu-id="2f1a4-122">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-122">The parent resource type.</span></span>

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

### <span data-ttu-id="2f1a4-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2f1a4-123">-ResourceType</span></span>
<span data-ttu-id="2f1a4-124">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-124">The resource type.</span></span>

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

### <span data-ttu-id="2f1a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1a4-125">CommonParameters</span></span>
<span data-ttu-id="2f1a4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f1a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1a4-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f1a4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1a4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f1a4-128">INPUTS</span></span>

### <span data-ttu-id="2f1a4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2f1a4-129">System.String</span></span>

## <span data-ttu-id="2f1a4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f1a4-130">OUTPUTS</span></span>

### <span data-ttu-id="2f1a4-131">Microsoft. Azure. Management. Maintenance. models. Update</span><span class="sxs-lookup"><span data-stu-id="2f1a4-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="2f1a4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f1a4-132">NOTES</span></span>

## <span data-ttu-id="2f1a4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f1a4-133">RELATED LINKS</span></span>
