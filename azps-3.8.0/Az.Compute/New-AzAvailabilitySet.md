---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011479"
---
# <span data-ttu-id="4a0ba-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a0ba-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="4a0ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a0ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0ba-103">Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="4a0ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a0ba-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a0ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a0ba-105">DESCRIPTION</span></span>
<span data-ttu-id="4a0ba-106">A **New-AzAvailabilitySet** parancsmag egy Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="4a0ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a0ba-107">EXAMPLES</span></span>

### <span data-ttu-id="4a0ba-108">Példa 1: elérhetőségi halmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="4a0ba-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="4a0ba-109">Ez a parancs létrehoz egy AvailabilitySet03 nevű elérhetőségi készletet az ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4a0ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a0ba-110">PARAMETERS</span></span>

### <span data-ttu-id="4a0ba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a0ba-111">-AsJob</span></span>
<span data-ttu-id="4a0ba-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4a0ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0ba-113">-DefaultProfile</span></span>
<span data-ttu-id="4a0ba-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a0ba-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="4a0ba-115">-Location</span></span>
<span data-ttu-id="4a0ba-116">Az elérhetőségi halmaz helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a0ba-117">-Name</span></span>
<span data-ttu-id="4a0ba-118">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4a0ba-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4a0ba-120">A platform hibás tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="4a0ba-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="4a0ba-122">A platform Update domain count (platform frissítése) beállítás.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4a0ba-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4a0ba-124">Annak a közelségi helynek az erőforrás-azonosítója, amellyel az elérhetőségi készlet használható.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a0ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a0ba-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="4a0ba-127">-Sku</span></span>
<span data-ttu-id="4a0ba-128">Az SKU neve.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-128">The Name of Sku.</span></span>
<span data-ttu-id="4a0ba-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4a0ba-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a0ba-130">Igazítás: felügyelt lemezek esetén</span><span class="sxs-lookup"><span data-stu-id="4a0ba-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="4a0ba-131">Klasszikus: nem felügyelt lemezek esetén</span><span class="sxs-lookup"><span data-stu-id="4a0ba-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="4a0ba-132">-Tag</span></span>
<span data-ttu-id="4a0ba-133">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a0ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0ba-134">CommonParameters</span></span>
<span data-ttu-id="4a0ba-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a0ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0ba-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0ba-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a0ba-137">INPUTS</span></span>

### <span data-ttu-id="4a0ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4a0ba-138">System.String</span></span>

### <span data-ttu-id="4a0ba-139">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4a0ba-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4a0ba-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a0ba-140">OUTPUTS</span></span>

### <span data-ttu-id="4a0ba-141">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a0ba-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="4a0ba-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a0ba-142">NOTES</span></span>

## <span data-ttu-id="4a0ba-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a0ba-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a0ba-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a0ba-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="4a0ba-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4a0ba-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


