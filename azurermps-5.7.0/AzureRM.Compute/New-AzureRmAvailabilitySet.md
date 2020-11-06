---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495452"
---
# <span data-ttu-id="fc994-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fc994-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="fc994-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc994-102">SYNOPSIS</span></span>
<span data-ttu-id="fc994-103">Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fc994-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc994-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc994-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="fc994-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc994-105">DESCRIPTION</span></span>
<span data-ttu-id="fc994-106">A **New-AzureRmAvailabilitySet** parancsmag egy Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fc994-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="fc994-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc994-107">EXAMPLES</span></span>

### <span data-ttu-id="fc994-108">Példa 1: elérhetőségi halmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="fc994-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="fc994-109">Ez a parancs létrehoz egy AvailablitySet03 nevű elérhetőségi készletet az ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="fc994-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="fc994-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc994-110">PARAMETERS</span></span>

### <span data-ttu-id="fc994-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="fc994-111">-Location</span></span>
<span data-ttu-id="fc994-112">Az elérhetőségi halmaz helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc994-112">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="fc994-113">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="fc994-113">-Managed</span></span>
<span data-ttu-id="fc994-114">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="fc994-114">Managed Availability Set</span></span>
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

### <span data-ttu-id="fc994-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc994-115">-Name</span></span>
<span data-ttu-id="fc994-116">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc994-116">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="fc994-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fc994-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fc994-118">A platform hibás tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc994-118">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="fc994-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="fc994-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="fc994-120">A platform Update domain count (platform frissítése) beállítás.</span><span class="sxs-lookup"><span data-stu-id="fc994-120">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="fc994-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc994-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc994-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc994-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fc994-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="fc994-123">-Sku</span></span>
<span data-ttu-id="fc994-124">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="fc994-124">The Name of Sku</span></span>
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

### <span data-ttu-id="fc994-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc994-125">CommonParameters</span></span>
<span data-ttu-id="fc994-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc994-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc994-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc994-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc994-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc994-128">INPUTS</span></span>

### <span data-ttu-id="fc994-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fc994-129">None</span></span>
<span data-ttu-id="fc994-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fc994-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc994-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc994-131">OUTPUTS</span></span>

## <span data-ttu-id="fc994-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc994-132">NOTES</span></span>

## <span data-ttu-id="fc994-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc994-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc994-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fc994-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="fc994-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fc994-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


