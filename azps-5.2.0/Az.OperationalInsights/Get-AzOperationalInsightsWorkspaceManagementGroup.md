---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339977"
---
# <span data-ttu-id="ad6c0-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ad6c0-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="ad6c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6c0-103">A munkaterülethez csatlakoztatott felügyeleti csoportok részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="ad6c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad6c0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad6c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ad6c0-106">A **Get-AzOperationalInsightsWorkspaceManagementGroup** parancsmag felsorolja a munkaterülethez csatlakoztatott felügyeleti csoportokat.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="ad6c0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad6c0-107">EXAMPLES</span></span>

### <span data-ttu-id="ad6c0-108">1. példa: Felügyeleti csoportok lekértése munkaterület neve alapján</span><span class="sxs-lookup"><span data-stu-id="ad6c0-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="ad6c0-109">Ez a parancs a ContosoResourceGroup nevű erőforráscsoport MyWorkspace nevű munkaterületének felügyeleti csoportjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ad6c0-110">2. példa: Felügyeleti csoportok levezetése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="ad6c0-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="ad6c0-111">Ez a parancs a Get-AzOperationalInsightsWorkspace parancsmagot használva szerezze be a MyWorkspace nevű munkaterületet, majd átadja a munkaterületet az aktuális parancsmagnak, amely az adott munkaterület felügyeleti csoportjait kapja.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="ad6c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad6c0-112">PARAMETERS</span></span>

### <span data-ttu-id="ad6c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6c0-113">-DefaultProfile</span></span>
<span data-ttu-id="ad6c0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ad6c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad6c0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ad6c0-115">-Name</span></span>
<span data-ttu-id="ad6c0-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ad6c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad6c0-118">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="ad6c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6c0-119">CommonParameters</span></span>
<span data-ttu-id="ad6c0-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6c0-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6c0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6c0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad6c0-122">INPUTS</span></span>

### <span data-ttu-id="ad6c0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ad6c0-123">System.String</span></span>

## <span data-ttu-id="ad6c0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad6c0-124">OUTPUTS</span></span>

### <span data-ttu-id="ad6c0-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ad6c0-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="ad6c0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad6c0-126">NOTES</span></span>

## <span data-ttu-id="ad6c0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad6c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="ad6c0-128">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ad6c0-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="ad6c0-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ad6c0-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


