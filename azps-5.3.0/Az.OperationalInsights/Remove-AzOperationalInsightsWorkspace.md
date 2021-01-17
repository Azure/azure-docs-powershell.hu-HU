---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466701"
---
# <span data-ttu-id="0dd67-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0dd67-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="0dd67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dd67-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd67-103">Eltávolít egy munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="0dd67-103">Removes a workspace.</span></span>

## <span data-ttu-id="0dd67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0dd67-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd67-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0dd67-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd67-106">A **Remove-AzOperationalInsightsWorkspace** parancsmag töröl egy meglévő munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="0dd67-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="0dd67-107">Ha ezt a munkaterületet a létrehozáskor a *CustomerId* paraméterrel kapcsolta hozzá egy meglévő fiókhoz, az eredeti fiók nem törlődik a Operational Insights portálról.</span><span class="sxs-lookup"><span data-stu-id="0dd67-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="0dd67-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0dd67-108">EXAMPLES</span></span>

### <span data-ttu-id="0dd67-109">1. példa: Munkaterület eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="0dd67-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0dd67-110">Ez a parancs eltávolítja a MyWorkspace nevű munkaterületet a ContosoResourceGroup nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="0dd67-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0dd67-111">2. példa: Munkaterület eltávolítása a folyamat használatával és megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="0dd67-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="0dd67-112">Ez a parancs a Get-AzOperationalInsightsWorkspace-parancsmag segítségével begyűjte a MyWorkspace nevű munkaterületet, majd átadja a **Remove-AzOperationalInsightsWorkspace** parancsmagnak úgy, hogy a folyamatoperációs operátorral eltávolítja azt.</span><span class="sxs-lookup"><span data-stu-id="0dd67-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="0dd67-113">Mivel a *Force* paraméter meg van adva, a parancs nem kéri a munkaterület eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="0dd67-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="0dd67-114">3. példa: A törlés kényszerítése munkaterület (nem állíthatók helyre)</span><span class="sxs-lookup"><span data-stu-id="0dd67-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="0dd67-115">Munkaterület törlésének kényszerítése.</span><span class="sxs-lookup"><span data-stu-id="0dd67-115">Force delete a workspace.</span></span>

## <span data-ttu-id="0dd67-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dd67-116">PARAMETERS</span></span>

### <span data-ttu-id="0dd67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd67-117">-DefaultProfile</span></span>
<span data-ttu-id="0dd67-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0dd67-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dd67-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd67-119">-Force</span></span>
<span data-ttu-id="0dd67-120">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0dd67-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0dd67-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="0dd67-121">-ForceDelete</span></span>
<span data-ttu-id="0dd67-122">A törlési munkaterület kényszerítése</span><span class="sxs-lookup"><span data-stu-id="0dd67-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="0dd67-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0dd67-123">-Name</span></span>
<span data-ttu-id="0dd67-124">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0dd67-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="0dd67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd67-125">-ResourceGroupName</span></span>
<span data-ttu-id="0dd67-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0dd67-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0dd67-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dd67-127">-Confirm</span></span>
<span data-ttu-id="0dd67-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0dd67-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd67-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd67-129">-WhatIf</span></span>
<span data-ttu-id="0dd67-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0dd67-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dd67-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0dd67-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd67-132">CommonParameters</span></span>
<span data-ttu-id="0dd67-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd67-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dd67-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd67-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0dd67-135">INPUTS</span></span>

### <span data-ttu-id="0dd67-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0dd67-136">System.String</span></span>

## <span data-ttu-id="0dd67-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dd67-137">OUTPUTS</span></span>

### <span data-ttu-id="0dd67-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="0dd67-138">System.Void</span></span>

## <span data-ttu-id="0dd67-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0dd67-139">NOTES</span></span>

## <span data-ttu-id="0dd67-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dd67-140">RELATED LINKS</span></span>

[<span data-ttu-id="0dd67-141">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0dd67-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="0dd67-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0dd67-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


