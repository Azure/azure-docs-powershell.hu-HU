---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497751"
---
# <span data-ttu-id="71737-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="71737-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="71737-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71737-102">SYNOPSIS</span></span>
<span data-ttu-id="71737-103">Az Azure elérhetőségi készleteit egy erőforráscsoport kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71737-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71737-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71737-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="71737-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71737-105">DESCRIPTION</span></span>
<span data-ttu-id="71737-106">A **Get-AzureRmAvailabilitySet** parancsmag az Azure elérhetőségi készleteit egy erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71737-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="71737-107">Megadhatja a beszerzéshez megadott elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="71737-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="71737-108">Példák</span><span class="sxs-lookup"><span data-stu-id="71737-108">EXAMPLES</span></span>

### <span data-ttu-id="71737-109">Példa 1: meghatározott elérhetőségi halmaz beszerzése</span><span class="sxs-lookup"><span data-stu-id="71737-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="71737-110">Ez a parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforrás-csoport elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="71737-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="71737-111">2. példa: az összes elérhetőségi készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="71737-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="71737-112">Ez a parancs a ResourceGroup11 nevű erőforráscsoport elérhetőségi készleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71737-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="71737-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71737-113">PARAMETERS</span></span>

### <span data-ttu-id="71737-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71737-114">-Name</span></span>
<span data-ttu-id="71737-115">A parancsmag által beolvasott elérhetőségi készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71737-115">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="71737-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71737-116">-ResourceGroupName</span></span>
<span data-ttu-id="71737-117">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71737-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="71737-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71737-118">CommonParameters</span></span>
<span data-ttu-id="71737-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71737-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71737-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71737-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71737-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71737-121">INPUTS</span></span>

### <span data-ttu-id="71737-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="71737-122">None</span></span>
<span data-ttu-id="71737-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="71737-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71737-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71737-124">OUTPUTS</span></span>

## <span data-ttu-id="71737-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71737-125">NOTES</span></span>

## <span data-ttu-id="71737-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71737-126">RELATED LINKS</span></span>

[<span data-ttu-id="71737-127">Új – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="71737-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="71737-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="71737-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


