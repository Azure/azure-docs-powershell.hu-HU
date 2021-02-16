---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149635"
---
# <span data-ttu-id="f37c9-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f37c9-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f37c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f37c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f37c9-103">Új Analysis Services tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="f37c9-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="f37c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f37c9-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f37c9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f37c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f37c9-106">A New-AzAnalysisServicesFirewallRule létrehoz egy új tűzfalszabály-objektumot.</span><span class="sxs-lookup"><span data-stu-id="f37c9-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="f37c9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f37c9-107">EXAMPLES</span></span>

### <span data-ttu-id="f37c9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f37c9-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="f37c9-109">Létrehoz egy szabály1 nevű tűzfalszabályt a 0.0.0.0 kezdőtartomány és a 255.255.255.255.255 kezdőtartománysal</span><span class="sxs-lookup"><span data-stu-id="f37c9-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="f37c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f37c9-110">PARAMETERS</span></span>

### <span data-ttu-id="f37c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37c9-111">-DefaultProfile</span></span>
<span data-ttu-id="f37c9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f37c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f37c9-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f37c9-113">-FirewallRuleName</span></span>
<span data-ttu-id="f37c9-114">A tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="f37c9-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="f37c9-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="f37c9-115">-RangeEnd</span></span>
<span data-ttu-id="f37c9-116">A tűzfalszabály tartományának vége</span><span class="sxs-lookup"><span data-stu-id="f37c9-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="f37c9-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="f37c9-117">-RangeStart</span></span>
<span data-ttu-id="f37c9-118">A tűzfalszabály kezdete</span><span class="sxs-lookup"><span data-stu-id="f37c9-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="f37c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37c9-119">CommonParameters</span></span>
<span data-ttu-id="f37c9-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f37c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37c9-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f37c9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37c9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f37c9-122">INPUTS</span></span>

### <span data-ttu-id="f37c9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f37c9-123">System.String</span></span>

## <span data-ttu-id="f37c9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f37c9-124">OUTPUTS</span></span>

### <span data-ttu-id="f37c9-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f37c9-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f37c9-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f37c9-126">NOTES</span></span>

## <span data-ttu-id="f37c9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f37c9-127">RELATED LINKS</span></span>

[<span data-ttu-id="f37c9-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f37c9-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)