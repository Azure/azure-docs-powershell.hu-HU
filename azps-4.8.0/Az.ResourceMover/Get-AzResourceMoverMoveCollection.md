---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182898"
---
# <span data-ttu-id="c8add-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c8add-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="c8add-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8add-102">SYNOPSIS</span></span>
<span data-ttu-id="c8add-103">Megkapja az áthelyezés gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="c8add-103">Gets the move collection.</span></span>

## <span data-ttu-id="c8add-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8add-104">SYNTAX</span></span>

### <span data-ttu-id="c8add-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8add-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8add-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c8add-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8add-107">Lista1</span><span class="sxs-lookup"><span data-stu-id="c8add-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c8add-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8add-108">DESCRIPTION</span></span>
<span data-ttu-id="c8add-109">Megkapja az áthelyezés gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="c8add-109">Gets the move collection.</span></span>

## <span data-ttu-id="c8add-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c8add-110">EXAMPLES</span></span>

### <span data-ttu-id="c8add-111">1. példa: az előfizetésben lévő összes áthelyezési gyűjtemény részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="c8add-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="c8add-112">Az előfizetésben az áthelyezési gyűjtemények részletei című témakörben tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="c8add-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="c8add-113">2. példa: az előfizetésben megadott áthelyezési gyűjtemény nevének megtekintése a gyűjteményben</span><span class="sxs-lookup"><span data-stu-id="c8add-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="c8add-114">Bemutatjuk a gyűjtemény áthelyezésével kapcsolatos részleteket az előfizetésben megadott áthelyezési gyűjtemény nevével.</span><span class="sxs-lookup"><span data-stu-id="c8add-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="c8add-115">3. példa: a gyűjtemény áthelyezése az előfizetésben megadott erőforráscsoport nevével</span><span class="sxs-lookup"><span data-stu-id="c8add-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="c8add-116">Az előfizetésben megadott erőforráscsoport nevével megtudhatja, hogy miként helyezheti át a gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="c8add-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="c8add-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8add-117">PARAMETERS</span></span>

### <span data-ttu-id="c8add-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8add-118">-DefaultProfile</span></span>
<span data-ttu-id="c8add-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8add-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8add-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8add-120">-Name</span></span>
<span data-ttu-id="c8add-121">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c8add-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c8add-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8add-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8add-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c8add-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c8add-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8add-124">-SubscriptionId</span></span>
<span data-ttu-id="c8add-125">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="c8add-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="c8add-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8add-126">CommonParameters</span></span>
<span data-ttu-id="c8add-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8add-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8add-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8add-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8add-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8add-129">INPUTS</span></span>

## <span data-ttu-id="c8add-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8add-130">OUTPUTS</span></span>

### <span data-ttu-id="c8add-131">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c8add-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="c8add-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8add-132">NOTES</span></span>

<span data-ttu-id="c8add-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c8add-133">ALIASES</span></span>

## <span data-ttu-id="c8add-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8add-134">RELATED LINKS</span></span>

