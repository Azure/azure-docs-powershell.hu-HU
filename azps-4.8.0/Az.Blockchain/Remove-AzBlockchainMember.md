---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024866"
---
# <span data-ttu-id="9c0b6-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="9c0b6-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="9c0b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0b6-103">Blockchain-tag törlése</span><span class="sxs-lookup"><span data-stu-id="9c0b6-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="9c0b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c0b6-104">SYNTAX</span></span>

### <span data-ttu-id="9c0b6-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c0b6-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c0b6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c0b6-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c0b6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c0b6-107">DESCRIPTION</span></span>
<span data-ttu-id="9c0b6-108">Blockchain-tag törlése</span><span class="sxs-lookup"><span data-stu-id="9c0b6-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="9c0b6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c0b6-109">EXAMPLES</span></span>

### <span data-ttu-id="9c0b6-110">1. példa: blockchain-tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9c0b6-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="9c0b6-111">Ez a parancs eltávolítja a blockchain tagot.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="9c0b6-112">2. példa: blockchain tagok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9c0b6-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="9c0b6-113">Ez a parancs eltávolítja a blockchain tagot.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="9c0b6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c0b6-114">PARAMETERS</span></span>

### <span data-ttu-id="9c0b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c0b6-115">-AsJob</span></span>
<span data-ttu-id="9c0b6-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9c0b6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9c0b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c0b6-117">-DefaultProfile</span></span>
<span data-ttu-id="9c0b6-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c0b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c0b6-119">-InputObject</span></span>
<span data-ttu-id="9c0b6-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c0b6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c0b6-121">-Name</span></span>
<span data-ttu-id="9c0b6-122">Blockchain tag neve</span><span class="sxs-lookup"><span data-stu-id="9c0b6-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c0b6-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="9c0b6-123">-NoWait</span></span>
<span data-ttu-id="9c0b6-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9c0b6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9c0b6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c0b6-125">-PassThru</span></span>
<span data-ttu-id="9c0b6-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="9c0b6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9c0b6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c0b6-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c0b6-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9c0b6-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c0b6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c0b6-130">-SubscriptionId</span></span>
<span data-ttu-id="9c0b6-131">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9c0b6-132">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c0b6-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c0b6-133">-Confirm</span></span>
<span data-ttu-id="9c0b6-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c0b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c0b6-135">-WhatIf</span></span>
<span data-ttu-id="9c0b6-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c0b6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c0b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0b6-138">CommonParameters</span></span>
<span data-ttu-id="9c0b6-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c0b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0b6-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0b6-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c0b6-141">INPUTS</span></span>

### <span data-ttu-id="9c0b6-142">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="9c0b6-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="9c0b6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c0b6-143">OUTPUTS</span></span>

### <span data-ttu-id="9c0b6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c0b6-144">System.Boolean</span></span>

## <span data-ttu-id="9c0b6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c0b6-145">NOTES</span></span>

<span data-ttu-id="9c0b6-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9c0b6-146">ALIASES</span></span>

<span data-ttu-id="9c0b6-147">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="9c0b6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c0b6-148">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c0b6-149">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c0b6-150">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9c0b6-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c0b6-151">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="9c0b6-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9c0b6-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c0b6-153">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="9c0b6-154">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="9c0b6-155">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9c0b6-156">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9c0b6-157">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9c0b6-158">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="9c0b6-159">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="9c0b6-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="9c0b6-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c0b6-160">RELATED LINKS</span></span>

