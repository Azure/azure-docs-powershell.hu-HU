---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145187"
---
# <span data-ttu-id="7b347-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="7b347-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="7b347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b347-102">SYNOPSIS</span></span>
<span data-ttu-id="7b347-103">Blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="7b347-103">Create a blockchain member.</span></span>

## <span data-ttu-id="7b347-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b347-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b347-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b347-105">DESCRIPTION</span></span>
<span data-ttu-id="7b347-106">Blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="7b347-106">Create a blockchain member.</span></span>

## <span data-ttu-id="7b347-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b347-107">EXAMPLES</span></span>

### <span data-ttu-id="7b347-108">1. példa: Új blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="7b347-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7b347-109">Ezzel a paranccsal új blockchain-tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7b347-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="7b347-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b347-110">PARAMETERS</span></span>

### <span data-ttu-id="7b347-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b347-111">-AsJob</span></span>
<span data-ttu-id="7b347-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="7b347-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7b347-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="7b347-113">-Consortium</span></span>
<span data-ttu-id="7b347-114">Beállítja vagy beállítja a blockchain-tagnak a consortiumt.</span><span class="sxs-lookup"><span data-stu-id="7b347-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="7b347-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7b347-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="7b347-116">Beállítja a felügyelt consortium felügyeleti fiók jelszavát.</span><span class="sxs-lookup"><span data-stu-id="7b347-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="7b347-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="7b347-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="7b347-118">A consortium tagjainak megjelenítendő nevét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7b347-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="7b347-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="7b347-119">-ConsortiumRole</span></span>
<span data-ttu-id="7b347-120">A tag szerepkörét a consortiumban betöltötte.</span><span class="sxs-lookup"><span data-stu-id="7b347-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="7b347-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b347-121">-DefaultProfile</span></span>
<span data-ttu-id="7b347-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b347-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b347-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7b347-123">-FirewallRule</span></span>
<span data-ttu-id="7b347-124">Tűzfalszabályok létrehozása vagy beállítása A TŰZFALSZABÁLY tulajdonságairól és a kivonattáblák létrehozásáról a NOTES szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="7b347-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b347-125">-Location</span><span class="sxs-lookup"><span data-stu-id="7b347-125">-Location</span></span>
<span data-ttu-id="7b347-126">A blockchain szolgáltatás FÖLDRAJZI helye.</span><span class="sxs-lookup"><span data-stu-id="7b347-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="7b347-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7b347-127">-Name</span></span>
<span data-ttu-id="7b347-128">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="7b347-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="7b347-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7b347-129">-NoWait</span></span>
<span data-ttu-id="7b347-130">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="7b347-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7b347-131">-Password</span><span class="sxs-lookup"><span data-stu-id="7b347-131">-Password</span></span>
<span data-ttu-id="7b347-132">Beállítja a blockchain tag alapvető hitelesítési jelszavát.</span><span class="sxs-lookup"><span data-stu-id="7b347-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="7b347-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7b347-133">-Protocol</span></span>
<span data-ttu-id="7b347-134">Beállítja vagy beállítja a blockchain protokollt.</span><span class="sxs-lookup"><span data-stu-id="7b347-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="7b347-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b347-135">-ResourceGroupName</span></span>
<span data-ttu-id="7b347-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b347-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7b347-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="7b347-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7b347-138">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="7b347-138">-Sku</span></span>
<span data-ttu-id="7b347-139">A termékváltozat nevének lekérte vagy be van állítja</span><span class="sxs-lookup"><span data-stu-id="7b347-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="7b347-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7b347-140">-SkuTier</span></span>
<span data-ttu-id="7b347-141">Termékváltozatszintet kap vagy állít be</span><span class="sxs-lookup"><span data-stu-id="7b347-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="7b347-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b347-142">-SubscriptionId</span></span>
<span data-ttu-id="7b347-143">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="7b347-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7b347-144">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="7b347-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7b347-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b347-145">-Tag</span></span>
<span data-ttu-id="7b347-146">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="7b347-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="7b347-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7b347-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="7b347-148">Beállítja vagy beállítja a csomópontok kapacitását.</span><span class="sxs-lookup"><span data-stu-id="7b347-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="7b347-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b347-149">-Confirm</span></span>
<span data-ttu-id="7b347-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b347-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b347-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b347-151">-WhatIf</span></span>
<span data-ttu-id="7b347-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b347-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b347-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b347-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b347-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b347-154">CommonParameters</span></span>
<span data-ttu-id="7b347-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b347-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b347-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b347-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b347-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b347-157">INPUTS</span></span>

## <span data-ttu-id="7b347-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b347-158">OUTPUTS</span></span>

### <span data-ttu-id="7b347-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="7b347-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="7b347-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b347-160">NOTES</span></span>

<span data-ttu-id="7b347-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7b347-161">ALIASES</span></span>

<span data-ttu-id="7b347-162">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7b347-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b347-163">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7b347-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b347-164">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b347-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b347-165">FIREWALLRULE <IFirewallRule[]>: Tűzfalszabályok be- vagy kikapcsolása</span><span class="sxs-lookup"><span data-stu-id="7b347-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="7b347-166">`[EndIPAddress <String>]`: Beállítja vagy beállítja a tűzfalszabály-tartomány IP-címét.</span><span class="sxs-lookup"><span data-stu-id="7b347-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="7b347-167">`[RuleName <String>]`: Beállítja vagy beállítja a tűzfalszabályok nevét.</span><span class="sxs-lookup"><span data-stu-id="7b347-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="7b347-168">`[StartIPAddress <String>]`: A tűzfalszabály tartományának kezdő IP-címét kapja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="7b347-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="7b347-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b347-169">RELATED LINKS</span></span>

