---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 0e63b6926f635a4260e6e3c9d658afa410f29966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494430"
---
# <span data-ttu-id="03be2-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="03be2-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="03be2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03be2-102">SYNOPSIS</span></span>
<span data-ttu-id="03be2-103">A rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="03be2-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03be2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03be2-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03be2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03be2-105">DESCRIPTION</span></span>
<span data-ttu-id="03be2-106">A **Get-AzureRmOperationalInsightsIntelligencePacks** parancsmag az elérhető intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="03be2-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="03be2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03be2-107">EXAMPLES</span></span>

### <span data-ttu-id="03be2-108">1. példa: intelligencia-csomagok beolvasása</span><span class="sxs-lookup"><span data-stu-id="03be2-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="03be2-109">Ez a parancs a rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="03be2-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="03be2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03be2-110">PARAMETERS</span></span>

### <span data-ttu-id="03be2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03be2-111">-DefaultProfile</span></span>
<span data-ttu-id="03be2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="03be2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03be2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03be2-113">-ResourceGroupName</span></span>
<span data-ttu-id="03be2-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="03be2-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03be2-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03be2-115">-WorkspaceName</span></span>
<span data-ttu-id="03be2-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03be2-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03be2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03be2-117">CommonParameters</span></span>
<span data-ttu-id="03be2-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03be2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03be2-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03be2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03be2-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03be2-120">INPUTS</span></span>

### <span data-ttu-id="03be2-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="03be2-121">None</span></span>
<span data-ttu-id="03be2-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="03be2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03be2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03be2-123">OUTPUTS</span></span>

### <span data-ttu-id="03be2-124">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="03be2-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="03be2-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03be2-125">NOTES</span></span>

## <span data-ttu-id="03be2-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03be2-126">RELATED LINKS</span></span>

[<span data-ttu-id="03be2-127">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="03be2-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


