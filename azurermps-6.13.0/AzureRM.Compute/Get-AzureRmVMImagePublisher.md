---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506056"
---
# <span data-ttu-id="86fc9-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="86fc9-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="86fc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="86fc9-103">Megkapja a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="86fc9-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86fc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86fc9-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86fc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="86fc9-106">A **Get-AzureRmVMImagePublisher** parancsmag a VMImage-közzétevőket kapja.</span><span class="sxs-lookup"><span data-stu-id="86fc9-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="86fc9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86fc9-107">EXAMPLES</span></span>

### <span data-ttu-id="86fc9-108">Példa 1: VMImage-közzétevők beszerzése régióhoz</span><span class="sxs-lookup"><span data-stu-id="86fc9-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="86fc9-109">Ez a parancs a VMImage-példányok közzétevőit a közép-amerikai régióban az Azure-profilon belül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86fc9-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="86fc9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86fc9-110">PARAMETERS</span></span>

### <span data-ttu-id="86fc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86fc9-111">-DefaultProfile</span></span>
<span data-ttu-id="86fc9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86fc9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86fc9-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="86fc9-113">-Location</span></span>
<span data-ttu-id="86fc9-114">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86fc9-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="86fc9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86fc9-115">CommonParameters</span></span>
<span data-ttu-id="86fc9-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86fc9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86fc9-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86fc9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86fc9-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86fc9-118">INPUTS</span></span>

### <span data-ttu-id="86fc9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="86fc9-119">System.String</span></span>

## <span data-ttu-id="86fc9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86fc9-120">OUTPUTS</span></span>

### <span data-ttu-id="86fc9-121">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="86fc9-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="86fc9-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86fc9-122">NOTES</span></span>

## <span data-ttu-id="86fc9-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86fc9-123">RELATED LINKS</span></span>

[<span data-ttu-id="86fc9-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="86fc9-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="86fc9-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="86fc9-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="86fc9-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="86fc9-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="86fc9-127">Mentés-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="86fc9-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


