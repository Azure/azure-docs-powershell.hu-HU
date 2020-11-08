---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195254"
---
# <span data-ttu-id="96ae6-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="96ae6-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="96ae6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="96ae6-103">Blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="96ae6-103">Create a blockchain member.</span></span>

## <span data-ttu-id="96ae6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96ae6-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96ae6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="96ae6-106">Blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="96ae6-106">Create a blockchain member.</span></span>

## <span data-ttu-id="96ae6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="96ae6-108">Példa 1: új blockchain-tag létrehozása</span><span class="sxs-lookup"><span data-stu-id="96ae6-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="96ae6-109">A parancs új blockchain-tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="96ae6-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="96ae6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="96ae6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96ae6-111">-AsJob</span></span>
<span data-ttu-id="96ae6-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="96ae6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="96ae6-113">-Konzorcium</span><span class="sxs-lookup"><span data-stu-id="96ae6-113">-Consortium</span></span>
<span data-ttu-id="96ae6-114">A blockchain-tag konzorciumának beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="96ae6-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="96ae6-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="96ae6-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="96ae6-116">A felügyelt konzorcium-kezelési fiók jelszavának megadása</span><span class="sxs-lookup"><span data-stu-id="96ae6-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="96ae6-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="96ae6-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="96ae6-118">Megkapja a konzorciumban a tagok megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="96ae6-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="96ae6-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="96ae6-119">-ConsortiumRole</span></span>
<span data-ttu-id="96ae6-120">A tag szerepkörét kapja a konzorciumban.</span><span class="sxs-lookup"><span data-stu-id="96ae6-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="96ae6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ae6-121">-DefaultProfile</span></span>
<span data-ttu-id="96ae6-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96ae6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96ae6-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="96ae6-123">-FirewallRule</span></span>
<span data-ttu-id="96ae6-124">Tűzfal-szabályok beolvasása vagy beállítása a létrehozáshoz, a FIREWALLRULE tulajdonságainak megjegyzések szakasza és a kivonatoló táblázat létrehozása című témakörben talál segítséget.</span><span class="sxs-lookup"><span data-stu-id="96ae6-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="96ae6-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="96ae6-125">-Location</span></span>
<span data-ttu-id="96ae6-126">A blockchain szolgáltatás földrajzi helye.</span><span class="sxs-lookup"><span data-stu-id="96ae6-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="96ae6-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96ae6-127">-Name</span></span>
<span data-ttu-id="96ae6-128">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="96ae6-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="96ae6-129">-Várva</span><span class="sxs-lookup"><span data-stu-id="96ae6-129">-NoWait</span></span>
<span data-ttu-id="96ae6-130">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="96ae6-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96ae6-131">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="96ae6-131">-Password</span></span>
<span data-ttu-id="96ae6-132">A blockchain-tag alapvető hitelesítő jelszavának megadása.</span><span class="sxs-lookup"><span data-stu-id="96ae6-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="96ae6-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="96ae6-133">-Protocol</span></span>
<span data-ttu-id="96ae6-134">A blockchain-protokollt kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="96ae6-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="96ae6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ae6-135">-ResourceGroupName</span></span>
<span data-ttu-id="96ae6-136">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="96ae6-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="96ae6-137">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="96ae6-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="96ae6-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="96ae6-138">-Sku</span></span>
<span data-ttu-id="96ae6-139">SKU-név beolvasása vagy visszaállítása</span><span class="sxs-lookup"><span data-stu-id="96ae6-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="96ae6-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="96ae6-140">-SkuTier</span></span>
<span data-ttu-id="96ae6-141">SKU-szint beolvasása vagy beállításának módja</span><span class="sxs-lookup"><span data-stu-id="96ae6-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="96ae6-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96ae6-142">-SubscriptionId</span></span>
<span data-ttu-id="96ae6-143">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="96ae6-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="96ae6-144">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="96ae6-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="96ae6-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="96ae6-145">-Tag</span></span>
<span data-ttu-id="96ae6-146">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcspárt tartalmazó párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="96ae6-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="96ae6-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="96ae6-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="96ae6-148">A csomópontok kapacitását kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="96ae6-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="96ae6-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96ae6-149">-Confirm</span></span>
<span data-ttu-id="96ae6-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96ae6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96ae6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96ae6-151">-WhatIf</span></span>
<span data-ttu-id="96ae6-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96ae6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96ae6-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96ae6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96ae6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ae6-154">CommonParameters</span></span>
<span data-ttu-id="96ae6-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96ae6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ae6-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96ae6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ae6-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96ae6-157">INPUTS</span></span>

## <span data-ttu-id="96ae6-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96ae6-158">OUTPUTS</span></span>

### <span data-ttu-id="96ae6-159">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="96ae6-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="96ae6-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96ae6-160">NOTES</span></span>

<span data-ttu-id="96ae6-161">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="96ae6-161">ALIASES</span></span>

<span data-ttu-id="96ae6-162">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="96ae6-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96ae6-163">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="96ae6-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96ae6-164">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="96ae6-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96ae6-165">FIREWALLRULE <IFirewallRule [] >: tűzfalszabályok beolvasása vagy megállítása</span><span class="sxs-lookup"><span data-stu-id="96ae6-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="96ae6-166">`[EndIPAddress <String>]`: A tűzfalszabály-tartományok végpontjának IP-címét adja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="96ae6-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="96ae6-167">`[RuleName <String>]`: A tűzfalszabályok nevének beírása vagy bekapcsolása.</span><span class="sxs-lookup"><span data-stu-id="96ae6-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="96ae6-168">`[StartIPAddress <String>]`: Beilleszti vagy beállítja a tűzfalszabály-tartományok kezdő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="96ae6-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="96ae6-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96ae6-169">RELATED LINKS</span></span>
