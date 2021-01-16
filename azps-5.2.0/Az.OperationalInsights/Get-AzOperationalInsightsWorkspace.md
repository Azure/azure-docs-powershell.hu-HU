---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341297"
---
# <span data-ttu-id="75f63-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="75f63-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="75f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f63-102">SYNOPSIS</span></span>
<span data-ttu-id="75f63-103">Információkat kap egy munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="75f63-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="75f63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75f63-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f63-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75f63-105">DESCRIPTION</span></span>
<span data-ttu-id="75f63-106">A **Get-AzOperationalInsightsWorkspace** parancsmag információt kap egy meglévő munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="75f63-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="75f63-107">Ha megadja a munkaterület nevét, ez a parancsmag információt kap a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="75f63-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="75f63-108">Ha nem ad meg nevet, ez a parancsmag információt kap egy erőforráscsoport összes munkaterületének adatairól.</span><span class="sxs-lookup"><span data-stu-id="75f63-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="75f63-109">Ha nem ad meg nevet és erőforráscsoportot, ez a parancsmag információkat kap az előfizetés összes munkaterületével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="75f63-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="75f63-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75f63-110">EXAMPLES</span></span>

### <span data-ttu-id="75f63-111">1. példa: Munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="75f63-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="75f63-112">Ez a parancs kap egy MyWorkspace nevű munkaterületet a ContosoResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="75f63-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="75f63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f63-113">PARAMETERS</span></span>

### <span data-ttu-id="75f63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f63-114">-DefaultProfile</span></span>
<span data-ttu-id="75f63-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="75f63-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75f63-116">-Name</span><span class="sxs-lookup"><span data-stu-id="75f63-116">-Name</span></span>
<span data-ttu-id="75f63-117">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75f63-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f63-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f63-118">-ResourceGroupName</span></span>
<span data-ttu-id="75f63-119">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75f63-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f63-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f63-120">CommonParameters</span></span>
<span data-ttu-id="75f63-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f63-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f63-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f63-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f63-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75f63-123">INPUTS</span></span>

### <span data-ttu-id="75f63-124">System.String</span><span class="sxs-lookup"><span data-stu-id="75f63-124">System.String</span></span>

## <span data-ttu-id="75f63-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75f63-125">OUTPUTS</span></span>

### <span data-ttu-id="75f63-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="75f63-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="75f63-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75f63-127">NOTES</span></span>

## <span data-ttu-id="75f63-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75f63-128">RELATED LINKS</span></span>

[<span data-ttu-id="75f63-129">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="75f63-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


