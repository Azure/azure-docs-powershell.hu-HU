---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: dcb5913176af352c39867f7029523765aca0d781
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844582"
---
# <span data-ttu-id="06919-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="06919-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="06919-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06919-102">SYNOPSIS</span></span>
<span data-ttu-id="06919-103">Megkapja a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="06919-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="06919-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06919-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06919-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06919-105">DESCRIPTION</span></span>
<span data-ttu-id="06919-106">A **Get-AzVMImagePublisher** parancsmag a VMImage-közzétevőket kapja.</span><span class="sxs-lookup"><span data-stu-id="06919-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="06919-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06919-107">EXAMPLES</span></span>

### <span data-ttu-id="06919-108">Példa 1: VMImage-közzétevők beszerzése régióhoz</span><span class="sxs-lookup"><span data-stu-id="06919-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="06919-109">Ez a parancs a VMImage-példányok közzétevőit a közép-amerikai régióban az Azure-profilon belül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="06919-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="06919-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06919-110">PARAMETERS</span></span>

### <span data-ttu-id="06919-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06919-111">-DefaultProfile</span></span>
<span data-ttu-id="06919-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06919-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06919-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="06919-113">-Location</span></span>
<span data-ttu-id="06919-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06919-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="06919-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06919-115">CommonParameters</span></span>
<span data-ttu-id="06919-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06919-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06919-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06919-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06919-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06919-118">INPUTS</span></span>

### <span data-ttu-id="06919-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="06919-119">None</span></span>
<span data-ttu-id="06919-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="06919-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06919-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06919-121">OUTPUTS</span></span>

### <span data-ttu-id="06919-122">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="06919-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="06919-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06919-123">NOTES</span></span>

## <span data-ttu-id="06919-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06919-124">RELATED LINKS</span></span>

[<span data-ttu-id="06919-125">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="06919-125">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="06919-126">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="06919-126">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="06919-127">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="06919-127">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="06919-128">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="06919-128">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


