---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186089"
---
# <span data-ttu-id="42459-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="42459-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="42459-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42459-102">SYNOPSIS</span></span>
<span data-ttu-id="42459-103">Azure tűzfal-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="42459-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="42459-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42459-104">SYNTAX</span></span>

### <span data-ttu-id="42459-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42459-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42459-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42459-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42459-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42459-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42459-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42459-108">DESCRIPTION</span></span>
<span data-ttu-id="42459-109">A **Remove-AzFirewallPolicy** parancsmag eltávolít egy Azure tűzfal-házirendet.</span><span class="sxs-lookup"><span data-stu-id="42459-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="42459-110">Példák</span><span class="sxs-lookup"><span data-stu-id="42459-110">EXAMPLES</span></span>

### <span data-ttu-id="42459-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42459-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="42459-112">Ez a példa eltávolítja a "firewallpolicy" nevű tűzfal-házirendet a resourcegroup "TestRg" ("").</span><span class="sxs-lookup"><span data-stu-id="42459-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="42459-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="42459-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="42459-114">Ebben a példában az azonosítóval eltávolítja a tűzfal-házirendet.</span><span class="sxs-lookup"><span data-stu-id="42459-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="42459-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="42459-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="42459-116">Ez a példa eltávolítja a tűzfal házirend-$fp</span><span class="sxs-lookup"><span data-stu-id="42459-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="42459-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42459-117">PARAMETERS</span></span>

### <span data-ttu-id="42459-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42459-118">-AsJob</span></span>
<span data-ttu-id="42459-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="42459-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42459-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42459-120">-DefaultProfile</span></span>
<span data-ttu-id="42459-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42459-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42459-122">-Force</span><span class="sxs-lookup"><span data-stu-id="42459-122">-Force</span></span>
<span data-ttu-id="42459-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42459-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="42459-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42459-124">-InputObject</span></span>
<span data-ttu-id="42459-125">A AzureFirewall házirend</span><span class="sxs-lookup"><span data-stu-id="42459-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42459-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42459-126">-Name</span></span>
<span data-ttu-id="42459-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="42459-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42459-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42459-128">-PassThru</span></span>
<span data-ttu-id="42459-129">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="42459-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42459-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="42459-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42459-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42459-131">-ResourceGroupName</span></span>
<span data-ttu-id="42459-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="42459-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42459-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42459-133">-ResourceId</span></span>
<span data-ttu-id="42459-134">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="42459-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42459-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42459-135">-Confirm</span></span>
<span data-ttu-id="42459-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42459-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42459-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42459-137">-WhatIf</span></span>
<span data-ttu-id="42459-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42459-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42459-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42459-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42459-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42459-140">CommonParameters</span></span>
<span data-ttu-id="42459-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42459-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42459-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="42459-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42459-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42459-143">INPUTS</span></span>

### <span data-ttu-id="42459-144">System. String</span><span class="sxs-lookup"><span data-stu-id="42459-144">System.String</span></span>

### <span data-ttu-id="42459-145">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="42459-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="42459-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42459-146">OUTPUTS</span></span>

### <span data-ttu-id="42459-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42459-147">System.Boolean</span></span>

## <span data-ttu-id="42459-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42459-148">NOTES</span></span>

## <span data-ttu-id="42459-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42459-149">RELATED LINKS</span></span>
