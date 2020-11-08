---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025759"
---
# <span data-ttu-id="bbf37-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="bbf37-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="bbf37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbf37-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf37-103">Ismerje meg a tranzakció csomópont részleteit.</span><span class="sxs-lookup"><span data-stu-id="bbf37-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="bbf37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbf37-104">SYNTAX</span></span>

### <span data-ttu-id="bbf37-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bbf37-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bbf37-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbf37-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bbf37-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bbf37-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbf37-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbf37-108">DESCRIPTION</span></span>
<span data-ttu-id="bbf37-109">Ismerje meg a tranzakció csomópont részleteit.</span><span class="sxs-lookup"><span data-stu-id="bbf37-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="bbf37-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bbf37-110">EXAMPLES</span></span>

### <span data-ttu-id="bbf37-111">1. példa: a blockchain-tagok listázási tranzakciós csomópontjai</span><span class="sxs-lookup"><span data-stu-id="bbf37-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="bbf37-112">Ez a parancs felsorolja a blockchain-tagok tranzakciós csomópontját.</span><span class="sxs-lookup"><span data-stu-id="bbf37-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="bbf37-113">2. példa: tranzakció-csomópont beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbf37-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="bbf37-114">Ez a parancs a tranzakció csomópontot kapja.</span><span class="sxs-lookup"><span data-stu-id="bbf37-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="bbf37-115">3. példa: tranzakciós csomópont beszerzése</span><span class="sxs-lookup"><span data-stu-id="bbf37-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="bbf37-116">Ez a parancs a tranzakció csomópontot kapja.</span><span class="sxs-lookup"><span data-stu-id="bbf37-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="bbf37-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbf37-117">PARAMETERS</span></span>

### <span data-ttu-id="bbf37-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="bbf37-118">-BlockchainMemberName</span></span>
<span data-ttu-id="bbf37-119">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="bbf37-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf37-120">-DefaultProfile</span></span>
<span data-ttu-id="bbf37-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbf37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf37-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbf37-122">-InputObject</span></span>
<span data-ttu-id="bbf37-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bbf37-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf37-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bbf37-124">-Name</span></span>
<span data-ttu-id="bbf37-125">A tranzakció csomópontjának neve</span><span class="sxs-lookup"><span data-stu-id="bbf37-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf37-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf37-126">-ResourceGroupName</span></span>
<span data-ttu-id="bbf37-127">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bbf37-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="bbf37-128">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="bbf37-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf37-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbf37-129">-SubscriptionId</span></span>
<span data-ttu-id="bbf37-130">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="bbf37-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="bbf37-131">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="bbf37-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf37-132">CommonParameters</span></span>
<span data-ttu-id="bbf37-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbf37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf37-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bbf37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf37-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbf37-135">INPUTS</span></span>

### <span data-ttu-id="bbf37-136">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="bbf37-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="bbf37-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbf37-137">OUTPUTS</span></span>

### <span data-ttu-id="bbf37-138">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="bbf37-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="bbf37-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbf37-139">NOTES</span></span>

<span data-ttu-id="bbf37-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bbf37-140">ALIASES</span></span>

<span data-ttu-id="bbf37-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="bbf37-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbf37-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="bbf37-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbf37-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="bbf37-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbf37-144">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="bbf37-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbf37-145">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="bbf37-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="bbf37-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bbf37-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbf37-147">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="bbf37-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="bbf37-148">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="bbf37-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="bbf37-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bbf37-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="bbf37-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="bbf37-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="bbf37-151">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="bbf37-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="bbf37-152">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="bbf37-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="bbf37-153">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="bbf37-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="bbf37-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbf37-154">RELATED LINKS</span></span>

