---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505628"
---
# <span data-ttu-id="73bfd-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73bfd-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="73bfd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="73bfd-103">Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73bfd-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73bfd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73bfd-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73bfd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="73bfd-106">A **New-AzureRmAvailabilitySet** parancsmag egy Azure elérhetőségi készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73bfd-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="73bfd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="73bfd-108">Példa 1: elérhetőségi halmaz létrehozása</span><span class="sxs-lookup"><span data-stu-id="73bfd-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="73bfd-109">Ez a parancs létrehoz egy AvailablitySet03 nevű elérhetőségi készletet az ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="73bfd-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="73bfd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73bfd-110">PARAMETERS</span></span>

### <span data-ttu-id="73bfd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bfd-111">-DefaultProfile</span></span>
<span data-ttu-id="73bfd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73bfd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73bfd-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="73bfd-113">-Location</span></span>
<span data-ttu-id="73bfd-114">Az elérhetőségi halmaz helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73bfd-114">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="73bfd-115">Által felügyelt</span><span class="sxs-lookup"><span data-stu-id="73bfd-115">-Managed</span></span>
<span data-ttu-id="73bfd-116">Felügyelt elérhetőségi készlet</span><span class="sxs-lookup"><span data-stu-id="73bfd-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73bfd-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73bfd-117">-Name</span></span>
<span data-ttu-id="73bfd-118">Az elérhetőségi halmaz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73bfd-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="73bfd-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="73bfd-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="73bfd-120">A platform hibás tartományának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="73bfd-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="73bfd-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="73bfd-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="73bfd-122">A platform Update domain count (platform frissítése) beállítás.</span><span class="sxs-lookup"><span data-stu-id="73bfd-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="73bfd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bfd-123">-ResourceGroupName</span></span>
<span data-ttu-id="73bfd-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73bfd-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73bfd-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="73bfd-125">-Sku</span></span>
<span data-ttu-id="73bfd-126">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="73bfd-126">The Name of Sku</span></span>
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

### <span data-ttu-id="73bfd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bfd-127">CommonParameters</span></span>
<span data-ttu-id="73bfd-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73bfd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bfd-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bfd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bfd-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73bfd-130">INPUTS</span></span>

## <span data-ttu-id="73bfd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73bfd-131">OUTPUTS</span></span>

## <span data-ttu-id="73bfd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73bfd-132">NOTES</span></span>

## <span data-ttu-id="73bfd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73bfd-133">RELATED LINKS</span></span>

[<span data-ttu-id="73bfd-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73bfd-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="73bfd-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="73bfd-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


