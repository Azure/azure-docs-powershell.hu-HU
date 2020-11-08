---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: c89938b677809fbdd8679411e0d6108d407afc6a
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017277"
---
# <span data-ttu-id="2cc07-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2cc07-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="2cc07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cc07-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc07-103">A munkaterülethez kapcsolt felügyeleti csoportok részletes adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2cc07-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="2cc07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cc07-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc07-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cc07-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc07-106">A **Get-AzOperationalInsightsWorkspaceManagementGroup** parancsmag a munkaterülethez kapcsolt felügyeleti csoportokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="2cc07-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="2cc07-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2cc07-107">EXAMPLES</span></span>

### <span data-ttu-id="2cc07-108">1. példa: felügyeleti csoportok beolvasása munkaterület szerint</span><span class="sxs-lookup"><span data-stu-id="2cc07-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="2cc07-109">Ez a parancs a MyWorkspace nevű munkaterület felügyeleti csoportját kapja meg az ContosoResourceGroup nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="2cc07-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2cc07-110">2. példa: felügyeleti csoportok beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="2cc07-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="2cc07-111">Ez a parancs a Get-AzOperationalInsightsWorkspace parancsmagot használja a MyWorkspace nevű munkaterület beolvasásához, majd átadja a munkaterületet az aktuális parancsmagnak, amely az adott munkaterület kezelési csoportját kapja.</span><span class="sxs-lookup"><span data-stu-id="2cc07-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="2cc07-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cc07-112">PARAMETERS</span></span>

### <span data-ttu-id="2cc07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc07-113">-DefaultProfile</span></span>
<span data-ttu-id="2cc07-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2cc07-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cc07-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2cc07-115">-Name</span></span>
<span data-ttu-id="2cc07-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cc07-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2cc07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc07-117">-ResourceGroupName</span></span>
<span data-ttu-id="2cc07-118">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cc07-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="2cc07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc07-119">CommonParameters</span></span>
<span data-ttu-id="2cc07-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cc07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc07-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc07-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc07-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cc07-122">INPUTS</span></span>

### <span data-ttu-id="2cc07-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2cc07-123">System.String</span></span>

## <span data-ttu-id="2cc07-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cc07-124">OUTPUTS</span></span>

### <span data-ttu-id="2cc07-125">Microsoft. Azure. Command. OperationalInsights. models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2cc07-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="2cc07-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cc07-126">NOTES</span></span>

## <span data-ttu-id="2cc07-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cc07-127">RELATED LINKS</span></span>

[<span data-ttu-id="2cc07-128">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2cc07-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="2cc07-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2cc07-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


