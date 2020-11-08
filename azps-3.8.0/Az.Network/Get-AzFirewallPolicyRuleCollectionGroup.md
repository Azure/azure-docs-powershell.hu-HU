---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013344"
---
# <span data-ttu-id="f5460-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="f5460-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="f5460-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5460-102">SYNOPSIS</span></span>
<span data-ttu-id="f5460-103">Az Azure tűzfal házirend-begyűjtési csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5460-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="f5460-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5460-104">SYNTAX</span></span>

### <span data-ttu-id="f5460-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5460-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5460-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5460-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5460-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5460-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5460-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5460-108">DESCRIPTION</span></span>
<span data-ttu-id="f5460-109">A **Get-AzFirewallPolicyRuleCollectionGroup** parancsmag a tűzfal-házirendben említett RuleCollectionGroup kapja.</span><span class="sxs-lookup"><span data-stu-id="f5460-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="f5460-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5460-110">EXAMPLES</span></span>

### <span data-ttu-id="f5460-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5460-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="f5460-112">Ez a példa beolvassa a collectionGroup szabályt a tűzfal-házirend $fp</span><span class="sxs-lookup"><span data-stu-id="f5460-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="f5460-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5460-113">PARAMETERS</span></span>

### <span data-ttu-id="f5460-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f5460-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="f5460-115">Tűzfal-házirend.</span><span class="sxs-lookup"><span data-stu-id="f5460-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5460-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="f5460-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="f5460-117">A tűzfal-házirend neve</span><span class="sxs-lookup"><span data-stu-id="f5460-117">The Firewall policy name</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5460-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5460-118">-DefaultProfile</span></span>
<span data-ttu-id="f5460-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5460-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5460-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5460-120">-Name</span></span>
<span data-ttu-id="f5460-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f5460-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5460-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5460-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5460-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5460-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5460-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5460-124">-ResourceId</span></span>
<span data-ttu-id="f5460-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f5460-125">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5460-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5460-126">CommonParameters</span></span>
<span data-ttu-id="f5460-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5460-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5460-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5460-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5460-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5460-129">INPUTS</span></span>

### <span data-ttu-id="f5460-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f5460-130">System.String</span></span>

### <span data-ttu-id="f5460-131">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f5460-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="f5460-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5460-132">OUTPUTS</span></span>

### <span data-ttu-id="f5460-133">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f5460-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="f5460-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 1.12.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f5460-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f5460-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5460-135">NOTES</span></span>

## <span data-ttu-id="f5460-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5460-136">RELATED LINKS</span></span>
