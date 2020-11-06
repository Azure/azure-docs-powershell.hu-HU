---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500648"
---
# <span data-ttu-id="453e5-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="453e5-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="453e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="453e5-102">SYNOPSIS</span></span>
<span data-ttu-id="453e5-103">Új Analysis Services-tűzfalszabályok létrehozása</span><span class="sxs-lookup"><span data-stu-id="453e5-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="453e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="453e5-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="453e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="453e5-105">DESCRIPTION</span></span>
<span data-ttu-id="453e5-106">A New-AzureRmAnalysisServicesFirewallRule új tűzfalszabály-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="453e5-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="453e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="453e5-107">EXAMPLES</span></span>

### <span data-ttu-id="453e5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="453e5-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="453e5-109">A Szabály1 nevű tűzfalszabályok létrehozása a 0.0.0.0 és a záró tartománnyal 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="453e5-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="453e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="453e5-110">PARAMETERS</span></span>

### <span data-ttu-id="453e5-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="453e5-111">-FirewallRuleName</span></span>
<span data-ttu-id="453e5-112">Tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="453e5-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453e5-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="453e5-113">-RangeStart</span></span>
<span data-ttu-id="453e5-114">A tűzfalszabályok kezdési köre</span><span class="sxs-lookup"><span data-stu-id="453e5-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453e5-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="453e5-115">-RangeEnd</span></span>
<span data-ttu-id="453e5-116">A tűzfalszabály végpontja</span><span class="sxs-lookup"><span data-stu-id="453e5-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="453e5-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="453e5-117">INPUTS</span></span>

## <span data-ttu-id="453e5-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="453e5-118">OUTPUTS</span></span>

### <span data-ttu-id="453e5-119">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="453e5-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="453e5-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="453e5-120">RELATED LINKS</span></span>

[<span data-ttu-id="453e5-121">Új – AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="453e5-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
