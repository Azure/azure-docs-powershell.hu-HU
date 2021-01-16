---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363186"
---
# <span data-ttu-id="ebc72-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="ebc72-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="ebc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc72-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc72-103">Frissítse a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ebc72-103">Update the transaction node.</span></span>

## <span data-ttu-id="ebc72-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebc72-104">SYNTAX</span></span>

### <span data-ttu-id="ebc72-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebc72-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebc72-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ebc72-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ebc72-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebc72-107">DESCRIPTION</span></span>
<span data-ttu-id="ebc72-108">Frissítse a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ebc72-108">Update the transaction node.</span></span>

## <span data-ttu-id="ebc72-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebc72-109">EXAMPLES</span></span>

### <span data-ttu-id="ebc72-110">1. példa: Transzcation csomópont frissítése</span><span class="sxs-lookup"><span data-stu-id="ebc72-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="ebc72-111">Ez a parancs frissíti a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ebc72-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="ebc72-112">2. példa: Transzcation csomópont frissítése</span><span class="sxs-lookup"><span data-stu-id="ebc72-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="ebc72-113">Ez a parancs frissíti a tranzakciós csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ebc72-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="ebc72-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebc72-114">PARAMETERS</span></span>

### <span data-ttu-id="ebc72-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="ebc72-115">-BlockchainMemberName</span></span>
<span data-ttu-id="ebc72-116">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="ebc72-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="ebc72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc72-117">-DefaultProfile</span></span>
<span data-ttu-id="ebc72-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebc72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc72-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebc72-119">-FirewallRule</span></span>
<span data-ttu-id="ebc72-120">Beállítja vagy beállítja a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="ebc72-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="ebc72-121">A felépítéséről a NOTES (JEGYZETEK) szakaszban láthatja a FIREWALLRULE tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="ebc72-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ebc72-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc72-122">-InputObject</span></span>
<span data-ttu-id="ebc72-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ebc72-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ebc72-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ebc72-124">-Name</span></span>
<span data-ttu-id="ebc72-125">Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="ebc72-125">Transaction node name.</span></span>

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

### <span data-ttu-id="ebc72-126">-Password</span><span class="sxs-lookup"><span data-stu-id="ebc72-126">-Password</span></span>
<span data-ttu-id="ebc72-127">Beállítja a tranzakciós csomópont dns-végpontjának alapvető hitelesítésjelszóját.</span><span class="sxs-lookup"><span data-stu-id="ebc72-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="ebc72-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc72-128">-ResourceGroupName</span></span>
<span data-ttu-id="ebc72-129">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebc72-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ebc72-130">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="ebc72-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ebc72-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebc72-131">-SubscriptionId</span></span>
<span data-ttu-id="ebc72-132">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="ebc72-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ebc72-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="ebc72-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ebc72-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc72-134">-Confirm</span></span>
<span data-ttu-id="ebc72-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ebc72-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc72-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc72-136">-WhatIf</span></span>
<span data-ttu-id="ebc72-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ebc72-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc72-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebc72-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc72-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc72-139">CommonParameters</span></span>
<span data-ttu-id="ebc72-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc72-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc72-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebc72-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc72-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc72-142">INPUTS</span></span>

### <span data-ttu-id="ebc72-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="ebc72-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="ebc72-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc72-144">OUTPUTS</span></span>

### <span data-ttu-id="ebc72-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="ebc72-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="ebc72-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebc72-146">NOTES</span></span>

<span data-ttu-id="ebc72-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ebc72-147">ALIASES</span></span>

<span data-ttu-id="ebc72-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ebc72-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ebc72-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ebc72-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebc72-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ebc72-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ebc72-151">FIREWALLRULE <IFirewallRule[]>: Beállítja vagy beállítja a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="ebc72-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="ebc72-152">`[EndIPAddress <String>]`: Beállítja vagy beállítja a tűzfalszabály-tartomány IP-címét.</span><span class="sxs-lookup"><span data-stu-id="ebc72-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="ebc72-153">`[RuleName <String>]`: Beállítja vagy beállítja a tűzfalszabályok nevét.</span><span class="sxs-lookup"><span data-stu-id="ebc72-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="ebc72-154">`[StartIPAddress <String>]`: A tűzfalszabály tartományának kezdő IP-címét kapja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="ebc72-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="ebc72-155">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ebc72-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebc72-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="ebc72-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="ebc72-157">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ebc72-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebc72-158">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="ebc72-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="ebc72-159">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="ebc72-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="ebc72-160">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebc72-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ebc72-161">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="ebc72-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ebc72-162">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ebc72-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ebc72-163">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="ebc72-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="ebc72-164">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="ebc72-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="ebc72-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebc72-165">RELATED LINKS</span></span>

