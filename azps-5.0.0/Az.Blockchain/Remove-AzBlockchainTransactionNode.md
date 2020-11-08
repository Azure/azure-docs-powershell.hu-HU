---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194811"
---
# <span data-ttu-id="5ba21-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="5ba21-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="5ba21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ba21-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba21-103">Törölje a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="5ba21-103">Delete the transaction node.</span></span>

## <span data-ttu-id="5ba21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ba21-104">SYNTAX</span></span>

### <span data-ttu-id="5ba21-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ba21-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5ba21-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ba21-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ba21-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ba21-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba21-108">Törölje a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="5ba21-108">Delete the transaction node.</span></span>

## <span data-ttu-id="5ba21-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5ba21-109">EXAMPLES</span></span>

### <span data-ttu-id="5ba21-110">1. példa: a tranzakciós csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5ba21-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="5ba21-111">Ez a parancs eltávolítja a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="5ba21-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="5ba21-112">2. példa: a tranzakciós csomópont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5ba21-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="5ba21-113">Ez a parancs eltávolítja a tranzakció csomópontot.</span><span class="sxs-lookup"><span data-stu-id="5ba21-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="5ba21-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ba21-114">PARAMETERS</span></span>

### <span data-ttu-id="5ba21-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ba21-115">-AsJob</span></span>
<span data-ttu-id="5ba21-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="5ba21-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5ba21-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="5ba21-117">-BlockchainMemberName</span></span>
<span data-ttu-id="5ba21-118">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="5ba21-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="5ba21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba21-119">-DefaultProfile</span></span>
<span data-ttu-id="5ba21-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ba21-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba21-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ba21-121">-InputObject</span></span>
<span data-ttu-id="5ba21-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ba21-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ba21-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ba21-123">-Name</span></span>
<span data-ttu-id="5ba21-124">A tranzakció csomópontjának neve</span><span class="sxs-lookup"><span data-stu-id="5ba21-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba21-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="5ba21-125">-NoWait</span></span>
<span data-ttu-id="5ba21-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="5ba21-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ba21-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ba21-127">-PassThru</span></span>
<span data-ttu-id="5ba21-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="5ba21-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ba21-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba21-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ba21-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ba21-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5ba21-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="5ba21-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5ba21-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ba21-132">-SubscriptionId</span></span>
<span data-ttu-id="5ba21-133">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="5ba21-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ba21-134">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="5ba21-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ba21-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ba21-135">-Confirm</span></span>
<span data-ttu-id="5ba21-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ba21-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba21-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba21-137">-WhatIf</span></span>
<span data-ttu-id="5ba21-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ba21-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba21-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ba21-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba21-140">CommonParameters</span></span>
<span data-ttu-id="5ba21-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ba21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba21-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5ba21-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba21-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ba21-143">INPUTS</span></span>

### <span data-ttu-id="5ba21-144">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="5ba21-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="5ba21-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ba21-145">OUTPUTS</span></span>

### <span data-ttu-id="5ba21-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ba21-146">System.Boolean</span></span>

## <span data-ttu-id="5ba21-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ba21-147">NOTES</span></span>

<span data-ttu-id="5ba21-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5ba21-148">ALIASES</span></span>

<span data-ttu-id="5ba21-149">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="5ba21-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ba21-150">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5ba21-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ba21-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5ba21-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ba21-152">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5ba21-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ba21-153">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="5ba21-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="5ba21-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5ba21-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ba21-155">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="5ba21-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="5ba21-156">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="5ba21-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="5ba21-157">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ba21-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5ba21-158">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="5ba21-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5ba21-159">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="5ba21-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="5ba21-160">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="5ba21-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="5ba21-161">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="5ba21-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="5ba21-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ba21-162">RELATED LINKS</span></span>

