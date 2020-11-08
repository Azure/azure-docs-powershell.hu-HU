---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025756"
---
# <span data-ttu-id="833be-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="833be-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="833be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="833be-102">SYNOPSIS</span></span>
<span data-ttu-id="833be-103">Frissítse a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="833be-103">Update the transaction node.</span></span>

## <span data-ttu-id="833be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="833be-104">SYNTAX</span></span>

### <span data-ttu-id="833be-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="833be-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="833be-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="833be-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="833be-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="833be-107">DESCRIPTION</span></span>
<span data-ttu-id="833be-108">Frissítse a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="833be-108">Update the transaction node.</span></span>

## <span data-ttu-id="833be-109">Példák</span><span class="sxs-lookup"><span data-stu-id="833be-109">EXAMPLES</span></span>

### <span data-ttu-id="833be-110">Példa 1: transcation csomópont frissítése</span><span class="sxs-lookup"><span data-stu-id="833be-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="833be-111">Ez a parancs frissíti a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="833be-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="833be-112">2. példa: transcation-csomópont frissítése</span><span class="sxs-lookup"><span data-stu-id="833be-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="833be-113">Ez a parancs frissíti a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="833be-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="833be-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="833be-114">PARAMETERS</span></span>

### <span data-ttu-id="833be-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="833be-115">-BlockchainMemberName</span></span>
<span data-ttu-id="833be-116">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="833be-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="833be-117">-DefaultProfile</span></span>
<span data-ttu-id="833be-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="833be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="833be-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="833be-119">-FirewallRule</span></span>
<span data-ttu-id="833be-120">A tűzfalszabályok beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="833be-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="833be-121">A kivitelezéshez tekintse meg a FIREWALLRULE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="833be-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="833be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="833be-122">-InputObject</span></span>
<span data-ttu-id="833be-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="833be-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="833be-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="833be-124">-Name</span></span>
<span data-ttu-id="833be-125">A tranzakció csomópontjának neve</span><span class="sxs-lookup"><span data-stu-id="833be-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833be-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="833be-126">-Password</span></span>
<span data-ttu-id="833be-127">A Transaction node (DNS-végpont) alapvető hitelesítő jelszavának megadása</span><span class="sxs-lookup"><span data-stu-id="833be-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="833be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="833be-128">-ResourceGroupName</span></span>
<span data-ttu-id="833be-129">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="833be-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="833be-130">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="833be-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833be-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="833be-131">-SubscriptionId</span></span>
<span data-ttu-id="833be-132">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="833be-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="833be-133">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="833be-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833be-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="833be-134">-Confirm</span></span>
<span data-ttu-id="833be-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="833be-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="833be-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="833be-136">-WhatIf</span></span>
<span data-ttu-id="833be-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="833be-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="833be-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="833be-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="833be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833be-139">CommonParameters</span></span>
<span data-ttu-id="833be-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="833be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833be-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="833be-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833be-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="833be-142">INPUTS</span></span>

### <span data-ttu-id="833be-143">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="833be-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="833be-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="833be-144">OUTPUTS</span></span>

### <span data-ttu-id="833be-145">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="833be-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="833be-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="833be-146">NOTES</span></span>

<span data-ttu-id="833be-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="833be-147">ALIASES</span></span>

<span data-ttu-id="833be-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="833be-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="833be-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="833be-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="833be-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="833be-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="833be-151">FIREWALLRULE <IFirewallRule [] >: beolvassa vagy beállítja a tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="833be-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="833be-152">`[EndIPAddress <String>]`: A tűzfalszabály-tartományok végpontjának IP-címét adja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="833be-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="833be-153">`[RuleName <String>]`: A tűzfalszabályok nevének beírása vagy bekapcsolása.</span><span class="sxs-lookup"><span data-stu-id="833be-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="833be-154">`[StartIPAddress <String>]`: Beilleszti vagy beállítja a tűzfalszabály-tartományok kezdő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="833be-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="833be-155">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="833be-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="833be-156">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="833be-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="833be-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="833be-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="833be-158">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="833be-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="833be-159">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="833be-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="833be-160">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="833be-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="833be-161">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="833be-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="833be-162">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="833be-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="833be-163">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="833be-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="833be-164">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="833be-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="833be-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="833be-165">RELATED LINKS</span></span>

