---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 769cb913c04c435071c6b743f0d3de533128986f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504224"
---
# <span data-ttu-id="7223a-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7223a-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="7223a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7223a-102">SYNOPSIS</span></span>
<span data-ttu-id="7223a-103">Az Azure elérhetőségi készleteit egy erőforráscsoport kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7223a-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7223a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7223a-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7223a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7223a-105">DESCRIPTION</span></span>
<span data-ttu-id="7223a-106">A **Get-AzureRmAvailabilitySet** parancsmag az Azure elérhetőségi készleteit egy erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7223a-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="7223a-107">Megadhatja a beszerzéshez megadott elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="7223a-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="7223a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7223a-108">EXAMPLES</span></span>

### <span data-ttu-id="7223a-109">Példa 1: meghatározott elérhetőségi halmaz beszerzése</span><span class="sxs-lookup"><span data-stu-id="7223a-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="7223a-110">Ez a parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforrás-csoport elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="7223a-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="7223a-111">2. példa: az összes elérhetőségi készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="7223a-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7223a-112">Ez a parancs a ResourceGroup11 nevű erőforráscsoport elérhetőségi készleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7223a-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7223a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7223a-113">PARAMETERS</span></span>

### <span data-ttu-id="7223a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7223a-114">-DefaultProfile</span></span>
<span data-ttu-id="7223a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7223a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7223a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7223a-116">-Name</span></span>
<span data-ttu-id="7223a-117">A parancsmag által beolvasott elérhetőségi készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7223a-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7223a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7223a-118">-ResourceGroupName</span></span>
<span data-ttu-id="7223a-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7223a-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7223a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7223a-120">CommonParameters</span></span>
<span data-ttu-id="7223a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7223a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7223a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7223a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7223a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7223a-123">INPUTS</span></span>

## <span data-ttu-id="7223a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7223a-124">OUTPUTS</span></span>

## <span data-ttu-id="7223a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7223a-125">NOTES</span></span>

## <span data-ttu-id="7223a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7223a-126">RELATED LINKS</span></span>

[<span data-ttu-id="7223a-127">Új – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7223a-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="7223a-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7223a-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


