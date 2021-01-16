---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352194"
---
# <span data-ttu-id="393c8-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="393c8-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="393c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="393c8-102">SYNOPSIS</span></span>
<span data-ttu-id="393c8-103">Részletek a blockchain tagról.</span><span class="sxs-lookup"><span data-stu-id="393c8-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="393c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="393c8-104">SYNTAX</span></span>

### <span data-ttu-id="393c8-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="393c8-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="393c8-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="393c8-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="393c8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="393c8-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="393c8-108">Lista</span><span class="sxs-lookup"><span data-stu-id="393c8-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="393c8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="393c8-109">DESCRIPTION</span></span>
<span data-ttu-id="393c8-110">Részletek a blockchain tagról.</span><span class="sxs-lookup"><span data-stu-id="393c8-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="393c8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="393c8-111">EXAMPLES</span></span>

### <span data-ttu-id="393c8-112">1. példa: Listablokkchain-tagok listája</span><span class="sxs-lookup"><span data-stu-id="393c8-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="393c8-113">Ez a parancs felsorolja az előfizetésben a blockchain tagokat.</span><span class="sxs-lookup"><span data-stu-id="393c8-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="393c8-114">2. példa: Listablokkchain-tagok listája</span><span class="sxs-lookup"><span data-stu-id="393c8-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="393c8-115">Ez a parancs felsorolja egy erőforráscsoportban a blockchain tagokat.</span><span class="sxs-lookup"><span data-stu-id="393c8-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="393c8-116">3. példa: Blockchain-tag lekérte</span><span class="sxs-lookup"><span data-stu-id="393c8-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="393c8-117">Ez a parancs egy blockchain tagot kap egy erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="393c8-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="393c8-118">4. példa: Blockchain-tag lekérte</span><span class="sxs-lookup"><span data-stu-id="393c8-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="393c8-119">Ez a parancs egy blockchain tagot kap egy erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="393c8-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="393c8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="393c8-120">PARAMETERS</span></span>

### <span data-ttu-id="393c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393c8-121">-DefaultProfile</span></span>
<span data-ttu-id="393c8-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="393c8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393c8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="393c8-123">-InputObject</span></span>
<span data-ttu-id="393c8-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="393c8-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="393c8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="393c8-125">-Name</span></span>
<span data-ttu-id="393c8-126">Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="393c8-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="393c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="393c8-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="393c8-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="393c8-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="393c8-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="393c8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="393c8-130">-SubscriptionId</span></span>
<span data-ttu-id="393c8-131">A Microsoft Azure-előfizetést egyedileg azonosító előfizetésazonosítót kap.</span><span class="sxs-lookup"><span data-stu-id="393c8-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="393c8-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="393c8-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="393c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393c8-133">CommonParameters</span></span>
<span data-ttu-id="393c8-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393c8-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="393c8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393c8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="393c8-136">INPUTS</span></span>

### <span data-ttu-id="393c8-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="393c8-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="393c8-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="393c8-138">OUTPUTS</span></span>

### <span data-ttu-id="393c8-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="393c8-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="393c8-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="393c8-140">NOTES</span></span>

<span data-ttu-id="393c8-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="393c8-141">ALIASES</span></span>

<span data-ttu-id="393c8-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="393c8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="393c8-143">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="393c8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="393c8-144">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="393c8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="393c8-145">INPUTOBJECT: <IBlockchainIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="393c8-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="393c8-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span><span class="sxs-lookup"><span data-stu-id="393c8-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="393c8-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="393c8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="393c8-148">`[Location <String>]`: Hely neve.</span><span class="sxs-lookup"><span data-stu-id="393c8-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="393c8-149">`[OperationId <String>]`: Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="393c8-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="393c8-150">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="393c8-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="393c8-151">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="393c8-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="393c8-152">`[SubscriptionId <String>]`: Beveszi az előfizetés azonosítóját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="393c8-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="393c8-153">Az előfizetésazonosító minden szolgáltatási hívás URI-jának része.</span><span class="sxs-lookup"><span data-stu-id="393c8-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="393c8-154">`[TransactionNodeName <String>]`: Tranzakciós csomópont neve.</span><span class="sxs-lookup"><span data-stu-id="393c8-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="393c8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="393c8-155">RELATED LINKS</span></span>

