---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480997"
---
# <span data-ttu-id="0eb34-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="0eb34-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="0eb34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb34-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb34-103">A tranzakciós csomópont részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="0eb34-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="0eb34-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0eb34-104">SYNTAX</span></span>

### <span data-ttu-id="0eb34-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0eb34-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0eb34-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="0eb34-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0eb34-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0eb34-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb34-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0eb34-108">DESCRIPTION</span></span>
<span data-ttu-id="0eb34-109">A tranzakciós csomópont részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="0eb34-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="0eb34-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0eb34-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb34-111">1. példa: Tranzakciós csomópontok listása egy blockchain taghoz</span><span class="sxs-lookup"><span data-stu-id="0eb34-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="0eb34-112">Ez a parancs felsorolja egy blockchain-tag tranzakciós csomópontját.</span><span class="sxs-lookup"><span data-stu-id="0eb34-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="0eb34-113">2. példa: Tranzakciós csomópont lekérte</span><span class="sxs-lookup"><span data-stu-id="0eb34-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="0eb34-114">Ez a parancs tranzakciós csomópontot kap.</span><span class="sxs-lookup"><span data-stu-id="0eb34-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="0eb34-115">3. példa: Tranzakciós csomópont lekérte</span><span class="sxs-lookup"><span data-stu-id="0eb34-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="0eb34-116">Ez a parancs tranzakciós csomópontot kap.</span><span class="sxs-lookup"><span data-stu-id="0eb34-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="0eb34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb34-117">PARAMETERS</span></span>

### <span data-ttu-id="0eb34-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="0eb34-118">-BlockchainMemberName</span></span>
<span data-ttu-id="0eb34-119">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="0eb34-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="0eb34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb34-120">-DefaultProfile</span></span>
<span data-ttu-id="0eb34-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0eb34-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eb34-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb34-122">-InputObject</span></span>
<span data-ttu-id="0eb34-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0eb34-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0eb34-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0eb34-124">-Name</span></span>
<span data-ttu-id="0eb34-125">Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="0eb34-125">Transaction node name.</span></span>

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

### <span data-ttu-id="0eb34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb34-126">-ResourceGroupName</span></span>
<span data-ttu-id="0eb34-127">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0eb34-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0eb34-128">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="0eb34-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0eb34-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0eb34-129">-SubscriptionId</span></span>
<span data-ttu-id="0eb34-130">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="0eb34-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0eb34-131">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="0eb34-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0eb34-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb34-132">CommonParameters</span></span>
<span data-ttu-id="0eb34-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb34-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb34-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eb34-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb34-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0eb34-135">INPUTS</span></span>

### <span data-ttu-id="0eb34-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="0eb34-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="0eb34-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eb34-137">OUTPUTS</span></span>

### <span data-ttu-id="0eb34-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="0eb34-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="0eb34-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0eb34-139">NOTES</span></span>

<span data-ttu-id="0eb34-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0eb34-140">ALIASES</span></span>

<span data-ttu-id="0eb34-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0eb34-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0eb34-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0eb34-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0eb34-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0eb34-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0eb34-144">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0eb34-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0eb34-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="0eb34-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="0eb34-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0eb34-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0eb34-147">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="0eb34-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="0eb34-148">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="0eb34-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="0eb34-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0eb34-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0eb34-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="0eb34-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0eb34-151">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="0eb34-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="0eb34-152">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="0eb34-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="0eb34-153">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="0eb34-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="0eb34-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0eb34-154">RELATED LINKS</span></span>

