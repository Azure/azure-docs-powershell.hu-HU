---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679867"
---
# <span data-ttu-id="9d6ea-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d6ea-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="9d6ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9d6ea-103">Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d6ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d6ea-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d6ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d6ea-105">DESCRIPTION</span></span>
<span data-ttu-id="9d6ea-106">A **New-AzureRmAvailabilitySet** parancsmag egy Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="9d6ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d6ea-107">EXAMPLES</span></span>

### <span data-ttu-id="9d6ea-108">Példa 1: elérhetőségi halmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="9d6ea-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="9d6ea-109">Ez a parancs létrehoz egy AvailablitySet03 nevű elérhetőségi készletet az ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9d6ea-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d6ea-110">PARAMETERS</span></span>

### <span data-ttu-id="9d6ea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d6ea-111">-AsJob</span></span>
<span data-ttu-id="9d6ea-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9d6ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d6ea-113">-DefaultProfile</span></span>
<span data-ttu-id="9d6ea-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d6ea-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="9d6ea-115">-Location</span></span>
<span data-ttu-id="9d6ea-116">Az elérhetőségi halmaz helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="9d6ea-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d6ea-117">-Name</span></span>
<span data-ttu-id="9d6ea-118">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="9d6ea-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="9d6ea-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="9d6ea-120">A platform hibás tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="9d6ea-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="9d6ea-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="9d6ea-122">A platform Update domain count (platform frissítése) beállítás.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="9d6ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d6ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d6ea-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9d6ea-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="9d6ea-125">-Sku</span></span>
<span data-ttu-id="9d6ea-126">Az SKU neve.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-126">The Name of Sku.</span></span>
<span data-ttu-id="9d6ea-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9d6ea-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d6ea-128">Igazítás: felügyelt lemezek esetén</span><span class="sxs-lookup"><span data-stu-id="9d6ea-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="9d6ea-129">Klasszikus: nem felügyelt lemezek esetén</span><span class="sxs-lookup"><span data-stu-id="9d6ea-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="9d6ea-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="9d6ea-130">-Tag</span></span>
<span data-ttu-id="9d6ea-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9d6ea-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="9d6ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6ea-132">CommonParameters</span></span>
<span data-ttu-id="9d6ea-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d6ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6ea-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d6ea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6ea-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6ea-135">INPUTS</span></span>

### <span data-ttu-id="9d6ea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9d6ea-136">System.String</span></span>

### <span data-ttu-id="9d6ea-137">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9d6ea-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9d6ea-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6ea-138">OUTPUTS</span></span>

### <span data-ttu-id="9d6ea-139">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d6ea-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9d6ea-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d6ea-140">NOTES</span></span>

## <span data-ttu-id="9d6ea-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d6ea-141">RELATED LINKS</span></span>

[<span data-ttu-id="9d6ea-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d6ea-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="9d6ea-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d6ea-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


