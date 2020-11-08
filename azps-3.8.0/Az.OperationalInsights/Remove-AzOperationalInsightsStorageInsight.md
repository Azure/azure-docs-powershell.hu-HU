---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 3d8c973b56f9623e344b147c2bcea6d03a43ee39
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017288"
---
# <span data-ttu-id="60fac-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="60fac-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="60fac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60fac-102">SYNOPSIS</span></span>
<span data-ttu-id="60fac-103">Eltávolít egy tárterület-betekintést.</span><span class="sxs-lookup"><span data-stu-id="60fac-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="60fac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60fac-104">SYNTAX</span></span>

### <span data-ttu-id="60fac-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60fac-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60fac-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60fac-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60fac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60fac-107">DESCRIPTION</span></span>
<span data-ttu-id="60fac-108">A **Remove-AzOperationalInsightsStorageInsight** parancsmag a tárterület-betekintést törli a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="60fac-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="60fac-109">Példák</span><span class="sxs-lookup"><span data-stu-id="60fac-109">EXAMPLES</span></span>

### <span data-ttu-id="60fac-110">Példa 1: tárterület-betekintés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="60fac-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="60fac-111">Ez a parancs eltávolítja a MyStorageInsight nevű tárterület-betekintést a megadott erőforráscsoport MyWorkspace nevű munkaterületéről.</span><span class="sxs-lookup"><span data-stu-id="60fac-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="60fac-112">A parancs nem adja meg az *erő* paramétert, ezért a tárterület-betekintési elem eltávolítása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60fac-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="60fac-113">2. példa: tárterület-betekintés eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="60fac-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="60fac-114">Az első parancs az Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd a $Workspace változóban tárolja. A második parancs eltávolítja a MyStorageInsight nevű tárterület-betekintést az $Workspaceból, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60fac-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="60fac-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60fac-115">PARAMETERS</span></span>

### <span data-ttu-id="60fac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fac-116">-DefaultProfile</span></span>
<span data-ttu-id="60fac-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="60fac-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60fac-118">-Force</span><span class="sxs-lookup"><span data-stu-id="60fac-118">-Force</span></span>
<span data-ttu-id="60fac-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="60fac-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60fac-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60fac-120">-Name</span></span>
<span data-ttu-id="60fac-121">A tárterület-betekintési terület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60fac-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="60fac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fac-122">-ResourceGroupName</span></span>
<span data-ttu-id="60fac-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60fac-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fac-124">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="60fac-124">-Workspace</span></span>
<span data-ttu-id="60fac-125">A tárterület-betekintést tartalmazó munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="60fac-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60fac-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="60fac-126">-WorkspaceName</span></span>
<span data-ttu-id="60fac-127">A tárterület-betekintést tartalmazó munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60fac-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fac-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60fac-128">-Confirm</span></span>
<span data-ttu-id="60fac-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60fac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60fac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fac-130">-WhatIf</span></span>
<span data-ttu-id="60fac-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60fac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60fac-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60fac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60fac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fac-133">CommonParameters</span></span>
<span data-ttu-id="60fac-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60fac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fac-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fac-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fac-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60fac-136">INPUTS</span></span>

### <span data-ttu-id="60fac-137">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="60fac-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="60fac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60fac-138">System.String</span></span>

## <span data-ttu-id="60fac-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60fac-139">OUTPUTS</span></span>

### <span data-ttu-id="60fac-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="60fac-140">System.Void</span></span>

## <span data-ttu-id="60fac-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60fac-141">NOTES</span></span>

## <span data-ttu-id="60fac-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60fac-142">RELATED LINKS</span></span>

[<span data-ttu-id="60fac-143">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="60fac-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="60fac-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="60fac-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


