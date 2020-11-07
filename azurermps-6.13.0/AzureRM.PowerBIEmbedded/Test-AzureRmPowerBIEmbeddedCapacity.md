---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672910"
---
# <span data-ttu-id="5d691-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5d691-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="5d691-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d691-102">SYNOPSIS</span></span>
<span data-ttu-id="5d691-103">Teszteli a PowerBI beágyazott kapacitású példányok létezését.</span><span class="sxs-lookup"><span data-stu-id="5d691-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d691-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d691-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d691-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d691-105">DESCRIPTION</span></span>
<span data-ttu-id="5d691-106">A Test-AzureRmPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásainak előfordulását teszteli</span><span class="sxs-lookup"><span data-stu-id="5d691-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="5d691-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5d691-107">EXAMPLES</span></span>

### <span data-ttu-id="5d691-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5d691-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="5d691-109">Ez a parancs azt ellenőrzi, hogy van-e testcapacity nevű kapacitás</span><span class="sxs-lookup"><span data-stu-id="5d691-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="5d691-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d691-110">PARAMETERS</span></span>

### <span data-ttu-id="5d691-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d691-111">-DefaultProfile</span></span>
<span data-ttu-id="5d691-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d691-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d691-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d691-113">-Name</span></span>
<span data-ttu-id="5d691-114">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="5d691-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d691-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d691-115">CommonParameters</span></span>
<span data-ttu-id="5d691-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d691-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d691-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d691-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d691-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d691-118">INPUTS</span></span>

### <span data-ttu-id="5d691-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d691-119">None</span></span>

## <span data-ttu-id="5d691-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d691-120">OUTPUTS</span></span>

### <span data-ttu-id="5d691-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d691-121">System.Boolean</span></span>

## <span data-ttu-id="5d691-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d691-122">NOTES</span></span>

## <span data-ttu-id="5d691-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d691-123">RELATED LINKS</span></span>

[<span data-ttu-id="5d691-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5d691-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="5d691-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5d691-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
