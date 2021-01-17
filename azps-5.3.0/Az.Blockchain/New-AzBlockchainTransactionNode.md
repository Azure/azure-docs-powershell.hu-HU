---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480992"
---
# <span data-ttu-id="be1d8-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="be1d8-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="be1d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="be1d8-103">Hozza létre vagy frissítse a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="be1d8-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="be1d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be1d8-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be1d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be1d8-105">DESCRIPTION</span></span>
<span data-ttu-id="be1d8-106">Hozza létre vagy frissítse a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="be1d8-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="be1d8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be1d8-107">EXAMPLES</span></span>

### <span data-ttu-id="be1d8-108">1. példa: Blockchain tranzakciós csomópont létrehozása</span><span class="sxs-lookup"><span data-stu-id="be1d8-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="be1d8-109">Ez a parancs blockchain tranzakciós csomópontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="be1d8-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="be1d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be1d8-110">PARAMETERS</span></span>

### <span data-ttu-id="be1d8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be1d8-111">-AsJob</span></span>
<span data-ttu-id="be1d8-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="be1d8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="be1d8-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="be1d8-113">-BlockchainMemberName</span></span>
<span data-ttu-id="be1d8-114">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="be1d8-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="be1d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1d8-115">-DefaultProfile</span></span>
<span data-ttu-id="be1d8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be1d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be1d8-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="be1d8-117">-FirewallRule</span></span>
<span data-ttu-id="be1d8-118">Beállítja vagy beállítja a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="be1d8-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="be1d8-119">A felépítéséről a NOTES (JEGYZETEK) szakaszban láthatja a FIREWALLRULE tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="be1d8-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="be1d8-120">-Location</span><span class="sxs-lookup"><span data-stu-id="be1d8-120">-Location</span></span>
<span data-ttu-id="be1d8-121">Beállítja vagy beállítja a tranzakciós csomópont helyét.</span><span class="sxs-lookup"><span data-stu-id="be1d8-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="be1d8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="be1d8-122">-Name</span></span>
<span data-ttu-id="be1d8-123">Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="be1d8-123">Transaction node name.</span></span>

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

### <span data-ttu-id="be1d8-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be1d8-124">-NoWait</span></span>
<span data-ttu-id="be1d8-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="be1d8-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be1d8-126">-Password</span><span class="sxs-lookup"><span data-stu-id="be1d8-126">-Password</span></span>
<span data-ttu-id="be1d8-127">Beállítja a tranzakciós csomópont dns-végpontjának alapvető hitelesítésjelszóját.</span><span class="sxs-lookup"><span data-stu-id="be1d8-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="be1d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be1d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="be1d8-129">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be1d8-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="be1d8-130">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="be1d8-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="be1d8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be1d8-131">-SubscriptionId</span></span>
<span data-ttu-id="be1d8-132">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="be1d8-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="be1d8-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="be1d8-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="be1d8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be1d8-134">-Confirm</span></span>
<span data-ttu-id="be1d8-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="be1d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be1d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be1d8-136">-WhatIf</span></span>
<span data-ttu-id="be1d8-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="be1d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be1d8-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be1d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be1d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1d8-139">CommonParameters</span></span>
<span data-ttu-id="be1d8-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be1d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be1d8-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be1d8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1d8-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be1d8-142">INPUTS</span></span>

## <span data-ttu-id="be1d8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be1d8-143">OUTPUTS</span></span>

### <span data-ttu-id="be1d8-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="be1d8-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="be1d8-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be1d8-145">NOTES</span></span>

<span data-ttu-id="be1d8-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="be1d8-146">ALIASES</span></span>

<span data-ttu-id="be1d8-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="be1d8-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be1d8-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="be1d8-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be1d8-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be1d8-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be1d8-150">FIREWALLRULE <IFirewallRule[]>: Beállítja vagy beállítja a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="be1d8-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="be1d8-151">`[EndIPAddress <String>]`: Beállítja vagy beállítja a tűzfalszabály-tartomány IP-címét.</span><span class="sxs-lookup"><span data-stu-id="be1d8-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="be1d8-152">`[RuleName <String>]`: Beállítja vagy beállítja a tűzfalszabályok nevét.</span><span class="sxs-lookup"><span data-stu-id="be1d8-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="be1d8-153">`[StartIPAddress <String>]`: A tűzfalszabály tartományának kezdő IP-címét kapja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="be1d8-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="be1d8-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be1d8-154">RELATED LINKS</span></span>

