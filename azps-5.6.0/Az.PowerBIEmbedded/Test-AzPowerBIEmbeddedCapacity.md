---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941497"
---
# <span data-ttu-id="b1924-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b1924-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b1924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1924-102">SYNOPSIS</span></span>
<span data-ttu-id="b1924-103">A PowerBI beágyazott kapacitásának meglétét teszteli.</span><span class="sxs-lookup"><span data-stu-id="b1924-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="b1924-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1924-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1924-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1924-105">DESCRIPTION</span></span>
<span data-ttu-id="b1924-106">A Test-AzPowerBIEmbeddedCapacity parancsmag teszteli a PowerBI beágyazott kapacitásának egy példányát</span><span class="sxs-lookup"><span data-stu-id="b1924-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="b1924-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1924-107">EXAMPLES</span></span>

### <span data-ttu-id="b1924-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b1924-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="b1924-109">Ez a parancs teszteli, hogy van-e tesztkapacitás nevű kapacitás</span><span class="sxs-lookup"><span data-stu-id="b1924-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="b1924-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1924-110">PARAMETERS</span></span>

### <span data-ttu-id="b1924-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1924-111">-DefaultProfile</span></span>
<span data-ttu-id="b1924-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1924-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1924-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b1924-113">-Name</span></span>
<span data-ttu-id="b1924-114">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="b1924-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="b1924-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1924-115">CommonParameters</span></span>
<span data-ttu-id="b1924-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1924-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1924-117">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1924-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1924-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1924-118">INPUTS</span></span>

### <span data-ttu-id="b1924-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1924-119">None</span></span>

## <span data-ttu-id="b1924-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1924-120">OUTPUTS</span></span>

### <span data-ttu-id="b1924-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1924-121">System.Boolean</span></span>

## <span data-ttu-id="b1924-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1924-122">NOTES</span></span>

## <span data-ttu-id="b1924-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1924-123">RELATED LINKS</span></span>

[<span data-ttu-id="b1924-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b1924-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b1924-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b1924-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
