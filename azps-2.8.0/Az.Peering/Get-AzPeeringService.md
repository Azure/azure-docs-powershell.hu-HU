---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: b2ebc3e91f08c2aa33853c8a90c929b31877a014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838436"
---
# <span data-ttu-id="707c8-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="707c8-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="707c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="707c8-102">SYNOPSIS</span></span>
<span data-ttu-id="707c8-103">Megtudhatja, hogy egyetlen objektumhoz tartozó társközi szolgáltatási objektumok listája</span><span class="sxs-lookup"><span data-stu-id="707c8-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="707c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="707c8-104">SYNTAX</span></span>

### <span data-ttu-id="707c8-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="707c8-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="707c8-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="707c8-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="707c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="707c8-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="707c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="707c8-108">DESCRIPTION</span></span>
<span data-ttu-id="707c8-109">Az előfizetéshez kapcsolódó szolgáltatások megkeresése</span><span class="sxs-lookup"><span data-stu-id="707c8-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="707c8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="707c8-110">EXAMPLES</span></span>

### <span data-ttu-id="707c8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="707c8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="707c8-112">Egy erőforráscsoport számára Kinyer egy egyenrangú szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="707c8-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="707c8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="707c8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="707c8-114">Egy erőforráscsoport és egy név társítására szolgáló szolgáltatás lekérdezése</span><span class="sxs-lookup"><span data-stu-id="707c8-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="707c8-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="707c8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="707c8-116">Erőforrás-azonosítóval rendelkező társközi szolgáltatás lekérdezése</span><span class="sxs-lookup"><span data-stu-id="707c8-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="707c8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="707c8-117">PARAMETERS</span></span>

### <span data-ttu-id="707c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707c8-118">-DefaultProfile</span></span>
<span data-ttu-id="707c8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="707c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707c8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="707c8-120">-Name</span></span>
<span data-ttu-id="707c8-121">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="707c8-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="707c8-123">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="707c8-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707c8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="707c8-124">-ResourceId</span></span>
<span data-ttu-id="707c8-125">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="707c8-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707c8-126">CommonParameters</span></span>
<span data-ttu-id="707c8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="707c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707c8-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="707c8-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707c8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="707c8-129">INPUTS</span></span>

### <span data-ttu-id="707c8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="707c8-130">System.String</span></span>

## <span data-ttu-id="707c8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="707c8-131">OUTPUTS</span></span>

### <span data-ttu-id="707c8-132">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="707c8-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="707c8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="707c8-133">NOTES</span></span>

## <span data-ttu-id="707c8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="707c8-134">RELATED LINKS</span></span>
