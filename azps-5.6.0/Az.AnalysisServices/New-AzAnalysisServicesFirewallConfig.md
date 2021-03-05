---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: bd958c9157a5e47b1fc4a878c9ce72405490ec2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004998"
---
# <span data-ttu-id="9954c-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="9954c-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="9954c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9954c-102">SYNOPSIS</span></span>
<span data-ttu-id="9954c-103">Létrehoz egy új Analysis Services tűzfal-konfigurációt</span><span class="sxs-lookup"><span data-stu-id="9954c-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="9954c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9954c-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9954c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9954c-105">DESCRIPTION</span></span>
<span data-ttu-id="9954c-106">A New-AzAnalysisServicesFirewallConfig létrehoz egy új tűzfal konfigurációs objektumot</span><span class="sxs-lookup"><span data-stu-id="9954c-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="9954c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9954c-107">EXAMPLES</span></span>

### <span data-ttu-id="9954c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9954c-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="9954c-109">Létrehoz egy tűzfal konfigurációs objektumát két sszabályokkal, miközben engedélyezi a hozzáférést a Power BI szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="9954c-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="9954c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9954c-110">PARAMETERS</span></span>

### <span data-ttu-id="9954c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9954c-111">-DefaultProfile</span></span>
<span data-ttu-id="9954c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9954c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9954c-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="9954c-113">-EnablePowerBIService</span></span>
<span data-ttu-id="9954c-114">Egy jelző, amely jelzi, hogy a tűzfal engedélyezi-e a hozzáférést a Power BI-ból</span><span class="sxs-lookup"><span data-stu-id="9954c-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9954c-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="9954c-115">-FirewallRule</span></span>
<span data-ttu-id="9954c-116">Tűzfalszabályok listája</span><span class="sxs-lookup"><span data-stu-id="9954c-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9954c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9954c-117">CommonParameters</span></span>
<span data-ttu-id="9954c-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9954c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9954c-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9954c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9954c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9954c-120">INPUTS</span></span>

### <span data-ttu-id="9954c-121">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9954c-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9954c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9954c-122">OUTPUTS</span></span>

### <span data-ttu-id="9954c-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="9954c-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="9954c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9954c-124">NOTES</span></span>

## <span data-ttu-id="9954c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9954c-125">RELATED LINKS</span></span>

[<span data-ttu-id="9954c-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9954c-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)