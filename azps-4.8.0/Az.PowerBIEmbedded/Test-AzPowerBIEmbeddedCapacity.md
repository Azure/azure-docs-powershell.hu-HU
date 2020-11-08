---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025105"
---
# <span data-ttu-id="6a2e9-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6a2e9-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="6a2e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2e9-103">Teszteli a PowerBI beágyazott kapacitású példányok létezését.</span><span class="sxs-lookup"><span data-stu-id="6a2e9-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="6a2e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a2e9-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a2e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2e9-106">A Test-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásainak előfordulását teszteli</span><span class="sxs-lookup"><span data-stu-id="6a2e9-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="6a2e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a2e9-107">EXAMPLES</span></span>

### <span data-ttu-id="6a2e9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a2e9-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="6a2e9-109">Ez a parancs azt ellenőrzi, hogy van-e testcapacity nevű kapacitás</span><span class="sxs-lookup"><span data-stu-id="6a2e9-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="6a2e9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a2e9-110">PARAMETERS</span></span>

### <span data-ttu-id="6a2e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2e9-111">-DefaultProfile</span></span>
<span data-ttu-id="6a2e9-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a2e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a2e9-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a2e9-113">-Name</span></span>
<span data-ttu-id="6a2e9-114">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="6a2e9-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="6a2e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2e9-115">CommonParameters</span></span>
<span data-ttu-id="6a2e9-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a2e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2e9-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2e9-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2e9-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a2e9-118">INPUTS</span></span>

### <span data-ttu-id="6a2e9-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a2e9-119">None</span></span>

## <span data-ttu-id="6a2e9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a2e9-120">OUTPUTS</span></span>

### <span data-ttu-id="6a2e9-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a2e9-121">System.Boolean</span></span>

## <span data-ttu-id="6a2e9-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a2e9-122">NOTES</span></span>

## <span data-ttu-id="6a2e9-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a2e9-123">RELATED LINKS</span></span>

[<span data-ttu-id="6a2e9-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6a2e9-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="6a2e9-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="6a2e9-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
