---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492240"
---
# <span data-ttu-id="9e86f-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9e86f-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9e86f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e86f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e86f-103">Teszteli a PowerBI beágyazott kapacitású példányok létezését.</span><span class="sxs-lookup"><span data-stu-id="9e86f-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e86f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e86f-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="9e86f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e86f-105">DESCRIPTION</span></span>
<span data-ttu-id="9e86f-106">A Test-AzureRmPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásainak előfordulását teszteli</span><span class="sxs-lookup"><span data-stu-id="9e86f-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="9e86f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e86f-107">EXAMPLES</span></span>

### <span data-ttu-id="9e86f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e86f-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="9e86f-109">Ez a parancs azt ellenőrzi, hogy van-e testcapacity nevű kapacitás</span><span class="sxs-lookup"><span data-stu-id="9e86f-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="9e86f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e86f-110">PARAMETERS</span></span>

### <span data-ttu-id="9e86f-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e86f-111">-Name</span></span>
<span data-ttu-id="9e86f-112">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="9e86f-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="9e86f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e86f-113">CommonParameters</span></span>
<span data-ttu-id="9e86f-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e86f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e86f-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e86f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e86f-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e86f-116">INPUTS</span></span>

### <span data-ttu-id="9e86f-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e86f-117">None</span></span>
<span data-ttu-id="9e86f-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9e86f-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e86f-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e86f-119">OUTPUTS</span></span>

### <span data-ttu-id="9e86f-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e86f-120">System.Boolean</span></span>

## <span data-ttu-id="9e86f-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e86f-121">NOTES</span></span>

## <span data-ttu-id="9e86f-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e86f-122">RELATED LINKS</span></span>

[<span data-ttu-id="9e86f-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9e86f-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="9e86f-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9e86f-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
