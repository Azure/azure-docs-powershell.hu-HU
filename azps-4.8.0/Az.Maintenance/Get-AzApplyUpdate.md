---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181657"
---
# <span data-ttu-id="8aec1-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="8aec1-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="8aec1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8aec1-102">SYNOPSIS</span></span>
<span data-ttu-id="8aec1-103">Az erőforrás karbantartási frissítéseinek nyomon követése</span><span class="sxs-lookup"><span data-stu-id="8aec1-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="8aec1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8aec1-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aec1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8aec1-105">DESCRIPTION</span></span>
<span data-ttu-id="8aec1-106">Az erőforrás karbantartási frissítéseinek nyomon követése</span><span class="sxs-lookup"><span data-stu-id="8aec1-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="8aec1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8aec1-107">EXAMPLES</span></span>

### <span data-ttu-id="8aec1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8aec1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="8aec1-109">Az erőforrás karbantartási frissítéseinek nyomon követése</span><span class="sxs-lookup"><span data-stu-id="8aec1-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="8aec1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8aec1-110">PARAMETERS</span></span>

### <span data-ttu-id="8aec1-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="8aec1-111">-ApplyUpdateName</span></span>
<span data-ttu-id="8aec1-112">A frissítési erőforrás nevének alkalmazása</span><span class="sxs-lookup"><span data-stu-id="8aec1-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aec1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aec1-113">-DefaultProfile</span></span>
<span data-ttu-id="8aec1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8aec1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aec1-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="8aec1-115">-ProviderName</span></span>
<span data-ttu-id="8aec1-116">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="8aec1-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="8aec1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aec1-117">-ResourceGroupName</span></span>
<span data-ttu-id="8aec1-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8aec1-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="8aec1-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8aec1-119">-ResourceName</span></span>
<span data-ttu-id="8aec1-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8aec1-120">The resource name.</span></span>

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

### <span data-ttu-id="8aec1-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="8aec1-121">-ResourceParentName</span></span>
<span data-ttu-id="8aec1-122">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8aec1-122">The parent resource name.</span></span>

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

### <span data-ttu-id="8aec1-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="8aec1-123">-ResourceParentType</span></span>
<span data-ttu-id="8aec1-124">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="8aec1-124">The parent resource type.</span></span>

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

### <span data-ttu-id="8aec1-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8aec1-125">-ResourceType</span></span>
<span data-ttu-id="8aec1-126">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="8aec1-126">The resource type.</span></span>

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

### <span data-ttu-id="8aec1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aec1-127">CommonParameters</span></span>
<span data-ttu-id="8aec1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8aec1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aec1-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8aec1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aec1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8aec1-130">INPUTS</span></span>

### <span data-ttu-id="8aec1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8aec1-131">System.String</span></span>

## <span data-ttu-id="8aec1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8aec1-132">OUTPUTS</span></span>

### <span data-ttu-id="8aec1-133">Microsoft. Azure. commands. Maintenance. models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="8aec1-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="8aec1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8aec1-134">NOTES</span></span>

## <span data-ttu-id="8aec1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8aec1-135">RELATED LINKS</span></span>
