---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024869"
---
# <span data-ttu-id="d175e-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="d175e-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="d175e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d175e-102">SYNOPSIS</span></span>
<span data-ttu-id="d175e-103">Hozza létre vagy frissítse a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d175e-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="d175e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d175e-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d175e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d175e-105">DESCRIPTION</span></span>
<span data-ttu-id="d175e-106">Hozza létre vagy frissítse a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d175e-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="d175e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d175e-107">EXAMPLES</span></span>

### <span data-ttu-id="d175e-108">Példa 1: blockchain-tranzakció csomópont létrehozása</span><span class="sxs-lookup"><span data-stu-id="d175e-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="d175e-109">Ez a parancs létrehoz egy blockchain-tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="d175e-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="d175e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d175e-110">PARAMETERS</span></span>

### <span data-ttu-id="d175e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d175e-111">-AsJob</span></span>
<span data-ttu-id="d175e-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d175e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d175e-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d175e-113">-BlockchainMemberName</span></span>
<span data-ttu-id="d175e-114">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="d175e-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="d175e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d175e-115">-DefaultProfile</span></span>
<span data-ttu-id="d175e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d175e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d175e-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="d175e-117">-FirewallRule</span></span>
<span data-ttu-id="d175e-118">A tűzfalszabályok beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="d175e-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="d175e-119">A kivitelezéshez tekintse meg a FIREWALLRULE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d175e-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d175e-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="d175e-120">-Location</span></span>
<span data-ttu-id="d175e-121">A tranzakció csomópont helyét kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="d175e-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="d175e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d175e-122">-Name</span></span>
<span data-ttu-id="d175e-123">A tranzakció csomópontjának neve</span><span class="sxs-lookup"><span data-stu-id="d175e-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d175e-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="d175e-124">-NoWait</span></span>
<span data-ttu-id="d175e-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d175e-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d175e-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="d175e-126">-Password</span></span>
<span data-ttu-id="d175e-127">A Transaction node (DNS-végpont) alapvető hitelesítő jelszavának megadása</span><span class="sxs-lookup"><span data-stu-id="d175e-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="d175e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d175e-128">-ResourceGroupName</span></span>
<span data-ttu-id="d175e-129">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d175e-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d175e-130">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="d175e-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d175e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d175e-131">-SubscriptionId</span></span>
<span data-ttu-id="d175e-132">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="d175e-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d175e-133">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="d175e-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d175e-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d175e-134">-Confirm</span></span>
<span data-ttu-id="d175e-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d175e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d175e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d175e-136">-WhatIf</span></span>
<span data-ttu-id="d175e-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d175e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d175e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d175e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d175e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d175e-139">CommonParameters</span></span>
<span data-ttu-id="d175e-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d175e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d175e-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d175e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d175e-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d175e-142">INPUTS</span></span>

## <span data-ttu-id="d175e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d175e-143">OUTPUTS</span></span>

### <span data-ttu-id="d175e-144">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="d175e-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="d175e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d175e-145">NOTES</span></span>

<span data-ttu-id="d175e-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d175e-146">ALIASES</span></span>

<span data-ttu-id="d175e-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d175e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d175e-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d175e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d175e-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d175e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d175e-150">FIREWALLRULE <IFirewallRule [] >: beolvassa vagy beállítja a tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="d175e-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="d175e-151">`[EndIPAddress <String>]`: A tűzfalszabály-tartományok végpontjának IP-címét adja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="d175e-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="d175e-152">`[RuleName <String>]`: A tűzfalszabályok nevének beírása vagy bekapcsolása.</span><span class="sxs-lookup"><span data-stu-id="d175e-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="d175e-153">`[StartIPAddress <String>]`: Beilleszti vagy beállítja a tűzfalszabály-tartományok kezdő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="d175e-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="d175e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d175e-154">RELATED LINKS</span></span>

