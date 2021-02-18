---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206358"
---
# <span data-ttu-id="9c8f1-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="9c8f1-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="9c8f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8f1-103">Munkaterület használati adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="9c8f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c8f1-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c8f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c8f1-105">DESCRIPTION</span></span>
<span data-ttu-id="9c8f1-106">A **Get-AzOperationalInsightsWorkspaceUsage** parancsmag beolvassa a munkaterület használati adatait.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="9c8f1-107">Ez a parancs felfedi, hogy a munkaterület mennyi adatot elemezt egy adott időszakban.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="9c8f1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c8f1-108">EXAMPLES</span></span>

### <span data-ttu-id="9c8f1-109">1. példa: Használati adatok lekérte munkaterület neve alapján</span><span class="sxs-lookup"><span data-stu-id="9c8f1-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="9c8f1-110">Ez a parancs a MyWorkspace nevű munkaterület használati adatait kapja meg a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="9c8f1-111">2. példa: Használati adatok lekérte a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="9c8f1-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="9c8f1-112">Ez a parancs a MyWorkSpace nevű munkaterületet a Get-AzOperationalInsightsWorkspace parancsmag használatával kapja meg, majd átadja a munkaterületet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="9c8f1-113">A parancs a munkaterület használati adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="9c8f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c8f1-114">PARAMETERS</span></span>

### <span data-ttu-id="9c8f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8f1-115">-DefaultProfile</span></span>
<span data-ttu-id="9c8f1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c8f1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c8f1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9c8f1-117">-Name</span></span>
<span data-ttu-id="9c8f1-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="9c8f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c8f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c8f1-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="9c8f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8f1-121">CommonParameters</span></span>
<span data-ttu-id="9c8f1-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8f1-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8f1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8f1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c8f1-124">INPUTS</span></span>

### <span data-ttu-id="9c8f1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9c8f1-125">System.String</span></span>

## <span data-ttu-id="9c8f1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c8f1-126">OUTPUTS</span></span>

### <span data-ttu-id="9c8f1-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="9c8f1-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="9c8f1-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c8f1-128">NOTES</span></span>

## <span data-ttu-id="9c8f1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c8f1-129">RELATED LINKS</span></span>

[<span data-ttu-id="9c8f1-130">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9c8f1-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="9c8f1-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c8f1-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


