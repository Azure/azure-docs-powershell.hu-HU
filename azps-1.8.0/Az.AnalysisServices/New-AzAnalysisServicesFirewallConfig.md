---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: f3c84b22a9ea8c913cb520ae913fff89ae9470ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665738"
---
# <span data-ttu-id="7b211-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7b211-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="7b211-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b211-102">SYNOPSIS</span></span>
<span data-ttu-id="7b211-103">Új Analysis Services-tűzfal-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="7b211-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="7b211-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b211-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b211-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b211-105">DESCRIPTION</span></span>
<span data-ttu-id="7b211-106">A New-AzAnalysisServicesFirewallConfig létrehoz egy új tűzfal-konfigurációs objektumot</span><span class="sxs-lookup"><span data-stu-id="7b211-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="7b211-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7b211-107">EXAMPLES</span></span>

### <span data-ttu-id="7b211-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b211-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="7b211-109">Tűzfal-konfigurációs objektum létrehozása két szabállyal, miközben engedélyezi a hozzáférést a Power BI szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="7b211-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="7b211-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b211-110">PARAMETERS</span></span>

### <span data-ttu-id="7b211-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b211-111">-DefaultProfile</span></span>
<span data-ttu-id="7b211-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b211-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b211-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="7b211-113">-EnablePowerBIService</span></span>
<span data-ttu-id="7b211-114">Annak jelzése, hogy a tűzfal engedélyezi-e a hozzáférést a Power BI-ről</span><span class="sxs-lookup"><span data-stu-id="7b211-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="7b211-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7b211-115">-FirewallRule</span></span>
<span data-ttu-id="7b211-116">A tűzfalszabályok listája</span><span class="sxs-lookup"><span data-stu-id="7b211-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="7b211-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b211-117">CommonParameters</span></span>
<span data-ttu-id="7b211-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b211-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b211-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b211-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b211-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b211-120">INPUTS</span></span>

### <span data-ttu-id="7b211-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. parancsmagok. AnalysisServices, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7b211-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7b211-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b211-122">OUTPUTS</span></span>

### <span data-ttu-id="7b211-123">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7b211-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="7b211-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b211-124">NOTES</span></span>

## <span data-ttu-id="7b211-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b211-125">RELATED LINKS</span></span>

[<span data-ttu-id="7b211-126">Új – AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7b211-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)