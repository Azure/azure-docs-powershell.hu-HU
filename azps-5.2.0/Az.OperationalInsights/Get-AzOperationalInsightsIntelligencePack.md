---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370283"
---
# <span data-ttu-id="ca561-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ca561-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="ca561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca561-102">SYNOPSIS</span></span>
<span data-ttu-id="ca561-103">A rendelkezésre álló intelligensintelligencia-csomagok.</span><span class="sxs-lookup"><span data-stu-id="ca561-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="ca561-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca561-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca561-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca561-105">DESCRIPTION</span></span>
<span data-ttu-id="ca561-106">A **Get-AzOperationalInsightsIntelligencePack** parancsmag megkapja a rendelkezésre álló intelligenciacsomagokat.</span><span class="sxs-lookup"><span data-stu-id="ca561-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="ca561-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca561-107">EXAMPLES</span></span>

### <span data-ttu-id="ca561-108">1. példa: Intelligens csomagok lekérte</span><span class="sxs-lookup"><span data-stu-id="ca561-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ca561-109">Ez a parancs a rendelkezésre álló intelligensintelligencia-csomagokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ca561-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="ca561-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca561-110">PARAMETERS</span></span>

### <span data-ttu-id="ca561-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca561-111">-DefaultProfile</span></span>
<span data-ttu-id="ca561-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ca561-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca561-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca561-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca561-114">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca561-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ca561-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ca561-115">-WorkspaceName</span></span>
<span data-ttu-id="ca561-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca561-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ca561-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca561-117">CommonParameters</span></span>
<span data-ttu-id="ca561-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca561-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca561-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca561-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca561-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca561-120">INPUTS</span></span>

### <span data-ttu-id="ca561-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ca561-121">System.String</span></span>

## <span data-ttu-id="ca561-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca561-122">OUTPUTS</span></span>

### <span data-ttu-id="ca561-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ca561-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="ca561-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca561-124">NOTES</span></span>

## <span data-ttu-id="ca561-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca561-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca561-126">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ca561-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


