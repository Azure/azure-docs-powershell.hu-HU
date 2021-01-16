---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363522"
---
# <span data-ttu-id="ee1f2-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ee1f2-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ee1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1f2-103">Az Azure tűzfal házirendszabálycsoportját távolítja el egy Azure tűzfal-házirendben</span><span class="sxs-lookup"><span data-stu-id="ee1f2-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="ee1f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee1f2-104">SYNTAX</span></span>

### <span data-ttu-id="ee1f2-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee1f2-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1f2-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1f2-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1f2-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1f2-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1f2-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1f2-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1f2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee1f2-109">DESCRIPTION</span></span>
<span data-ttu-id="ee1f2-110">A **Remove-AzFirewallPolicyRuleCollectionGroup** parancsmag eltávolít egy szabálycsoportot az Azure tűzfalházi házirendből.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ee1f2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee1f2-111">EXAMPLES</span></span>

### <span data-ttu-id="ee1f2-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ee1f2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="ee1f2-113">Ebben a példában eltávolítja a "testRcGroup" nevű tűzfalháziszabály-oszlopfedő csoportot a tűzfal házirendobjektumában $fp</span><span class="sxs-lookup"><span data-stu-id="ee1f2-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="ee1f2-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ee1f2-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="ee1f2-115">Ebben a példában eltávolítja a "testRcGroup" nevű tűzfalháziszabály-oszlopcsoportot az "fpName" frpm nevű tűzfalban az erőforráscsoport neve "testRg"</span><span class="sxs-lookup"><span data-stu-id="ee1f2-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="ee1f2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1f2-116">PARAMETERS</span></span>

### <span data-ttu-id="ee1f2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee1f2-117">-AsJob</span></span>
<span data-ttu-id="ee1f2-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ee1f2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee1f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1f2-119">-DefaultProfile</span></span>
<span data-ttu-id="ee1f2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1f2-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="ee1f2-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="ee1f2-122">A tűzfal házirend neve</span><span class="sxs-lookup"><span data-stu-id="ee1f2-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="ee1f2-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ee1f2-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="ee1f2-124">Tűzfal házirend.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="ee1f2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ee1f2-125">-Force</span></span>
<span data-ttu-id="ee1f2-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ee1f2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1f2-127">-InputObject</span></span>
<span data-ttu-id="ee1f2-128">Firewall Policy Rule collection group object</span><span class="sxs-lookup"><span data-stu-id="ee1f2-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="ee1f2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ee1f2-129">-Name</span></span>
<span data-ttu-id="ee1f2-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-130">The resource name.</span></span>

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

### <span data-ttu-id="ee1f2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee1f2-131">-PassThru</span></span>
<span data-ttu-id="ee1f2-132">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee1f2-133">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee1f2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1f2-134">-ResourceGroupName</span></span>
<span data-ttu-id="ee1f2-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-135">The resource group name.</span></span>

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

### <span data-ttu-id="ee1f2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1f2-136">-ResourceId</span></span>
<span data-ttu-id="ee1f2-137">A Szabálycsoport-csoport erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ee1f2-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="ee1f2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee1f2-138">-Confirm</span></span>
<span data-ttu-id="ee1f2-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1f2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1f2-140">-WhatIf</span></span>
<span data-ttu-id="ee1f2-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1f2-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1f2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1f2-143">CommonParameters</span></span>
<span data-ttu-id="ee1f2-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1f2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1f2-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee1f2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1f2-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee1f2-146">INPUTS</span></span>

### <span data-ttu-id="ee1f2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ee1f2-147">System.String</span></span>

### <span data-ttu-id="ee1f2-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ee1f2-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="ee1f2-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="ee1f2-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="ee1f2-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee1f2-150">OUTPUTS</span></span>

### <span data-ttu-id="ee1f2-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee1f2-151">System.Boolean</span></span>

## <span data-ttu-id="ee1f2-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee1f2-152">NOTES</span></span>

## <span data-ttu-id="ee1f2-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee1f2-153">RELATED LINKS</span></span>
