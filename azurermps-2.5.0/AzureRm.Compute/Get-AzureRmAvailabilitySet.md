---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848538"
---
# <span data-ttu-id="f4d72-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4d72-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="f4d72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4d72-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d72-103">Az Azure elérhetőségi készleteit egy erőforráscsoport kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4d72-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4d72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4d72-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4d72-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d72-106">A **Get-AzureRmAvailabilitySet** parancsmag az Azure elérhetőségi készleteit egy erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4d72-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="f4d72-107">Megadhatja a beszerzéshez megadott elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="f4d72-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="f4d72-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f4d72-108">EXAMPLES</span></span>

### <span data-ttu-id="f4d72-109">Példa 1: meghatározott elérhetőségi halmaz beszerzése</span><span class="sxs-lookup"><span data-stu-id="f4d72-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="f4d72-110">Ez a parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforrás-csoport elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="f4d72-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f4d72-111">2. példa: az összes elérhetőségi készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="f4d72-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f4d72-112">Ez a parancs a ResourceGroup11 nevű erőforráscsoport elérhetőségi készleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f4d72-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f4d72-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4d72-113">PARAMETERS</span></span>

### <span data-ttu-id="f4d72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d72-114">-DefaultProfile</span></span>
<span data-ttu-id="f4d72-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4d72-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d72-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4d72-116">-Name</span></span>
<span data-ttu-id="f4d72-117">A parancsmag által beolvasott elérhetőségi készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4d72-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d72-118">-ResourceGroupName</span></span>
<span data-ttu-id="f4d72-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4d72-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f4d72-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d72-120">CommonParameters</span></span>
<span data-ttu-id="f4d72-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4d72-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d72-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d72-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d72-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4d72-123">INPUTS</span></span>

### <span data-ttu-id="f4d72-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4d72-124">None</span></span>
<span data-ttu-id="f4d72-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f4d72-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4d72-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4d72-126">OUTPUTS</span></span>

### <span data-ttu-id="f4d72-127">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4d72-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f4d72-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4d72-128">NOTES</span></span>

## <span data-ttu-id="f4d72-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4d72-129">RELATED LINKS</span></span>

[<span data-ttu-id="f4d72-130">Új – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4d72-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="f4d72-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f4d72-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


