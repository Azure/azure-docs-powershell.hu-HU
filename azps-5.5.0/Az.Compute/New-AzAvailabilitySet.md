---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148891"
---
# <span data-ttu-id="10e42-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10e42-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="10e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e42-102">SYNOPSIS</span></span>
<span data-ttu-id="10e42-103">Létrehozza az Azure rendelkezésre állási készletét.</span><span class="sxs-lookup"><span data-stu-id="10e42-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="10e42-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10e42-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10e42-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10e42-105">DESCRIPTION</span></span>
<span data-ttu-id="10e42-106">A **New-AzAvailabilitySet** parancsmag létrehoz egy Azure rendelkezésre állási készletet.</span><span class="sxs-lookup"><span data-stu-id="10e42-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="10e42-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10e42-107">EXAMPLES</span></span>

### <span data-ttu-id="10e42-108">1. példa: Elérhetőségi készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="10e42-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="10e42-109">Ez a parancs létrehoz egy AvailabilitySet03 nevű rendelkezésre állási készletet az Erőforráscsoport11 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="10e42-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="10e42-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10e42-110">PARAMETERS</span></span>

### <span data-ttu-id="10e42-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10e42-111">-AsJob</span></span>
<span data-ttu-id="10e42-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="10e42-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="10e42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e42-113">-DefaultProfile</span></span>
<span data-ttu-id="10e42-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10e42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e42-115">-Location</span><span class="sxs-lookup"><span data-stu-id="10e42-115">-Location</span></span>
<span data-ttu-id="10e42-116">Az elérhetőségi készlet helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="10e42-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="10e42-117">-Name</span><span class="sxs-lookup"><span data-stu-id="10e42-117">-Name</span></span>
<span data-ttu-id="10e42-118">Megadja az elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="10e42-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="10e42-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="10e42-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="10e42-120">A platformhiba-tartomány számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10e42-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="10e42-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="10e42-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="10e42-122">A platformfrissítési tartomány számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="10e42-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="10e42-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="10e42-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="10e42-124">Az elérhetőségi készlethez használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="10e42-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="10e42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e42-125">-ResourceGroupName</span></span>
<span data-ttu-id="10e42-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10e42-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10e42-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="10e42-127">-Sku</span></span>
<span data-ttu-id="10e42-128">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="10e42-128">The Name of Sku.</span></span>
<span data-ttu-id="10e42-129">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="10e42-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10e42-130">Igazított: Felügyelt lemez esetén</span><span class="sxs-lookup"><span data-stu-id="10e42-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="10e42-131">Klasszikus: Nemmanaged lemez esetén</span><span class="sxs-lookup"><span data-stu-id="10e42-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="10e42-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="10e42-132">-Tag</span></span>
<span data-ttu-id="10e42-133">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="10e42-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="10e42-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e42-134">CommonParameters</span></span>
<span data-ttu-id="10e42-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e42-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e42-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10e42-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e42-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10e42-137">INPUTS</span></span>

### <span data-ttu-id="10e42-138">System.String</span><span class="sxs-lookup"><span data-stu-id="10e42-138">System.String</span></span>

### <span data-ttu-id="10e42-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10e42-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="10e42-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10e42-140">OUTPUTS</span></span>

### <span data-ttu-id="10e42-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10e42-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="10e42-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10e42-142">NOTES</span></span>

## <span data-ttu-id="10e42-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10e42-143">RELATED LINKS</span></span>

[<span data-ttu-id="10e42-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10e42-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="10e42-145">Remove-AzavailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10e42-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


