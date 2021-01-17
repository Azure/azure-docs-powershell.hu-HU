---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467210"
---
# <span data-ttu-id="744d0-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="744d0-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="744d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744d0-102">SYNOPSIS</span></span>
<span data-ttu-id="744d0-103">Beveszi az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="744d0-103">Gets the move collection.</span></span>

## <span data-ttu-id="744d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="744d0-104">SYNTAX</span></span>

### <span data-ttu-id="744d0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="744d0-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="744d0-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="744d0-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="744d0-107">Lista1</span><span class="sxs-lookup"><span data-stu-id="744d0-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="744d0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="744d0-108">DESCRIPTION</span></span>
<span data-ttu-id="744d0-109">Beveszi az áthelyezési gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="744d0-109">Gets the move collection.</span></span>

## <span data-ttu-id="744d0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="744d0-110">EXAMPLES</span></span>

### <span data-ttu-id="744d0-111">1. példa: Az előfizetés összes áthelyezési gyűjteményének részletei</span><span class="sxs-lookup"><span data-stu-id="744d0-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="744d0-112">Részleteket olvashat az előfizetésben elérhető Összes Áthelyezés gyűjteményről.</span><span class="sxs-lookup"><span data-stu-id="744d0-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="744d0-113">2. példa: A gyűjtemény áthelyezése az előfizetésben megadott áthelyezési gyűjteménynévvel</span><span class="sxs-lookup"><span data-stu-id="744d0-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="744d0-114">Részleteket olvashat az Áthelyezés gyűjteményről az előfizetésben megadott áthelyezési gyűjteménynévvel.</span><span class="sxs-lookup"><span data-stu-id="744d0-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="744d0-115">3. példa: Az Áthelyezés gyűjtemény részleteinek megtekintése egy adott erőforráscsoportnévvel az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="744d0-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="744d0-116">A Gyűjtemény áthelyezése az előfizetésben megadott erőforráscsoportnévvel</span><span class="sxs-lookup"><span data-stu-id="744d0-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="744d0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="744d0-117">PARAMETERS</span></span>

### <span data-ttu-id="744d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744d0-118">-DefaultProfile</span></span>
<span data-ttu-id="744d0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="744d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744d0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="744d0-120">-Name</span></span>
<span data-ttu-id="744d0-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="744d0-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="744d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="744d0-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="744d0-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="744d0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="744d0-124">-SubscriptionId</span></span>
<span data-ttu-id="744d0-125">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="744d0-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="744d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744d0-126">CommonParameters</span></span>
<span data-ttu-id="744d0-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744d0-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="744d0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744d0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="744d0-129">INPUTS</span></span>

## <span data-ttu-id="744d0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="744d0-130">OUTPUTS</span></span>

### <span data-ttu-id="744d0-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="744d0-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="744d0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="744d0-132">NOTES</span></span>

<span data-ttu-id="744d0-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="744d0-133">ALIASES</span></span>

## <span data-ttu-id="744d0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="744d0-134">RELATED LINKS</span></span>

