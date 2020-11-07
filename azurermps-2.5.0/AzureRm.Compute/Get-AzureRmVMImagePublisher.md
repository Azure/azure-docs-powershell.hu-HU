---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850161"
---
# <span data-ttu-id="c98bb-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c98bb-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="c98bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c98bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c98bb-103">Megkapja a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="c98bb-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c98bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c98bb-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c98bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c98bb-105">DESCRIPTION</span></span>
<span data-ttu-id="c98bb-106">A **Get-AzureRmVMImagePublisher** parancsmag a VMImage-közzétevőket kapja.</span><span class="sxs-lookup"><span data-stu-id="c98bb-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="c98bb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c98bb-107">EXAMPLES</span></span>

### <span data-ttu-id="c98bb-108">Példa 1: VMImage-közzétevők beszerzése régióhoz</span><span class="sxs-lookup"><span data-stu-id="c98bb-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="c98bb-109">Ez a parancs a VMImage-példányok közzétevőit a közép-amerikai régióban az Azure-profilon belül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c98bb-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="c98bb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c98bb-110">PARAMETERS</span></span>

### <span data-ttu-id="c98bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98bb-111">-DefaultProfile</span></span>
<span data-ttu-id="c98bb-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c98bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c98bb-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="c98bb-113">-Location</span></span>
<span data-ttu-id="c98bb-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c98bb-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="c98bb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98bb-115">CommonParameters</span></span>
<span data-ttu-id="c98bb-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c98bb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98bb-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98bb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98bb-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c98bb-118">INPUTS</span></span>

### <span data-ttu-id="c98bb-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="c98bb-119">None</span></span>
<span data-ttu-id="c98bb-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c98bb-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c98bb-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c98bb-121">OUTPUTS</span></span>

### <span data-ttu-id="c98bb-122">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c98bb-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="c98bb-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c98bb-123">NOTES</span></span>

## <span data-ttu-id="c98bb-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c98bb-124">RELATED LINKS</span></span>

[<span data-ttu-id="c98bb-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c98bb-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="c98bb-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c98bb-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="c98bb-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c98bb-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c98bb-128">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c98bb-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


