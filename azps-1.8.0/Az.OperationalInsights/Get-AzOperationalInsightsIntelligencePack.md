---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: fa4df1d2b2149a0bc9c637ffefd5c60e52fa0059
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671948"
---
# <span data-ttu-id="7f19d-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="7f19d-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="7f19d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f19d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f19d-103">A rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7f19d-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="7f19d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f19d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f19d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f19d-105">DESCRIPTION</span></span>
<span data-ttu-id="7f19d-106">A **Get-AzOperationalInsightsIntelligencePack** parancsmag az elérhető intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7f19d-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="7f19d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7f19d-107">EXAMPLES</span></span>

### <span data-ttu-id="7f19d-108">1. példa: intelligencia-csomagok beolvasása</span><span class="sxs-lookup"><span data-stu-id="7f19d-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7f19d-109">Ez a parancs a rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7f19d-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="7f19d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f19d-110">PARAMETERS</span></span>

### <span data-ttu-id="7f19d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f19d-111">-DefaultProfile</span></span>
<span data-ttu-id="7f19d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f19d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f19d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f19d-113">-ResourceGroupName</span></span>
<span data-ttu-id="7f19d-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7f19d-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="7f19d-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f19d-115">-WorkspaceName</span></span>
<span data-ttu-id="7f19d-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f19d-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="7f19d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f19d-117">CommonParameters</span></span>
<span data-ttu-id="7f19d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f19d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f19d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f19d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f19d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f19d-120">INPUTS</span></span>

### <span data-ttu-id="7f19d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7f19d-121">System.String</span></span>

## <span data-ttu-id="7f19d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f19d-122">OUTPUTS</span></span>

### <span data-ttu-id="7f19d-123">Microsoft. Azure. Command. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="7f19d-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="7f19d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f19d-124">NOTES</span></span>

## <span data-ttu-id="7f19d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f19d-125">RELATED LINKS</span></span>

[<span data-ttu-id="7f19d-126">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="7f19d-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


