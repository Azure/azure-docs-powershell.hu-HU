---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: c34bbb3cfd753c48a961373a44dd1e9bb4302208
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671322"
---
# <span data-ttu-id="bc71a-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bc71a-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="bc71a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc71a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc71a-103">Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bc71a-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="bc71a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc71a-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc71a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc71a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc71a-106">A **New-AzAvailabilitySet** parancsmag egy Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bc71a-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="bc71a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc71a-107">EXAMPLES</span></span>

### <span data-ttu-id="bc71a-108">Példa 1: elérhetőségi halmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="bc71a-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="bc71a-109">Ez a parancs létrehoz egy AvailablitySet03 nevű elérhetőségi készletet az ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="bc71a-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="bc71a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc71a-110">PARAMETERS</span></span>

### <span data-ttu-id="bc71a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc71a-111">-AsJob</span></span>
<span data-ttu-id="bc71a-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="bc71a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bc71a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc71a-113">-DefaultProfile</span></span>
<span data-ttu-id="bc71a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc71a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc71a-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="bc71a-115">-Location</span></span>
<span data-ttu-id="bc71a-116">Az elérhetőségi halmaz helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc71a-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="bc71a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc71a-117">-Name</span></span>
<span data-ttu-id="bc71a-118">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc71a-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="bc71a-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="bc71a-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="bc71a-120">A platform hibás tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc71a-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="bc71a-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="bc71a-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="bc71a-122">A platform Update domain count (platform frissítése) beállítás.</span><span class="sxs-lookup"><span data-stu-id="bc71a-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="bc71a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc71a-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc71a-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc71a-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bc71a-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="bc71a-125">-Sku</span></span>
<span data-ttu-id="bc71a-126">Az SKU neve.</span><span class="sxs-lookup"><span data-stu-id="bc71a-126">The Name of Sku.</span></span>
<span data-ttu-id="bc71a-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bc71a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc71a-128">Igazítás: felügyelt lemezek esetén</span><span class="sxs-lookup"><span data-stu-id="bc71a-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="bc71a-129">Klasszikus: nem felügyelt lemezek esetén</span><span class="sxs-lookup"><span data-stu-id="bc71a-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="bc71a-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="bc71a-130">-Tag</span></span>
<span data-ttu-id="bc71a-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="bc71a-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="bc71a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc71a-132">CommonParameters</span></span>
<span data-ttu-id="bc71a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc71a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc71a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc71a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc71a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc71a-135">INPUTS</span></span>

### <span data-ttu-id="bc71a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bc71a-136">System.String</span></span>

### <span data-ttu-id="bc71a-137">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc71a-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bc71a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc71a-138">OUTPUTS</span></span>

### <span data-ttu-id="bc71a-139">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bc71a-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="bc71a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc71a-140">NOTES</span></span>

## <span data-ttu-id="bc71a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc71a-141">RELATED LINKS</span></span>

[<span data-ttu-id="bc71a-142">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bc71a-142">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="bc71a-143">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bc71a-143">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


