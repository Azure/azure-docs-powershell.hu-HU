---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479113"
---
# <span data-ttu-id="591e6-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="591e6-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="591e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591e6-102">SYNOPSIS</span></span>
<span data-ttu-id="591e6-103">Műveletszabály törlése</span><span class="sxs-lookup"><span data-stu-id="591e6-103">Deletes a action rule</span></span>

## <span data-ttu-id="591e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="591e6-104">SYNTAX</span></span>

### <span data-ttu-id="591e6-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="591e6-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591e6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="591e6-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591e6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="591e6-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591e6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="591e6-108">DESCRIPTION</span></span>
<span data-ttu-id="591e6-109">**Remove-AzActionRule** parancsmag törli a műveletszabályt.</span><span class="sxs-lookup"><span data-stu-id="591e6-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="591e6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="591e6-110">EXAMPLES</span></span>

### <span data-ttu-id="591e6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="591e6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="591e6-112">Ez a parancsmag törli az ActionRuleName nevű műveletszabályt az erőforráscsoport teszt-rg</span><span class="sxs-lookup"><span data-stu-id="591e6-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="591e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591e6-113">PARAMETERS</span></span>

### <span data-ttu-id="591e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591e6-114">-DefaultProfile</span></span>
<span data-ttu-id="591e6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="591e6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="591e6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="591e6-116">-InputObject</span></span>
<span data-ttu-id="591e6-117">A műveletszabály-erőforrás</span><span class="sxs-lookup"><span data-stu-id="591e6-117">The action rule resource</span></span>

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

### <span data-ttu-id="591e6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="591e6-118">-Name</span></span>
<span data-ttu-id="591e6-119">A műveletszabály neve</span><span class="sxs-lookup"><span data-stu-id="591e6-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591e6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="591e6-120">-PassThru</span></span>
<span data-ttu-id="591e6-121">A PassThru egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="591e6-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="591e6-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="591e6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="591e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="591e6-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="591e6-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591e6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="591e6-125">-ResourceId</span></span>
<span data-ttu-id="591e6-126">A Műveletszabály lekérte erőforrás-azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="591e6-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591e6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="591e6-127">-Confirm</span></span>
<span data-ttu-id="591e6-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="591e6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591e6-129">-WhatIf</span></span>
<span data-ttu-id="591e6-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="591e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591e6-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="591e6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591e6-132">CommonParameters</span></span>
<span data-ttu-id="591e6-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591e6-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="591e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591e6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="591e6-135">INPUTS</span></span>

### <span data-ttu-id="591e6-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="591e6-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="591e6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="591e6-137">OUTPUTS</span></span>

### <span data-ttu-id="591e6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="591e6-138">System.Boolean</span></span>

## <span data-ttu-id="591e6-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="591e6-139">NOTES</span></span>

## <span data-ttu-id="591e6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="591e6-140">RELATED LINKS</span></span>
