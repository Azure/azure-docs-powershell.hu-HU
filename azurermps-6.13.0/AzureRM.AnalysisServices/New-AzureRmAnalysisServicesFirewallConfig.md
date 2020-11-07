---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672500"
---
# <span data-ttu-id="7f3ae-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7f3ae-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="7f3ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3ae-103">Új Analysis Services-tűzfal-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="7f3ae-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f3ae-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3ae-106">A New-AzureRmAnalysisServicesFirewallConfig létrehoz egy új tűzfal-konfigurációs objektumot</span><span class="sxs-lookup"><span data-stu-id="7f3ae-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="7f3ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7f3ae-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3ae-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f3ae-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="7f3ae-109">Tűzfal-konfigurációs objektum létrehozása két szabállyal, miközben engedélyezi a hozzáférést a Power BI szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="7f3ae-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="7f3ae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f3ae-110">PARAMETERS</span></span>

### <span data-ttu-id="7f3ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3ae-111">-DefaultProfile</span></span>
<span data-ttu-id="7f3ae-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f3ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3ae-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="7f3ae-113">-EnablePowerBIService</span></span>
<span data-ttu-id="7f3ae-114">Annak jelzése, hogy a tűzfal engedélyezi-e a hozzáférést a Power BI-ről</span><span class="sxs-lookup"><span data-stu-id="7f3ae-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="7f3ae-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7f3ae-115">-FirewallRule</span></span>
<span data-ttu-id="7f3ae-116">A tűzfalszabályok listája</span><span class="sxs-lookup"><span data-stu-id="7f3ae-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="7f3ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3ae-117">CommonParameters</span></span>
<span data-ttu-id="7f3ae-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f3ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3ae-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3ae-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3ae-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3ae-120">INPUTS</span></span>

### <span data-ttu-id="7f3ae-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. commands. AnalysisServices, Version = 0.6.11.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7f3ae-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7f3ae-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3ae-122">OUTPUTS</span></span>

### <span data-ttu-id="7f3ae-123">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7f3ae-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="7f3ae-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f3ae-124">NOTES</span></span>

## <span data-ttu-id="7f3ae-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f3ae-125">RELATED LINKS</span></span>

[<span data-ttu-id="7f3ae-126">Új – AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7f3ae-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
