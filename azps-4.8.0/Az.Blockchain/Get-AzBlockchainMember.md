---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024872"
---
# <span data-ttu-id="c5c85-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c5c85-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="c5c85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5c85-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c85-103">Információkat kaphat a blockchain-tagokról.</span><span class="sxs-lookup"><span data-stu-id="c5c85-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="c5c85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5c85-104">SYNTAX</span></span>

### <span data-ttu-id="c5c85-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5c85-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5c85-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c5c85-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5c85-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5c85-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5c85-108">Lista</span><span class="sxs-lookup"><span data-stu-id="c5c85-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5c85-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5c85-109">DESCRIPTION</span></span>
<span data-ttu-id="c5c85-110">Információkat kaphat a blockchain-tagokról.</span><span class="sxs-lookup"><span data-stu-id="c5c85-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="c5c85-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c5c85-111">EXAMPLES</span></span>

### <span data-ttu-id="c5c85-112">1. példa: a lista blockchain tagjai</span><span class="sxs-lookup"><span data-stu-id="c5c85-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c5c85-113">Ez a parancs az előfizetésben szereplő blockchain-tagokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="c5c85-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="c5c85-114">2. példa: a lista blockchain tagjai</span><span class="sxs-lookup"><span data-stu-id="c5c85-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c5c85-115">Ez a parancs egy erőforráscsoport alatti blockchain-tagokat sorol fel.</span><span class="sxs-lookup"><span data-stu-id="c5c85-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="c5c85-116">3. példa: blockchain-tag beszerzése</span><span class="sxs-lookup"><span data-stu-id="c5c85-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c5c85-117">Ez a parancs egy blockchain-tagot kap egy erőforráscsoport alá.</span><span class="sxs-lookup"><span data-stu-id="c5c85-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="c5c85-118">4. példa: blockchain-tag beszerzése</span><span class="sxs-lookup"><span data-stu-id="c5c85-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c5c85-119">Ez a parancs egy blockchain-tagot kap egy erőforráscsoport alá.</span><span class="sxs-lookup"><span data-stu-id="c5c85-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="c5c85-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5c85-120">PARAMETERS</span></span>

### <span data-ttu-id="c5c85-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c85-121">-DefaultProfile</span></span>
<span data-ttu-id="c5c85-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5c85-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5c85-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5c85-123">-InputObject</span></span>
<span data-ttu-id="c5c85-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c5c85-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c5c85-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5c85-125">-Name</span></span>
<span data-ttu-id="c5c85-126">Blockchain-tag neve</span><span class="sxs-lookup"><span data-stu-id="c5c85-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c85-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c85-127">-ResourceGroupName</span></span>
<span data-ttu-id="c5c85-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5c85-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c5c85-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="c5c85-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c5c85-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5c85-130">-SubscriptionId</span></span>
<span data-ttu-id="c5c85-131">Megkapja a Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="c5c85-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c5c85-132">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="c5c85-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c85-133">CommonParameters</span></span>
<span data-ttu-id="c5c85-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5c85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c85-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c5c85-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c85-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5c85-136">INPUTS</span></span>

### <span data-ttu-id="c5c85-137">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="c5c85-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c5c85-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5c85-138">OUTPUTS</span></span>

### <span data-ttu-id="c5c85-139">Microsoft. Azure. PowerShell. parancsmagok. Blockchain. modellek. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c5c85-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="c5c85-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5c85-140">NOTES</span></span>

<span data-ttu-id="c5c85-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c5c85-141">ALIASES</span></span>

<span data-ttu-id="c5c85-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c5c85-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5c85-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c5c85-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5c85-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c5c85-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5c85-145">INPUTOBJECT <IBlockchainIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c5c85-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c5c85-146">`[BlockchainMemberName <String>]`: Blockchain tag neve.</span><span class="sxs-lookup"><span data-stu-id="c5c85-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c5c85-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c5c85-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c5c85-148">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="c5c85-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c5c85-149">`[OperationId <String>]`: Műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="c5c85-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c5c85-150">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5c85-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c5c85-151">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="c5c85-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c5c85-152">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="c5c85-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c5c85-153">Az előfizetési azonosító az összes szolgáltatási hívás URI azonosítójának része.</span><span class="sxs-lookup"><span data-stu-id="c5c85-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c5c85-154">`[TransactionNodeName <String>]`: A tranzakció csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="c5c85-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c5c85-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5c85-155">RELATED LINKS</span></span>

