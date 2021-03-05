---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: 15af3a6bb7e80020cd014bfbdd8ff944cafd187a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009350"
---
# <span data-ttu-id="2ea17-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="2ea17-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="2ea17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea17-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea17-103">Blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ea17-103">Create a blockchain member.</span></span>

## <span data-ttu-id="2ea17-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ea17-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ea17-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ea17-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea17-106">Blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ea17-106">Create a blockchain member.</span></span>

## <span data-ttu-id="2ea17-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ea17-107">EXAMPLES</span></span>

### <span data-ttu-id="2ea17-108">1. példa: Új blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ea17-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="2ea17-109">Ezzel a paranccsal új blockchain-tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2ea17-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="2ea17-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ea17-110">PARAMETERS</span></span>

### <span data-ttu-id="2ea17-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ea17-111">-AsJob</span></span>
<span data-ttu-id="2ea17-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="2ea17-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2ea17-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="2ea17-113">-Consortium</span></span>
<span data-ttu-id="2ea17-114">Beállítja vagy beállítja a blockchain-tagnak a consortiumt.</span><span class="sxs-lookup"><span data-stu-id="2ea17-114">Gets or sets the consortium for the blockchain member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="2ea17-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="2ea17-116">Beállítja a felügyelt consortium felügyeleti fiók jelszavát.</span><span class="sxs-lookup"><span data-stu-id="2ea17-116">Sets the managed consortium management account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="2ea17-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="2ea17-118">A consortium tagjainak megjelenítendő nevét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ea17-118">Gets the display name of the member in the consortium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="2ea17-119">-ConsortiumRole</span></span>
<span data-ttu-id="2ea17-120">A tag szerepkörét a consortiumban betöltötte.</span><span class="sxs-lookup"><span data-stu-id="2ea17-120">Gets the role of the member in the consortium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea17-121">-DefaultProfile</span></span>
<span data-ttu-id="2ea17-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ea17-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="2ea17-123">-FirewallRule</span></span>
<span data-ttu-id="2ea17-124">Tűzfalszabályok létrehozása vagy beállítása A TŰZFALSZABÁLY tulajdonságairól és a kivonattáblák létrehozásáról a NOTES szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="2ea17-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-125">-Location</span><span class="sxs-lookup"><span data-stu-id="2ea17-125">-Location</span></span>
<span data-ttu-id="2ea17-126">A blockchain szolgáltatás FÖLDRAJZI helye.</span><span class="sxs-lookup"><span data-stu-id="2ea17-126">The GEO location of the blockchain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2ea17-127">-Name</span></span>
<span data-ttu-id="2ea17-128">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="2ea17-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ea17-129">-NoWait</span></span>
<span data-ttu-id="2ea17-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="2ea17-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ea17-131">-Password</span><span class="sxs-lookup"><span data-stu-id="2ea17-131">-Password</span></span>
<span data-ttu-id="2ea17-132">Beállítja a blockchain tag alapszintű hitelesítési jelszavát.</span><span class="sxs-lookup"><span data-stu-id="2ea17-132">Sets the basic auth password of the blockchain member.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2ea17-133">-Protocol</span></span>
<span data-ttu-id="2ea17-134">Beállítja vagy beállítja a blockchain protokollt.</span><span class="sxs-lookup"><span data-stu-id="2ea17-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea17-135">-ResourceGroupName</span></span>
<span data-ttu-id="2ea17-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ea17-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2ea17-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="2ea17-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-138">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="2ea17-138">-Sku</span></span>
<span data-ttu-id="2ea17-139">Termékváltozat nevének lekérte vagy be van állítja</span><span class="sxs-lookup"><span data-stu-id="2ea17-139">Gets or sets Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2ea17-140">-SkuTier</span></span>
<span data-ttu-id="2ea17-141">Termékváltozatréteg lekért vagy beállítja</span><span class="sxs-lookup"><span data-stu-id="2ea17-141">Gets or sets Sku tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ea17-142">-SubscriptionId</span></span>
<span data-ttu-id="2ea17-143">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="2ea17-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ea17-144">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="2ea17-144">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ea17-145">-Tag</span></span>
<span data-ttu-id="2ea17-146">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="2ea17-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2ea17-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="2ea17-148">Beállítja vagy beállítja a csomópontok kapacitását.</span><span class="sxs-lookup"><span data-stu-id="2ea17-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea17-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ea17-149">-Confirm</span></span>
<span data-ttu-id="2ea17-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ea17-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea17-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea17-151">-WhatIf</span></span>
<span data-ttu-id="2ea17-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ea17-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea17-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ea17-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea17-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea17-154">CommonParameters</span></span>
<span data-ttu-id="2ea17-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea17-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea17-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ea17-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea17-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ea17-157">INPUTS</span></span>

## <span data-ttu-id="2ea17-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea17-158">OUTPUTS</span></span>

### <span data-ttu-id="2ea17-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="2ea17-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="2ea17-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ea17-160">NOTES</span></span>

<span data-ttu-id="2ea17-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2ea17-161">ALIASES</span></span>

<span data-ttu-id="2ea17-162">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2ea17-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ea17-163">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2ea17-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ea17-164">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ea17-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ea17-165">FIREWALLRULE <IFirewallRule[]>: Tűzfalszabályok be- vagy kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="2ea17-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="2ea17-166">`[EndIPAddress <String>]`: Beállítja vagy beállítja a tűzfalszabály-tartomány IP-címét.</span><span class="sxs-lookup"><span data-stu-id="2ea17-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="2ea17-167">`[RuleName <String>]`: Beállítja vagy beállítja a tűzfalszabályok nevét.</span><span class="sxs-lookup"><span data-stu-id="2ea17-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="2ea17-168">`[StartIPAddress <String>]`: A tűzfalszabály tartományának kezdő IP-címét kapja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="2ea17-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="2ea17-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ea17-169">RELATED LINKS</span></span>

