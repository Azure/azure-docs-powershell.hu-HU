---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186091"
---
# <span data-ttu-id="69c1a-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="69c1a-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="69c1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="69c1a-103">Azure Firewall Policy Rule Collection csoport eltávolítása Azure tűzfal-házirendben</span><span class="sxs-lookup"><span data-stu-id="69c1a-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="69c1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69c1a-104">SYNTAX</span></span>

### <span data-ttu-id="69c1a-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69c1a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c1a-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c1a-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69c1a-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c1a-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69c1a-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c1a-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c1a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="69c1a-109">DESCRIPTION</span></span>
<span data-ttu-id="69c1a-110">A **Remove-AzFirewallPolicyRuleCollectionGroup** parancsmag egy szabály-összegyűjtési csoportot távolít el egy Azure tűzfal-házirendből.</span><span class="sxs-lookup"><span data-stu-id="69c1a-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="69c1a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="69c1a-111">EXAMPLES</span></span>

### <span data-ttu-id="69c1a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="69c1a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="69c1a-113">Ez a példa eltávolítja a tűzfal házirend-objektum "testRcGroup" nevű colelction-csoportját a tűzfal házirend-objektumában $fp</span><span class="sxs-lookup"><span data-stu-id="69c1a-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="69c1a-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="69c1a-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="69c1a-115">Ez a példa eltávolítja a "testRcGroup" nevű tűzfal-házirend colelction-csoportját a "fpName" frpm a resourcegroup nevek "testRg" nevű tűzfalban.</span><span class="sxs-lookup"><span data-stu-id="69c1a-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="69c1a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69c1a-116">PARAMETERS</span></span>

### <span data-ttu-id="69c1a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69c1a-117">-AsJob</span></span>
<span data-ttu-id="69c1a-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="69c1a-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c1a-119">-DefaultProfile</span></span>
<span data-ttu-id="69c1a-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69c1a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c1a-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="69c1a-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="69c1a-122">A tűzfal-házirend neve</span><span class="sxs-lookup"><span data-stu-id="69c1a-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="69c1a-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="69c1a-124">Tűzfal-házirend.</span><span class="sxs-lookup"><span data-stu-id="69c1a-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="69c1a-125">-Force</span></span>
<span data-ttu-id="69c1a-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69c1a-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69c1a-127">-InputObject</span></span>
<span data-ttu-id="69c1a-128">A tűzfal házirend-gyűjteményi csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="69c1a-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69c1a-129">-Name</span></span>
<span data-ttu-id="69c1a-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="69c1a-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69c1a-131">-PassThru</span></span>
<span data-ttu-id="69c1a-132">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="69c1a-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69c1a-133">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="69c1a-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c1a-134">-ResourceGroupName</span></span>
<span data-ttu-id="69c1a-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="69c1a-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69c1a-136">-ResourceId</span></span>
<span data-ttu-id="69c1a-137">A szabály-összegyűjtési csoport erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="69c1a-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69c1a-138">-Confirm</span></span>
<span data-ttu-id="69c1a-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69c1a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c1a-140">-WhatIf</span></span>
<span data-ttu-id="69c1a-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69c1a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c1a-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69c1a-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c1a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c1a-143">CommonParameters</span></span>
<span data-ttu-id="69c1a-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69c1a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c1a-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69c1a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c1a-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c1a-146">INPUTS</span></span>

### <span data-ttu-id="69c1a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="69c1a-147">System.String</span></span>

### <span data-ttu-id="69c1a-148">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="69c1a-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="69c1a-149">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="69c1a-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="69c1a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c1a-150">OUTPUTS</span></span>

### <span data-ttu-id="69c1a-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69c1a-151">System.Boolean</span></span>

## <span data-ttu-id="69c1a-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69c1a-152">NOTES</span></span>

## <span data-ttu-id="69c1a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69c1a-153">RELATED LINKS</span></span>
