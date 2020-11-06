---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 45accc1c3fd52720d3764a9167f6354316a0c9fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493841"
---
# <span data-ttu-id="f44fc-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="f44fc-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="f44fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f44fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f44fc-103">Az Azure-bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="f44fc-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f44fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f44fc-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f44fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f44fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f44fc-106">A **Get-AzureRmVMExtensionImageType** parancsmag az Azure-bővítmény típusát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="f44fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f44fc-107">EXAMPLES</span></span>

### <span data-ttu-id="f44fc-108">Példa 1: mellék képtípusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f44fc-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="f44fc-109">Ez a parancs a megadott közzétevő és hely kiterjesztési képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="f44fc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f44fc-110">PARAMETERS</span></span>

### <span data-ttu-id="f44fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44fc-111">-DefaultProfile</span></span>
<span data-ttu-id="f44fc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f44fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f44fc-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="f44fc-113">-Location</span></span>
<span data-ttu-id="f44fc-114">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="f44fc-115">Ez a parancsmag a bővítmény típusát a paraméter által megadott helyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44fc-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f44fc-116">-PublisherName</span></span>
<span data-ttu-id="f44fc-117">A kiterjesztés közzétevője nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="f44fc-118">A bővítmények közzétevőjét az Get-AzureRmVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="f44fc-119">Ez a parancsmag a jelen paramétert tartalmazó közzétevőtől kapott bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f44fc-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44fc-120">CommonParameters</span></span>
<span data-ttu-id="f44fc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f44fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44fc-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44fc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44fc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f44fc-123">INPUTS</span></span>

## <span data-ttu-id="f44fc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f44fc-124">OUTPUTS</span></span>

## <span data-ttu-id="f44fc-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f44fc-125">NOTES</span></span>

## <span data-ttu-id="f44fc-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f44fc-126">RELATED LINKS</span></span>

[<span data-ttu-id="f44fc-127">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f44fc-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="f44fc-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f44fc-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


