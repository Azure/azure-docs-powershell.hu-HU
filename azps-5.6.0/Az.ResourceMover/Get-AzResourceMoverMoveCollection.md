---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000038"
---
# <span data-ttu-id="14aef-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="14aef-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="14aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14aef-102">SYNOPSIS</span></span>
<span data-ttu-id="14aef-103">Beveszi az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="14aef-103">Gets the move collection.</span></span>

## <span data-ttu-id="14aef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14aef-104">SYNTAX</span></span>

### <span data-ttu-id="14aef-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14aef-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="14aef-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="14aef-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14aef-107">Lista1</span><span class="sxs-lookup"><span data-stu-id="14aef-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="14aef-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14aef-108">DESCRIPTION</span></span>
<span data-ttu-id="14aef-109">Beveszi az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="14aef-109">Gets the move collection.</span></span>

## <span data-ttu-id="14aef-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14aef-110">EXAMPLES</span></span>

### <span data-ttu-id="14aef-111">1. példa: Az előfizetés összes áthelyezési gyűjteményének részletei</span><span class="sxs-lookup"><span data-stu-id="14aef-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="14aef-112">Részleteket olvashat az előfizetésben elérhető Összes Áthelyezés gyűjteményről.</span><span class="sxs-lookup"><span data-stu-id="14aef-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="14aef-113">2. példa: A gyűjtemény áthelyezése az előfizetésben megadott áthelyezési gyűjteménynévvel</span><span class="sxs-lookup"><span data-stu-id="14aef-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="14aef-114">Részleteket olvashat az Áthelyezés gyűjteményről, az előfizetésben megadott áthelyezési gyűjteménynévvel.</span><span class="sxs-lookup"><span data-stu-id="14aef-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="14aef-115">3. példa: Az Áthelyezés gyűjtemény részleteinek megtekintése egy adott erőforráscsoportnévvel az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="14aef-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="14aef-116">A Gyűjtemény áthelyezése az előfizetésben megadott erőforráscsoportnévvel</span><span class="sxs-lookup"><span data-stu-id="14aef-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="14aef-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14aef-117">PARAMETERS</span></span>

### <span data-ttu-id="14aef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14aef-118">-DefaultProfile</span></span>
<span data-ttu-id="14aef-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14aef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14aef-120">-Name</span><span class="sxs-lookup"><span data-stu-id="14aef-120">-Name</span></span>
<span data-ttu-id="14aef-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="14aef-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14aef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14aef-122">-ResourceGroupName</span></span>
<span data-ttu-id="14aef-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14aef-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14aef-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14aef-124">-SubscriptionId</span></span>
<span data-ttu-id="14aef-125">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14aef-125">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14aef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14aef-126">CommonParameters</span></span>
<span data-ttu-id="14aef-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14aef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14aef-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14aef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14aef-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14aef-129">INPUTS</span></span>

## <span data-ttu-id="14aef-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14aef-130">OUTPUTS</span></span>

### <span data-ttu-id="14aef-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="14aef-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="14aef-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14aef-132">NOTES</span></span>

<span data-ttu-id="14aef-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="14aef-133">ALIASES</span></span>

## <span data-ttu-id="14aef-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14aef-134">RELATED LINKS</span></span>

