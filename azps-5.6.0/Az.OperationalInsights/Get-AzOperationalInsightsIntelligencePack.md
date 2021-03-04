---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a56fd0303e6f610468c9f2784396023fd20edef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925426"
---
# <span data-ttu-id="5bffe-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="5bffe-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="5bffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bffe-102">SYNOPSIS</span></span>
<span data-ttu-id="5bffe-103">A rendelkezésre álló intelligensintelligencia-csomagok.</span><span class="sxs-lookup"><span data-stu-id="5bffe-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="5bffe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bffe-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bffe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bffe-105">DESCRIPTION</span></span>
<span data-ttu-id="5bffe-106">A **Get-AzOperationalInsightsIntelligencePack** parancsmag megkapja a rendelkezésre álló intelligenciacsomagokat.</span><span class="sxs-lookup"><span data-stu-id="5bffe-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="5bffe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bffe-107">EXAMPLES</span></span>

### <span data-ttu-id="5bffe-108">1. példa: Intelligens csomagok lekérte</span><span class="sxs-lookup"><span data-stu-id="5bffe-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="5bffe-109">Ez a parancs a rendelkezésre álló intelligensintelligencia-csomagokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5bffe-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="5bffe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bffe-110">PARAMETERS</span></span>

### <span data-ttu-id="5bffe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bffe-111">-DefaultProfile</span></span>
<span data-ttu-id="5bffe-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5bffe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bffe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bffe-113">-ResourceGroupName</span></span>
<span data-ttu-id="5bffe-114">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bffe-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="5bffe-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5bffe-115">-WorkspaceName</span></span>
<span data-ttu-id="5bffe-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bffe-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bffe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bffe-117">CommonParameters</span></span>
<span data-ttu-id="5bffe-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bffe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bffe-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bffe-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bffe-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bffe-120">INPUTS</span></span>

### <span data-ttu-id="5bffe-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5bffe-121">System.String</span></span>

## <span data-ttu-id="5bffe-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bffe-122">OUTPUTS</span></span>

### <span data-ttu-id="5bffe-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="5bffe-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="5bffe-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bffe-124">NOTES</span></span>

## <span data-ttu-id="5bffe-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bffe-125">RELATED LINKS</span></span>

[<span data-ttu-id="5bffe-126">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5bffe-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


