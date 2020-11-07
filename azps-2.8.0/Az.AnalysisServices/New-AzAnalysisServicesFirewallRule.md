---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 7fb766bfa65d37fd8491e93593b3ea423938fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668165"
---
# <span data-ttu-id="09f21-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="09f21-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="09f21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09f21-102">SYNOPSIS</span></span>
<span data-ttu-id="09f21-103">Új Analysis Services-tűzfalszabályok létrehozása</span><span class="sxs-lookup"><span data-stu-id="09f21-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="09f21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09f21-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f21-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09f21-105">DESCRIPTION</span></span>
<span data-ttu-id="09f21-106">A New-AzAnalysisServicesFirewallRule új tűzfalszabály-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="09f21-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="09f21-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09f21-107">EXAMPLES</span></span>

### <span data-ttu-id="09f21-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09f21-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="09f21-109">A Szabály1 nevű tűzfalszabályok létrehozása a 0.0.0.0 és a záró tartománnyal 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="09f21-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="09f21-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09f21-110">PARAMETERS</span></span>

### <span data-ttu-id="09f21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f21-111">-DefaultProfile</span></span>
<span data-ttu-id="09f21-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09f21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f21-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="09f21-113">-FirewallRuleName</span></span>
<span data-ttu-id="09f21-114">Tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="09f21-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="09f21-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="09f21-115">-RangeEnd</span></span>
<span data-ttu-id="09f21-116">A tűzfalszabály végpontja</span><span class="sxs-lookup"><span data-stu-id="09f21-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f21-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="09f21-117">-RangeStart</span></span>
<span data-ttu-id="09f21-118">A tűzfalszabályok kezdési köre</span><span class="sxs-lookup"><span data-stu-id="09f21-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="09f21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f21-119">CommonParameters</span></span>
<span data-ttu-id="09f21-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09f21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f21-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f21-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f21-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09f21-122">INPUTS</span></span>

### <span data-ttu-id="09f21-123">System. String</span><span class="sxs-lookup"><span data-stu-id="09f21-123">System.String</span></span>

## <span data-ttu-id="09f21-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09f21-124">OUTPUTS</span></span>

### <span data-ttu-id="09f21-125">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="09f21-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="09f21-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09f21-126">NOTES</span></span>

## <span data-ttu-id="09f21-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09f21-127">RELATED LINKS</span></span>

[<span data-ttu-id="09f21-128">Új – AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="09f21-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)