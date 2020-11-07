---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 05bcd77a732be66c426f456f6058e74107b6eb8d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671934"
---
# <span data-ttu-id="4d195-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d195-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="4d195-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d195-102">SYNOPSIS</span></span>
<span data-ttu-id="4d195-103">Információkat kap a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="4d195-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="4d195-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d195-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d195-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d195-105">DESCRIPTION</span></span>
<span data-ttu-id="4d195-106">A **Get-AzOperationalInsightsWorkspace** parancsmag információkat kap egy meglévő munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="4d195-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="4d195-107">Ha a munkaterület nevét adja meg, ez a parancsmag információkat kap a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="4d195-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="4d195-108">Ha nem ad meg nevet, ez a parancsmag információkat kap az erőforráscsoport minden munkaterületéről.</span><span class="sxs-lookup"><span data-stu-id="4d195-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="4d195-109">Ha nem ad meg nevet és erőforráscsoportot, ez a parancsmag információt kap az előfizetésben szereplő összes munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="4d195-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="4d195-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4d195-110">EXAMPLES</span></span>

### <span data-ttu-id="4d195-111">Példa 1: munkaterület beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="4d195-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="4d195-112">Ez a parancs a MyWorkspace nevű munkaterületet kapja a ContosoResourceGroup nevű erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="4d195-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="4d195-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d195-113">PARAMETERS</span></span>

### <span data-ttu-id="4d195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d195-114">-DefaultProfile</span></span>
<span data-ttu-id="4d195-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4d195-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d195-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d195-116">-Name</span></span>
<span data-ttu-id="4d195-117">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d195-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4d195-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d195-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d195-119">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d195-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="4d195-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d195-120">CommonParameters</span></span>
<span data-ttu-id="4d195-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d195-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d195-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d195-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d195-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d195-123">INPUTS</span></span>

### <span data-ttu-id="4d195-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4d195-124">System.String</span></span>

## <span data-ttu-id="4d195-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d195-125">OUTPUTS</span></span>

### <span data-ttu-id="4d195-126">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d195-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="4d195-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d195-127">NOTES</span></span>

## <span data-ttu-id="4d195-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d195-128">RELATED LINKS</span></span>

[<span data-ttu-id="4d195-129">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4d195-129">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


