---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494766"
---
# <span data-ttu-id="3a3c5-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="3a3c5-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="3a3c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3c5-103">A rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="3a3c5-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a3c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a3c5-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a3c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a3c5-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3c5-106">A **Get-AzureRmOperationalInsightsIntelligencePacks** parancsmag az elérhető intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="3a3c5-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="3a3c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a3c5-107">EXAMPLES</span></span>

### <span data-ttu-id="3a3c5-108">1. példa: intelligencia-csomagok beolvasása</span><span class="sxs-lookup"><span data-stu-id="3a3c5-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="3a3c5-109">Ez a parancs a rendelkezésre álló intelligencia csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="3a3c5-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="3a3c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a3c5-110">PARAMETERS</span></span>

### <span data-ttu-id="3a3c5-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3c5-111">-ResourceGroupName</span></span>
<span data-ttu-id="3a3c5-112">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3a3c5-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3a3c5-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a3c5-113">-WorkspaceName</span></span>
<span data-ttu-id="3a3c5-114">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a3c5-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3a3c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3c5-115">-DefaultProfile</span></span>
<span data-ttu-id="3a3c5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a3c5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3c5-117">CommonParameters</span></span>
<span data-ttu-id="3a3c5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a3c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3c5-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a3c5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3c5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a3c5-120">INPUTS</span></span>

## <span data-ttu-id="3a3c5-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a3c5-121">OUTPUTS</span></span>

### <span data-ttu-id="3a3c5-122">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="3a3c5-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="3a3c5-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a3c5-123">NOTES</span></span>

## <span data-ttu-id="3a3c5-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a3c5-124">RELATED LINKS</span></span>

[<span data-ttu-id="3a3c5-125">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3a3c5-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


