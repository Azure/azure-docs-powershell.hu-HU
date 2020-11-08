---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187699"
---
# <span data-ttu-id="f6486-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="f6486-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="f6486-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6486-102">SYNOPSIS</span></span>
<span data-ttu-id="f6486-103">Karbantartási frissítések alkalmazása az erőforrásokra</span><span class="sxs-lookup"><span data-stu-id="f6486-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="f6486-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6486-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6486-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6486-105">DESCRIPTION</span></span>
<span data-ttu-id="f6486-106">Karbantartási frissítések alkalmazása az erőforrásokra</span><span class="sxs-lookup"><span data-stu-id="f6486-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="f6486-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6486-107">EXAMPLES</span></span>

### <span data-ttu-id="f6486-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6486-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="f6486-109">Karbantartási frissítések alkalmazása az erőforrásokra</span><span class="sxs-lookup"><span data-stu-id="f6486-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="f6486-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6486-110">PARAMETERS</span></span>

### <span data-ttu-id="f6486-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6486-111">-AsJob</span></span>
<span data-ttu-id="f6486-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f6486-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6486-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6486-113">-DefaultProfile</span></span>
<span data-ttu-id="f6486-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6486-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6486-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f6486-115">-ProviderName</span></span>
<span data-ttu-id="f6486-116">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="f6486-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="f6486-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6486-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6486-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6486-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="f6486-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f6486-119">-ResourceName</span></span>
<span data-ttu-id="f6486-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6486-120">The resource name.</span></span>

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

### <span data-ttu-id="f6486-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f6486-121">-ResourceParentName</span></span>
<span data-ttu-id="f6486-122">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6486-122">The parent resource name.</span></span>

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

### <span data-ttu-id="f6486-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f6486-123">-ResourceParentType</span></span>
<span data-ttu-id="f6486-124">A szülő-erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f6486-124">The parent resource type.</span></span>

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

### <span data-ttu-id="f6486-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f6486-125">-ResourceType</span></span>
<span data-ttu-id="f6486-126">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="f6486-126">The resource type.</span></span>

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

### <span data-ttu-id="f6486-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6486-127">-Confirm</span></span>
<span data-ttu-id="f6486-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6486-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6486-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6486-129">-WhatIf</span></span>
<span data-ttu-id="f6486-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6486-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6486-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6486-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6486-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6486-132">CommonParameters</span></span>
<span data-ttu-id="f6486-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6486-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6486-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f6486-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6486-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6486-135">INPUTS</span></span>

### <span data-ttu-id="f6486-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f6486-136">System.String</span></span>

## <span data-ttu-id="f6486-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6486-137">OUTPUTS</span></span>

### <span data-ttu-id="f6486-138">Microsoft. Azure. commands. Maintenance. models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="f6486-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="f6486-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6486-139">NOTES</span></span>

## <span data-ttu-id="f6486-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6486-140">RELATED LINKS</span></span>
