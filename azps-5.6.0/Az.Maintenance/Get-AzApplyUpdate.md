---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: c6ebe985d0242e626d0a417d4af3a60388cbc776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008790"
---
# <span data-ttu-id="2e0fa-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="2e0fa-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="2e0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0fa-103">Az erőforrás karbantartási frissítésének nyomon követése</span><span class="sxs-lookup"><span data-stu-id="2e0fa-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="2e0fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e0fa-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e0fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2e0fa-106">Az erőforrás karbantartási frissítésének nyomon követése</span><span class="sxs-lookup"><span data-stu-id="2e0fa-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="2e0fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="2e0fa-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2e0fa-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="2e0fa-109">Az erőforrás karbantartási frissítésének nyomon követése</span><span class="sxs-lookup"><span data-stu-id="2e0fa-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="2e0fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e0fa-110">PARAMETERS</span></span>

### <span data-ttu-id="2e0fa-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="2e0fa-111">-ApplyUpdateName</span></span>
<span data-ttu-id="2e0fa-112">A frissítési erőforrás nevének alkalmazása</span><span class="sxs-lookup"><span data-stu-id="2e0fa-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="2e0fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0fa-113">-DefaultProfile</span></span>
<span data-ttu-id="2e0fa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e0fa-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="2e0fa-115">-ProviderName</span></span>
<span data-ttu-id="2e0fa-116">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="2e0fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e0fa-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="2e0fa-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2e0fa-119">-ResourceName</span></span>
<span data-ttu-id="2e0fa-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-120">The resource name.</span></span>

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

### <span data-ttu-id="2e0fa-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="2e0fa-121">-ResourceParentName</span></span>
<span data-ttu-id="2e0fa-122">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-122">The parent resource name.</span></span>

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

### <span data-ttu-id="2e0fa-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="2e0fa-123">-ResourceParentType</span></span>
<span data-ttu-id="2e0fa-124">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-124">The parent resource type.</span></span>

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

### <span data-ttu-id="2e0fa-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2e0fa-125">-ResourceType</span></span>
<span data-ttu-id="2e0fa-126">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-126">The resource type.</span></span>

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

### <span data-ttu-id="2e0fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0fa-127">CommonParameters</span></span>
<span data-ttu-id="2e0fa-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e0fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0fa-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e0fa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0fa-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e0fa-130">INPUTS</span></span>

### <span data-ttu-id="2e0fa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2e0fa-131">System.String</span></span>

## <span data-ttu-id="2e0fa-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e0fa-132">OUTPUTS</span></span>

### <span data-ttu-id="2e0fa-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="2e0fa-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="2e0fa-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e0fa-134">NOTES</span></span>

## <span data-ttu-id="2e0fa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e0fa-135">RELATED LINKS</span></span>
