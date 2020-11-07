---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844517"
---
# <span data-ttu-id="4737f-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4737f-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="4737f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4737f-102">SYNOPSIS</span></span>
<span data-ttu-id="4737f-103">Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4737f-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="4737f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4737f-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4737f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4737f-105">DESCRIPTION</span></span>
<span data-ttu-id="4737f-106">A **New-AzAvailabilitySet** parancsmag egy Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4737f-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="4737f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4737f-107">EXAMPLES</span></span>

### <span data-ttu-id="4737f-108">Példa 1: elérhetőségi halmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="4737f-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="4737f-109">Ez a parancs létrehoz egy AvailablitySet03 nevű elérhetőségi készletet az ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="4737f-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4737f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4737f-110">PARAMETERS</span></span>

### <span data-ttu-id="4737f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4737f-111">-AsJob</span></span>
<span data-ttu-id="4737f-112">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4737f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4737f-113">-DefaultProfile</span></span>
<span data-ttu-id="4737f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4737f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="4737f-115">-Location</span></span>
<span data-ttu-id="4737f-116">Az elérhetőségi halmaz helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4737f-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-117">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="4737f-117">-Managed</span></span>
<span data-ttu-id="4737f-118">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="4737f-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4737f-119">-Name</span></span>
<span data-ttu-id="4737f-120">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4737f-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4737f-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4737f-122">A platform hibás tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4737f-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="4737f-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="4737f-124">A platform Update domain count (platform frissítése) beállítás.</span><span class="sxs-lookup"><span data-stu-id="4737f-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4737f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4737f-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4737f-126">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="4737f-127">-Sku</span></span>
<span data-ttu-id="4737f-128">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="4737f-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4737f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4737f-129">CommonParameters</span></span>
<span data-ttu-id="4737f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4737f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4737f-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4737f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4737f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4737f-132">INPUTS</span></span>

### <span data-ttu-id="4737f-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="4737f-133">None</span></span>
<span data-ttu-id="4737f-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4737f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4737f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4737f-135">OUTPUTS</span></span>

### <span data-ttu-id="4737f-136">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4737f-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="4737f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4737f-137">NOTES</span></span>

## <span data-ttu-id="4737f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4737f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4737f-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4737f-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="4737f-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4737f-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


