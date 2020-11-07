---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: f2b0cd955cd63eb6066da43e8b468ab4ea9bb0bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667430"
---
# <span data-ttu-id="c70b6-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c70b6-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="c70b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c70b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c70b6-103">Megkapja a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="c70b6-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="c70b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c70b6-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c70b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c70b6-105">DESCRIPTION</span></span>
<span data-ttu-id="c70b6-106">A **Get-AzVMImagePublisher** parancsmag a VMImage-közzétevőket kapja.</span><span class="sxs-lookup"><span data-stu-id="c70b6-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="c70b6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c70b6-107">EXAMPLES</span></span>

### <span data-ttu-id="c70b6-108">Példa 1: VMImage-közzétevők beszerzése régióhoz</span><span class="sxs-lookup"><span data-stu-id="c70b6-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="c70b6-109">Ez a parancs a VMImage-példányok közzétevőit a közép-amerikai régióban az Azure-profilon belül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c70b6-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="c70b6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c70b6-110">PARAMETERS</span></span>

### <span data-ttu-id="c70b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70b6-111">-DefaultProfile</span></span>
<span data-ttu-id="c70b6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c70b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c70b6-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="c70b6-113">-Location</span></span>
<span data-ttu-id="c70b6-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c70b6-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="c70b6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70b6-115">CommonParameters</span></span>
<span data-ttu-id="c70b6-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c70b6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70b6-117">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c70b6-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70b6-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c70b6-118">INPUTS</span></span>

### <span data-ttu-id="c70b6-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c70b6-119">System.String</span></span>

## <span data-ttu-id="c70b6-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c70b6-120">OUTPUTS</span></span>

### <span data-ttu-id="c70b6-121">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c70b6-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="c70b6-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c70b6-122">NOTES</span></span>

## <span data-ttu-id="c70b6-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c70b6-123">RELATED LINKS</span></span>

[<span data-ttu-id="c70b6-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c70b6-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c70b6-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c70b6-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="c70b6-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c70b6-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="c70b6-127">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c70b6-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


