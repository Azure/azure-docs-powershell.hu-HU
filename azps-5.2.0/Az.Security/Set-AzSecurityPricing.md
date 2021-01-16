---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355158"
---
# <span data-ttu-id="cdbfb-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cdbfb-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="cdbfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdbfb-102">SYNOPSIS</span></span>

<span data-ttu-id="cdbfb-103">Engedélyezi vagy letiltja az Azure Defender-csomagokat egy előfizetéshez az Azure Biztonsági központban.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="cdbfb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cdbfb-104">SYNTAX</span></span>

### <span data-ttu-id="cdbfb-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdbfb-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdbfb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cdbfb-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdbfb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cdbfb-107">DESCRIPTION</span></span>

<span data-ttu-id="cdbfb-108">Engedélyezze vagy tiltsa le egy előfizetéshez az Azure Defender-csomagok bármelyikét.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="cdbfb-109">Az Azure Defenderről és a rendelkezésre álló csomagokról további információt az Azure Defender – [Bevezetés szolgáltatásban talál.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="cdbfb-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="cdbfb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cdbfb-110">EXAMPLES</span></span>

### <span data-ttu-id="cdbfb-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cdbfb-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="cdbfb-112">Engedélyezi **az Azure Defendert az** előfizetés kiszolgálóihoz.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="cdbfb-113">A "Standard" az Azure Defender-csomag "Be" állapotára utal, az Azure Security Center Azure Portalon elérhető árazási és beállítási területén látható módon.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="cdbfb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdbfb-114">PARAMETERS</span></span>

### <span data-ttu-id="cdbfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbfb-115">-DefaultProfile</span></span>

<span data-ttu-id="cdbfb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdbfb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdbfb-117">-InputObject</span></span>

<span data-ttu-id="cdbfb-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdbfb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cdbfb-119">-Name</span></span>

<span data-ttu-id="cdbfb-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbfb-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="cdbfb-121">-PricingTier</span></span>

<span data-ttu-id="cdbfb-122">Árazási szint.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbfb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdbfb-123">-Confirm</span></span>

<span data-ttu-id="cdbfb-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbfb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdbfb-125">-WhatIf</span></span>

<span data-ttu-id="cdbfb-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdbfb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdbfb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbfb-128">CommonParameters</span></span>

<span data-ttu-id="cdbfb-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdbfb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbfb-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdbfb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbfb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdbfb-131">INPUTS</span></span>

### <span data-ttu-id="cdbfb-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cdbfb-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="cdbfb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdbfb-133">OUTPUTS</span></span>

### <span data-ttu-id="cdbfb-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cdbfb-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="cdbfb-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cdbfb-135">NOTES</span></span>

## <span data-ttu-id="cdbfb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdbfb-136">RELATED LINKS</span></span>
