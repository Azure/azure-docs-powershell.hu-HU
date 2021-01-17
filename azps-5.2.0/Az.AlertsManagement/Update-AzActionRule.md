---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327399"
---
# <span data-ttu-id="905a4-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="905a4-101">Update-AzActionRule</span></span>

## <span data-ttu-id="905a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905a4-102">SYNOPSIS</span></span>
<span data-ttu-id="905a4-103">Frissíti a műveletszabály tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="905a4-103">Updates action rule properties.</span></span>

## <span data-ttu-id="905a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="905a4-104">SYNTAX</span></span>

### <span data-ttu-id="905a4-105">ByNameSimplifiedPatch (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="905a4-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="905a4-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="905a4-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="905a4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="905a4-108">DESCRIPTION</span></span>
<span data-ttu-id="905a4-109">**Update-AzActionRule parancsmag** frissíti a műveletszabály tulajdonságait – állapot és címkék.</span><span class="sxs-lookup"><span data-stu-id="905a4-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="905a4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="905a4-110">EXAMPLES</span></span>

### <span data-ttu-id="905a4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="905a4-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="905a4-112">Ez a parancsmag letiltja a műveletszabályt.</span><span class="sxs-lookup"><span data-stu-id="905a4-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="905a4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="905a4-113">PARAMETERS</span></span>

### <span data-ttu-id="905a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905a4-114">-DefaultProfile</span></span>
<span data-ttu-id="905a4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="905a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905a4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="905a4-116">-InputObject</span></span>
<span data-ttu-id="905a4-117">A műveletszabály-erőforrás</span><span class="sxs-lookup"><span data-stu-id="905a4-117">The action rule resource</span></span>

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

### <span data-ttu-id="905a4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="905a4-118">-Name</span></span>
<span data-ttu-id="905a4-119">Műveletszabály neve</span><span class="sxs-lookup"><span data-stu-id="905a4-119">Action rule name</span></span>

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

### <span data-ttu-id="905a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905a4-120">-ResourceGroupName</span></span>
<span data-ttu-id="905a4-121">Műveletszabály neve</span><span class="sxs-lookup"><span data-stu-id="905a4-121">Action rule name</span></span>

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

### <span data-ttu-id="905a4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="905a4-122">-ResourceId</span></span>
<span data-ttu-id="905a4-123">A műveletszabály erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="905a4-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="905a4-124">-Állapot</span><span class="sxs-lookup"><span data-stu-id="905a4-124">-Status</span></span>
<span data-ttu-id="905a4-125">Műveletszabály állapota</span><span class="sxs-lookup"><span data-stu-id="905a4-125">Action rule status</span></span>

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

### <span data-ttu-id="905a4-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="905a4-126">-Tag</span></span>
<span data-ttu-id="905a4-127">Műveletszabály címkéi</span><span class="sxs-lookup"><span data-stu-id="905a4-127">Action rule tags</span></span>

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

### <span data-ttu-id="905a4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="905a4-128">-Confirm</span></span>
<span data-ttu-id="905a4-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="905a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="905a4-130">-WhatIf</span></span>
<span data-ttu-id="905a4-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="905a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="905a4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="905a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="905a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905a4-133">CommonParameters</span></span>
<span data-ttu-id="905a4-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905a4-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="905a4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905a4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="905a4-136">INPUTS</span></span>

### <span data-ttu-id="905a4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="905a4-137">System.String</span></span>

### <span data-ttu-id="905a4-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="905a4-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="905a4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="905a4-139">OUTPUTS</span></span>

### <span data-ttu-id="905a4-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="905a4-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="905a4-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="905a4-141">NOTES</span></span>

## <span data-ttu-id="905a4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="905a4-142">RELATED LINKS</span></span>
