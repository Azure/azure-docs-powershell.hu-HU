---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342030"
---
# <span data-ttu-id="d0603-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d0603-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="d0603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0603-102">SYNOPSIS</span></span>
<span data-ttu-id="d0603-103">Eltávolítja a Tárterület-betekintőt.</span><span class="sxs-lookup"><span data-stu-id="d0603-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="d0603-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0603-104">SYNTAX</span></span>

### <span data-ttu-id="d0603-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0603-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0603-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d0603-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0603-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0603-107">DESCRIPTION</span></span>
<span data-ttu-id="d0603-108">A **Remove-AzOperationalInsightsStorageInsight** parancsmag törli a tárterület-betekintéseket a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d0603-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="d0603-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0603-109">EXAMPLES</span></span>

### <span data-ttu-id="d0603-110">1. példa: Tárterület-betekintés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="d0603-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="d0603-111">Ez a parancs eltávolítja a MyStorageInsight nevű tárterület-betekintőt a MyWorkspace nevű munkaterületről a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d0603-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="d0603-112">A parancs nem adja meg az *Kényszerítés* paramétert, ezért a Storage Insight eltávolítása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0603-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="d0603-113">2. példa: Tárterület-betekintés eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="d0603-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="d0603-114">Az első parancs a Get-AzOperationalInsightsWorkspace parancsmagot használva szerezze be a MyWorkspace nevű munkaterületet, majd tárolja azt a $Workspace változóban. A második parancs anélkül távolítja el a MyStorageInsight nevű tárterület-$Workspace hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0603-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="d0603-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0603-115">PARAMETERS</span></span>

### <span data-ttu-id="d0603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0603-116">-DefaultProfile</span></span>
<span data-ttu-id="d0603-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d0603-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0603-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d0603-118">-Force</span></span>
<span data-ttu-id="d0603-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="d0603-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0603-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d0603-120">-Name</span></span>
<span data-ttu-id="d0603-121">A Tárterület-elemzés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0603-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="d0603-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0603-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0603-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0603-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="d0603-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d0603-124">-Workspace</span></span>
<span data-ttu-id="d0603-125">A Tárterület-betekintőt tartalmazó munkaterület.</span><span class="sxs-lookup"><span data-stu-id="d0603-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="d0603-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0603-126">-WorkspaceName</span></span>
<span data-ttu-id="d0603-127">A Tárterület-betekintőt tartalmazó munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d0603-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="d0603-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0603-128">-Confirm</span></span>
<span data-ttu-id="d0603-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0603-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0603-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0603-130">-WhatIf</span></span>
<span data-ttu-id="d0603-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0603-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0603-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0603-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0603-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0603-133">CommonParameters</span></span>
<span data-ttu-id="d0603-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0603-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0603-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0603-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0603-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0603-136">INPUTS</span></span>

### <span data-ttu-id="d0603-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0603-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d0603-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d0603-138">System.String</span></span>

## <span data-ttu-id="d0603-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0603-139">OUTPUTS</span></span>

### <span data-ttu-id="d0603-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="d0603-140">System.Void</span></span>

## <span data-ttu-id="d0603-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0603-141">NOTES</span></span>

## <span data-ttu-id="d0603-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0603-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0603-143">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d0603-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="d0603-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0603-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


