---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 6a342143c8117bca1da5165ecb5a285ee6c0b686
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844586"
---
# <span data-ttu-id="a5efe-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a5efe-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="a5efe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5efe-102">SYNOPSIS</span></span>
<span data-ttu-id="a5efe-103">Az Azure-bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="a5efe-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="a5efe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5efe-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5efe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5efe-105">DESCRIPTION</span></span>
<span data-ttu-id="a5efe-106">A **Get-AzVMExtensionImageType** parancsmag az Azure-bővítmény típusát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="a5efe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5efe-107">EXAMPLES</span></span>

### <span data-ttu-id="a5efe-108">Példa 1: mellék képtípusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a5efe-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="a5efe-109">Ez a parancs a megadott közzétevő és hely kiterjesztési képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="a5efe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5efe-110">PARAMETERS</span></span>

### <span data-ttu-id="a5efe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5efe-111">-DefaultProfile</span></span>
<span data-ttu-id="a5efe-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5efe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5efe-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5efe-113">-Location</span></span>
<span data-ttu-id="a5efe-114">A kiterjesztés helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="a5efe-115">Ez a parancsmag a bővítmény típusát a paraméter által megadott helyen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5efe-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a5efe-116">-PublisherName</span></span>
<span data-ttu-id="a5efe-117">A kiterjesztés közzétevője nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="a5efe-118">A bővítmények közzétevőjét az Get-AzVMImagePublisher parancsmag használatával kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="a5efe-119">Ez a parancsmag a jelen paramétert tartalmazó közzétevőtől kapott bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5efe-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5efe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5efe-120">CommonParameters</span></span>
<span data-ttu-id="a5efe-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5efe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5efe-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5efe-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5efe-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5efe-123">INPUTS</span></span>

### <span data-ttu-id="a5efe-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5efe-124">None</span></span>
<span data-ttu-id="a5efe-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a5efe-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5efe-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5efe-126">OUTPUTS</span></span>

### <span data-ttu-id="a5efe-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a5efe-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="a5efe-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5efe-128">NOTES</span></span>

## <span data-ttu-id="a5efe-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5efe-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5efe-130">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a5efe-130">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="a5efe-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a5efe-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


