---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025128"
---
# <span data-ttu-id="c54f9-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="c54f9-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="c54f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c54f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c54f9-103">A rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="c54f9-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="c54f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c54f9-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c54f9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c54f9-105">DESCRIPTION</span></span>
<span data-ttu-id="c54f9-106">A **Get-AzOperationalInsightsIntelligencePack** parancsmag az elérhető intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="c54f9-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="c54f9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c54f9-107">EXAMPLES</span></span>

### <span data-ttu-id="c54f9-108">1. példa: intelligencia-csomagok beolvasása</span><span class="sxs-lookup"><span data-stu-id="c54f9-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c54f9-109">Ez a parancs a rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="c54f9-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="c54f9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c54f9-110">PARAMETERS</span></span>

### <span data-ttu-id="c54f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54f9-111">-DefaultProfile</span></span>
<span data-ttu-id="c54f9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c54f9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c54f9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54f9-113">-ResourceGroupName</span></span>
<span data-ttu-id="c54f9-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c54f9-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c54f9-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c54f9-115">-WorkspaceName</span></span>
<span data-ttu-id="c54f9-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c54f9-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c54f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54f9-117">CommonParameters</span></span>
<span data-ttu-id="c54f9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c54f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54f9-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c54f9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54f9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c54f9-120">INPUTS</span></span>

### <span data-ttu-id="c54f9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c54f9-121">System.String</span></span>

## <span data-ttu-id="c54f9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c54f9-122">OUTPUTS</span></span>

### <span data-ttu-id="c54f9-123">Microsoft. Azure. Command. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="c54f9-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="c54f9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c54f9-124">NOTES</span></span>

## <span data-ttu-id="c54f9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c54f9-125">RELATED LINKS</span></span>

[<span data-ttu-id="c54f9-126">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c54f9-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


