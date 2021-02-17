---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205894"
---
# <span data-ttu-id="fc6ca-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="fc6ca-101">Update-AzActionRule</span></span>

## <span data-ttu-id="fc6ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fc6ca-103">Frissíti a műveletszabály tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-103">Updates action rule properties.</span></span>

## <span data-ttu-id="fc6ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc6ca-104">SYNTAX</span></span>

### <span data-ttu-id="fc6ca-105">ByNameSimplifiedPatch (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc6ca-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc6ca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6ca-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc6ca-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc6ca-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc6ca-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc6ca-108">DESCRIPTION</span></span>
<span data-ttu-id="fc6ca-109">**Update-AzActionRule parancsmag** frissíti a műveletszabály tulajdonságait – állapot és címkék.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="fc6ca-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc6ca-110">EXAMPLES</span></span>

### <span data-ttu-id="fc6ca-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fc6ca-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="fc6ca-112">Ez a parancsmag letiltja a műveletszabályt.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="fc6ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc6ca-113">PARAMETERS</span></span>

### <span data-ttu-id="fc6ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc6ca-114">-DefaultProfile</span></span>
<span data-ttu-id="fc6ca-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc6ca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc6ca-116">-InputObject</span></span>
<span data-ttu-id="fc6ca-117">A műveletszabály-erőforrás</span><span class="sxs-lookup"><span data-stu-id="fc6ca-117">The action rule resource</span></span>

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

### <span data-ttu-id="fc6ca-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fc6ca-118">-Name</span></span>
<span data-ttu-id="fc6ca-119">Műveletszabály neve</span><span class="sxs-lookup"><span data-stu-id="fc6ca-119">Action rule name</span></span>

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

### <span data-ttu-id="fc6ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc6ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc6ca-121">Műveletszabály neve</span><span class="sxs-lookup"><span data-stu-id="fc6ca-121">Action rule name</span></span>

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

### <span data-ttu-id="fc6ca-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6ca-122">-ResourceId</span></span>
<span data-ttu-id="fc6ca-123">A műveletszabály erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fc6ca-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="fc6ca-124">-Állapot</span><span class="sxs-lookup"><span data-stu-id="fc6ca-124">-Status</span></span>
<span data-ttu-id="fc6ca-125">Műveletszabály állapota</span><span class="sxs-lookup"><span data-stu-id="fc6ca-125">Action rule status</span></span>

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

### <span data-ttu-id="fc6ca-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc6ca-126">-Tag</span></span>
<span data-ttu-id="fc6ca-127">Műveletszabály címkéi</span><span class="sxs-lookup"><span data-stu-id="fc6ca-127">Action rule tags</span></span>

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

### <span data-ttu-id="fc6ca-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc6ca-128">-Confirm</span></span>
<span data-ttu-id="fc6ca-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc6ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc6ca-130">-WhatIf</span></span>
<span data-ttu-id="fc6ca-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc6ca-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc6ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc6ca-133">CommonParameters</span></span>
<span data-ttu-id="fc6ca-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc6ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc6ca-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc6ca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc6ca-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc6ca-136">INPUTS</span></span>

### <span data-ttu-id="fc6ca-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fc6ca-137">System.String</span></span>

### <span data-ttu-id="fc6ca-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="fc6ca-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="fc6ca-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc6ca-139">OUTPUTS</span></span>

### <span data-ttu-id="fc6ca-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="fc6ca-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="fc6ca-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc6ca-141">NOTES</span></span>

## <span data-ttu-id="fc6ca-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc6ca-142">RELATED LINKS</span></span>
