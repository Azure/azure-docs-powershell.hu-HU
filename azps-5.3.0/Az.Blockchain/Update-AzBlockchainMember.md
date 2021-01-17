---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478085"
---
# <span data-ttu-id="5ce10-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="5ce10-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="5ce10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ce10-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce10-103">Blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="5ce10-103">Update a blockchain member.</span></span>

## <span data-ttu-id="5ce10-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ce10-104">SYNTAX</span></span>

### <span data-ttu-id="5ce10-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ce10-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce10-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5ce10-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce10-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ce10-107">DESCRIPTION</span></span>
<span data-ttu-id="5ce10-108">Blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="5ce10-108">Update a blockchain member.</span></span>

## <span data-ttu-id="5ce10-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ce10-109">EXAMPLES</span></span>

### <span data-ttu-id="5ce10-110">1. példa: Blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="5ce10-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="5ce10-111">Ez a parancs frissíti a blockchain egyik tagját.</span><span class="sxs-lookup"><span data-stu-id="5ce10-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="5ce10-112">2. példa: Blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="5ce10-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="5ce10-113">Ez a parancs frissíti a blockchain egyik tagját.</span><span class="sxs-lookup"><span data-stu-id="5ce10-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="5ce10-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ce10-114">PARAMETERS</span></span>

### <span data-ttu-id="5ce10-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="5ce10-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="5ce10-116">Beállítja a felügyelt consortium felügyeleti fiók jelszavát.</span><span class="sxs-lookup"><span data-stu-id="5ce10-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="5ce10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce10-117">-DefaultProfile</span></span>
<span data-ttu-id="5ce10-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ce10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce10-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ce10-119">-FirewallRule</span></span>
<span data-ttu-id="5ce10-120">Beállítja vagy beállítja a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="5ce10-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="5ce10-121">A felépítéséről a NOTES (JEGYZETEK) szakaszban láthatja a FIREWALLRULE tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="5ce10-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ce10-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce10-122">-InputObject</span></span>
<span data-ttu-id="5ce10-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5ce10-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ce10-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5ce10-124">-Name</span></span>
<span data-ttu-id="5ce10-125">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="5ce10-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce10-126">-Password</span><span class="sxs-lookup"><span data-stu-id="5ce10-126">-Password</span></span>
<span data-ttu-id="5ce10-127">Beállítja a tranzakciós csomópont dns-végpontjának alapvető hitelesítésjelszóját.</span><span class="sxs-lookup"><span data-stu-id="5ce10-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="5ce10-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce10-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ce10-129">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ce10-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5ce10-130">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5ce10-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5ce10-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ce10-131">-SubscriptionId</span></span>
<span data-ttu-id="5ce10-132">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="5ce10-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ce10-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="5ce10-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ce10-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ce10-134">-Tag</span></span>
<span data-ttu-id="5ce10-135">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="5ce10-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="5ce10-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ce10-136">-Confirm</span></span>
<span data-ttu-id="5ce10-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ce10-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce10-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce10-138">-WhatIf</span></span>
<span data-ttu-id="5ce10-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ce10-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce10-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ce10-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce10-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce10-141">CommonParameters</span></span>
<span data-ttu-id="5ce10-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce10-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce10-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ce10-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce10-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ce10-144">INPUTS</span></span>

### <span data-ttu-id="5ce10-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="5ce10-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="5ce10-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ce10-146">OUTPUTS</span></span>

### <span data-ttu-id="5ce10-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="5ce10-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="5ce10-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ce10-148">NOTES</span></span>

<span data-ttu-id="5ce10-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5ce10-149">ALIASES</span></span>

<span data-ttu-id="5ce10-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5ce10-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ce10-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5ce10-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ce10-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ce10-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ce10-153">FIREWALLRULE <IFirewallRule[]>: Beállítja vagy beállítja a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="5ce10-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="5ce10-154">`[EndIPAddress <String>]`: Beállítja vagy beállítja a tűzfalszabály-tartomány IP-címét.</span><span class="sxs-lookup"><span data-stu-id="5ce10-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="5ce10-155">`[RuleName <String>]`: Beállítja vagy beállítja a tűzfalszabályok nevét.</span><span class="sxs-lookup"><span data-stu-id="5ce10-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="5ce10-156">`[StartIPAddress <String>]`: A tűzfalszabály tartományának kezdő IP-címét kapja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="5ce10-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="5ce10-157">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5ce10-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ce10-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="5ce10-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="5ce10-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5ce10-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ce10-160">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="5ce10-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="5ce10-161">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="5ce10-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="5ce10-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ce10-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5ce10-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="5ce10-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5ce10-164">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5ce10-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="5ce10-165">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="5ce10-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="5ce10-166">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="5ce10-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="5ce10-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ce10-167">RELATED LINKS</span></span>

