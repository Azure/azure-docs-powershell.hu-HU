---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 726386fb4a455b3daab314e5f61d33122592dcf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495812"
---
# <span data-ttu-id="871d8-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="871d8-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="871d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="871d8-102">SYNOPSIS</span></span>
<span data-ttu-id="871d8-103">Eltávolít egy tárterület-betekintést.</span><span class="sxs-lookup"><span data-stu-id="871d8-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="871d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="871d8-104">SYNTAX</span></span>

### <span data-ttu-id="871d8-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="871d8-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="871d8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="871d8-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="871d8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="871d8-107">DESCRIPTION</span></span>
<span data-ttu-id="871d8-108">A **Remove-AzureRmOperationalInsightsStorageInsight** parancsmag a tárterület-betekintést törli a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="871d8-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="871d8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="871d8-109">EXAMPLES</span></span>

### <span data-ttu-id="871d8-110">Példa 1: tárterület-betekintés eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="871d8-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="871d8-111">Ez a parancs eltávolítja a MyStorageInsight nevű tárterület-betekintést a megadott erőforráscsoport MyWorkspace nevű munkaterületéről.</span><span class="sxs-lookup"><span data-stu-id="871d8-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="871d8-112">A parancs nem adja meg az *erő* paramétert, ezért a tárterület-betekintési elem eltávolítása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="871d8-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="871d8-113">2. példa: tárterület-betekintés eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="871d8-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="871d8-114">Az első parancs az Get-AzureRmOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd a $Workspace változóban tárolja. A második parancs eltávolítja a MyStorageInsight nevű tárterület-betekintést az $Workspaceból, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="871d8-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="871d8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="871d8-115">PARAMETERS</span></span>

### <span data-ttu-id="871d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871d8-116">-DefaultProfile</span></span>
<span data-ttu-id="871d8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="871d8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871d8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="871d8-118">-Force</span></span>
<span data-ttu-id="871d8-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="871d8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="871d8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="871d8-120">-Name</span></span>
<span data-ttu-id="871d8-121">A tárterület-betekintési terület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="871d8-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="871d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="871d8-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="871d8-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="871d8-124">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="871d8-124">-Workspace</span></span>
<span data-ttu-id="871d8-125">A tárterület-betekintést tartalmazó munkaterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="871d8-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="871d8-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="871d8-126">-WorkspaceName</span></span>
<span data-ttu-id="871d8-127">A tárterület-betekintést tartalmazó munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="871d8-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="871d8-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="871d8-128">-Confirm</span></span>
<span data-ttu-id="871d8-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="871d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="871d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="871d8-130">-WhatIf</span></span>
<span data-ttu-id="871d8-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="871d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="871d8-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="871d8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="871d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871d8-133">CommonParameters</span></span>
<span data-ttu-id="871d8-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="871d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871d8-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871d8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871d8-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="871d8-136">INPUTS</span></span>

### <span data-ttu-id="871d8-137">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="871d8-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="871d8-138">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="871d8-138">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="871d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="871d8-139">System.String</span></span>

## <span data-ttu-id="871d8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="871d8-140">OUTPUTS</span></span>

### <span data-ttu-id="871d8-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="871d8-141">System.Void</span></span>

## <span data-ttu-id="871d8-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="871d8-142">NOTES</span></span>

## <span data-ttu-id="871d8-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="871d8-143">RELATED LINKS</span></span>

[<span data-ttu-id="871d8-144">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="871d8-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="871d8-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="871d8-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


