---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187947"
---
# <span data-ttu-id="5a4eb-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="5a4eb-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="5a4eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4eb-103">Műveleti szabály törlése</span><span class="sxs-lookup"><span data-stu-id="5a4eb-103">Deletes a action rule</span></span>

## <span data-ttu-id="5a4eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a4eb-104">SYNTAX</span></span>

### <span data-ttu-id="5a4eb-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a4eb-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4eb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4eb-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4eb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a4eb-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4eb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a4eb-108">DESCRIPTION</span></span>
<span data-ttu-id="5a4eb-109">**Remove-AzActionRule** parancsmag: a műveleti szabály törlése.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="5a4eb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5a4eb-110">EXAMPLES</span></span>

### <span data-ttu-id="5a4eb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a4eb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="5a4eb-112">Ez a parancsmag törli a ActionRuleName nevű műveleti szabályt az erőforráscsoport teszt-RG</span><span class="sxs-lookup"><span data-stu-id="5a4eb-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="5a4eb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a4eb-113">PARAMETERS</span></span>

### <span data-ttu-id="5a4eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4eb-114">-DefaultProfile</span></span>
<span data-ttu-id="5a4eb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a4eb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4eb-116">-InputObject</span></span>
<span data-ttu-id="5a4eb-117">A műveleti szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="5a4eb-117">The action rule resource</span></span>

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

### <span data-ttu-id="5a4eb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a4eb-118">-Name</span></span>
<span data-ttu-id="5a4eb-119">A műveleti szabály neve</span><span class="sxs-lookup"><span data-stu-id="5a4eb-119">Name of action rule</span></span>

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

### <span data-ttu-id="5a4eb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a4eb-120">-PassThru</span></span>
<span data-ttu-id="5a4eb-121">A PassThru egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5a4eb-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a4eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a4eb-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5a4eb-124">Resource Group name</span></span>

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

### <span data-ttu-id="5a4eb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4eb-125">-ResourceId</span></span>
<span data-ttu-id="5a4eb-126">Műveletkérő szabály kérése erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="5a4eb-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="5a4eb-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a4eb-127">-Confirm</span></span>
<span data-ttu-id="5a4eb-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4eb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4eb-129">-WhatIf</span></span>
<span data-ttu-id="5a4eb-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4eb-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a4eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4eb-132">CommonParameters</span></span>
<span data-ttu-id="5a4eb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a4eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4eb-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4eb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a4eb-135">INPUTS</span></span>

### <span data-ttu-id="5a4eb-136">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="5a4eb-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="5a4eb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a4eb-137">OUTPUTS</span></span>

### <span data-ttu-id="5a4eb-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a4eb-138">System.Boolean</span></span>

## <span data-ttu-id="5a4eb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a4eb-139">NOTES</span></span>

## <span data-ttu-id="5a4eb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a4eb-140">RELATED LINKS</span></span>
