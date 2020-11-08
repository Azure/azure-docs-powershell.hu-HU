---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184028"
---
# <span data-ttu-id="8f993-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="8f993-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="8f993-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f993-102">SYNOPSIS</span></span>
<span data-ttu-id="8f993-103">Megkeresi az előfizetéshez tartozó társközi szolgáltatások előtagjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="8f993-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="8f993-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f993-104">SYNTAX</span></span>

### <span data-ttu-id="8f993-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f993-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f993-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8f993-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f993-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f993-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f993-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f993-108">DESCRIPTION</span></span>
<span data-ttu-id="8f993-109">A társas szolgáltatási objektumokra vonatkozó előtagok listája</span><span class="sxs-lookup"><span data-stu-id="8f993-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="8f993-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8f993-110">EXAMPLES</span></span>

### <span data-ttu-id="8f993-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8f993-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8f993-112">A csővezeték-parancsok alapján egy társközi szolgáltatás előtagjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8f993-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="8f993-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8f993-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8f993-114">Erőforrás-azonosítóval beolvashatja a társas szolgáltatások meghatározott előtagját.</span><span class="sxs-lookup"><span data-stu-id="8f993-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="8f993-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="8f993-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8f993-116">Erőforrás-azonosítóval beolvashatja a társas szolgáltatások meghatározott előtagját.</span><span class="sxs-lookup"><span data-stu-id="8f993-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="8f993-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="8f993-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8f993-118">A kibontott attribútumokat tartalmazó speciális előtagot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8f993-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="8f993-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f993-119">PARAMETERS</span></span>

### <span data-ttu-id="8f993-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f993-120">-DefaultProfile</span></span>
<span data-ttu-id="8f993-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f993-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f993-122">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="8f993-122">-Expand</span></span>
<span data-ttu-id="8f993-123">A társas szolgáltatások előtagjaként megjelenített események megtekintése</span><span class="sxs-lookup"><span data-stu-id="8f993-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="8f993-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f993-124">-Name</span></span>
<span data-ttu-id="8f993-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="8f993-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f993-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="8f993-126">-PeeringServiceName</span></span>
<span data-ttu-id="8f993-127">A társas szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="8f993-127">The peering service name.</span></span> <span data-ttu-id="8f993-128">New-AzPeeringService parancsmagot használhat új társközi szolgáltatáshoz vagy Get-AzPeeringService a listákhoz.</span><span class="sxs-lookup"><span data-stu-id="8f993-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f993-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="8f993-129">-PeeringServiceObject</span></span>
<span data-ttu-id="8f993-130">Get-AzPeeringService használata</span><span class="sxs-lookup"><span data-stu-id="8f993-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f993-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f993-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f993-132">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="8f993-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="8f993-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f993-133">-ResourceId</span></span>
<span data-ttu-id="8f993-134">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="8f993-134">The resource id string name.</span></span>

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

### <span data-ttu-id="8f993-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f993-135">CommonParameters</span></span>
<span data-ttu-id="8f993-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f993-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f993-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8f993-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f993-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f993-138">INPUTS</span></span>

### <span data-ttu-id="8f993-139">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="8f993-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="8f993-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8f993-140">System.String</span></span>

## <span data-ttu-id="8f993-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f993-141">OUTPUTS</span></span>

### <span data-ttu-id="8f993-142">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="8f993-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="8f993-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f993-143">NOTES</span></span>

## <span data-ttu-id="8f993-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f993-144">RELATED LINKS</span></span>
