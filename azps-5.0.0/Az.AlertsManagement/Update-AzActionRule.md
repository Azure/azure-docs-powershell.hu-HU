---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296603"
---
# <span data-ttu-id="7cc41-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="7cc41-101">Update-AzActionRule</span></span>

## <span data-ttu-id="7cc41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cc41-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc41-103">A műveleti szabály tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="7cc41-103">Updates action rule properties.</span></span>

## <span data-ttu-id="7cc41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cc41-104">SYNTAX</span></span>

### <span data-ttu-id="7cc41-105">ByNameSimplifiedPatch (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cc41-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cc41-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc41-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cc41-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7cc41-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cc41-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cc41-108">DESCRIPTION</span></span>
<span data-ttu-id="7cc41-109">**Update – a AzActionRule** parancsmag frissíti a műveleti szabály tulajdonságait – állapot és címkék.</span><span class="sxs-lookup"><span data-stu-id="7cc41-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="7cc41-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7cc41-110">EXAMPLES</span></span>

### <span data-ttu-id="7cc41-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7cc41-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="7cc41-112">Ez a parancsmag letiltja a műveleti szabályt.</span><span class="sxs-lookup"><span data-stu-id="7cc41-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="7cc41-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cc41-113">PARAMETERS</span></span>

### <span data-ttu-id="7cc41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc41-114">-DefaultProfile</span></span>
<span data-ttu-id="7cc41-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cc41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cc41-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cc41-116">-InputObject</span></span>
<span data-ttu-id="7cc41-117">A műveleti szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="7cc41-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc41-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cc41-118">-Name</span></span>
<span data-ttu-id="7cc41-119">Műveleti szabály neve</span><span class="sxs-lookup"><span data-stu-id="7cc41-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc41-120">-ResourceGroupName</span></span>
<span data-ttu-id="7cc41-121">Műveleti szabály neve</span><span class="sxs-lookup"><span data-stu-id="7cc41-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc41-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc41-122">-ResourceId</span></span>
<span data-ttu-id="7cc41-123">A műveleti szabály erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7cc41-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc41-124">-Állapot</span><span class="sxs-lookup"><span data-stu-id="7cc41-124">-Status</span></span>
<span data-ttu-id="7cc41-125">Műveleti szabály állapota</span><span class="sxs-lookup"><span data-stu-id="7cc41-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc41-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="7cc41-126">-Tag</span></span>
<span data-ttu-id="7cc41-127">A műveleti szabály címkéi</span><span class="sxs-lookup"><span data-stu-id="7cc41-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc41-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cc41-128">-Confirm</span></span>
<span data-ttu-id="7cc41-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cc41-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cc41-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cc41-130">-WhatIf</span></span>
<span data-ttu-id="7cc41-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cc41-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cc41-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cc41-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cc41-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc41-133">CommonParameters</span></span>
<span data-ttu-id="7cc41-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cc41-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc41-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7cc41-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc41-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cc41-136">INPUTS</span></span>

### <span data-ttu-id="7cc41-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc41-137">System.String</span></span>

### <span data-ttu-id="7cc41-138">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="7cc41-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="7cc41-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cc41-139">OUTPUTS</span></span>

### <span data-ttu-id="7cc41-140">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="7cc41-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="7cc41-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cc41-141">NOTES</span></span>

## <span data-ttu-id="7cc41-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cc41-142">RELATED LINKS</span></span>
