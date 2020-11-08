---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186418"
---
# <span data-ttu-id="4f35f-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="4f35f-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="4f35f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f35f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f35f-103">Blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="4f35f-103">Update a blockchain member.</span></span>

## <span data-ttu-id="4f35f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f35f-104">SYNTAX</span></span>

### <span data-ttu-id="4f35f-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f35f-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4f35f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4f35f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4f35f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f35f-107">DESCRIPTION</span></span>
<span data-ttu-id="4f35f-108">Blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="4f35f-108">Update a blockchain member.</span></span>

## <span data-ttu-id="4f35f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4f35f-109">EXAMPLES</span></span>

### <span data-ttu-id="4f35f-110">1. példa: blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="4f35f-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="4f35f-111">Ez a parancs egy blockchain-tagot frissít.</span><span class="sxs-lookup"><span data-stu-id="4f35f-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="4f35f-112">2. példa: blockchain-tag frissítése</span><span class="sxs-lookup"><span data-stu-id="4f35f-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="4f35f-113">Ez a parancs egy blockchain-tagot frissít.</span><span class="sxs-lookup"><span data-stu-id="4f35f-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="4f35f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f35f-114">PARAMETERS</span></span>

### <span data-ttu-id="4f35f-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="4f35f-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="4f35f-116">A felügyelt konzorcium-kezelési fiók jelszavának megadása</span><span class="sxs-lookup"><span data-stu-id="4f35f-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="4f35f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f35f-117">-DefaultProfile</span></span>
<span data-ttu-id="4f35f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f35f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f35f-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="4f35f-119">-FirewallRule</span></span>
<span data-ttu-id="4f35f-120">A tűzfalszabályok beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="4f35f-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="4f35f-121">A kivitelezéshez tekintse meg a FIREWALLRULE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4f35f-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f35f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f35f-122">-InputObject</span></span>
<span data-ttu-id="4f35f-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f35f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f35f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4f35f-124">-Name</span></span>
<span data-ttu-id="4f35f-125">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="4f35f-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="4f35f-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="4f35f-126">-Password</span></span>
<span data-ttu-id="4f35f-127">A Transaction node (DNS-végpont) alapvető hitelesítő jelszavának megadása</span><span class="sxs-lookup"><span data-stu-id="4f35f-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="4f35f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f35f-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f35f-129">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f35f-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4f35f-130">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="4f35f-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4f35f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f35f-131">-SubscriptionId</span></span>
<span data-ttu-id="4f35f-132">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="4f35f-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4f35f-133">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="4f35f-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4f35f-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="4f35f-134">-Tag</span></span>
<span data-ttu-id="4f35f-135">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcspárt tartalmazó párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="4f35f-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="4f35f-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f35f-136">-Confirm</span></span>
<span data-ttu-id="4f35f-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f35f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f35f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f35f-138">-WhatIf</span></span>
<span data-ttu-id="4f35f-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f35f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f35f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f35f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f35f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f35f-141">CommonParameters</span></span>
<span data-ttu-id="4f35f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f35f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f35f-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f35f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f35f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f35f-144">INPUTS</span></span>

### <span data-ttu-id="4f35f-145">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="4f35f-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="4f35f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f35f-146">OUTPUTS</span></span>

### <span data-ttu-id="4f35f-147">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="4f35f-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="4f35f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f35f-148">NOTES</span></span>

<span data-ttu-id="4f35f-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4f35f-149">ALIASES</span></span>

<span data-ttu-id="4f35f-150">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="4f35f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f35f-151">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4f35f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f35f-152">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4f35f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f35f-153">FIREWALLRULE <IFirewallRule [] >: beolvassa vagy beállítja a tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="4f35f-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="4f35f-154">`[EndIPAddress <String>]`: A tűzfalszabály-tartományok végpontjának IP-címét adja meg vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="4f35f-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="4f35f-155">`[RuleName <String>]`: A tűzfalszabályok nevének beírása vagy bekapcsolása.</span><span class="sxs-lookup"><span data-stu-id="4f35f-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="4f35f-156">`[StartIPAddress <String>]`: Beilleszti vagy beállítja a tűzfalszabály-tartományok kezdő IP-címét.</span><span class="sxs-lookup"><span data-stu-id="4f35f-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="4f35f-157">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="4f35f-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f35f-158">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="4f35f-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="4f35f-159">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4f35f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f35f-160">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="4f35f-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="4f35f-161">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="4f35f-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="4f35f-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f35f-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4f35f-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="4f35f-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4f35f-164">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="4f35f-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="4f35f-165">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="4f35f-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="4f35f-166">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="4f35f-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="4f35f-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f35f-167">RELATED LINKS</span></span>

