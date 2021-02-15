---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166522"
---
# <span data-ttu-id="31d97-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="31d97-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="31d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31d97-102">SYNOPSIS</span></span>
<span data-ttu-id="31d97-103">Beveszi a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="31d97-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="31d97-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31d97-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d97-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31d97-105">DESCRIPTION</span></span>
<span data-ttu-id="31d97-106">A **Get-AzVMImagePublisher** parancsmag beveszi a VMImage-közzétevőket.</span><span class="sxs-lookup"><span data-stu-id="31d97-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="31d97-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31d97-107">EXAMPLES</span></span>

### <span data-ttu-id="31d97-108">1. példa: VMImage-közzétevők lekérte egy régióhoz</span><span class="sxs-lookup"><span data-stu-id="31d97-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="31d97-109">Ez a parancs lekérte a VMImage-példányok közzétevőit az Azure-profilján belül az Egyesült Államok középső régiójában.</span><span class="sxs-lookup"><span data-stu-id="31d97-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="31d97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31d97-110">PARAMETERS</span></span>

### <span data-ttu-id="31d97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d97-111">-DefaultProfile</span></span>
<span data-ttu-id="31d97-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31d97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31d97-113">-Location</span><span class="sxs-lookup"><span data-stu-id="31d97-113">-Location</span></span>
<span data-ttu-id="31d97-114">A VMImage helyének megadása.</span><span class="sxs-lookup"><span data-stu-id="31d97-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="31d97-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d97-115">CommonParameters</span></span>
<span data-ttu-id="31d97-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31d97-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d97-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31d97-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d97-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31d97-118">INPUTS</span></span>

### <span data-ttu-id="31d97-119">System.String</span><span class="sxs-lookup"><span data-stu-id="31d97-119">System.String</span></span>

## <span data-ttu-id="31d97-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31d97-120">OUTPUTS</span></span>

### <span data-ttu-id="31d97-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="31d97-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="31d97-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31d97-122">NOTES</span></span>

## <span data-ttu-id="31d97-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31d97-123">RELATED LINKS</span></span>

[<span data-ttu-id="31d97-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="31d97-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="31d97-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="31d97-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="31d97-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="31d97-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="31d97-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="31d97-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


