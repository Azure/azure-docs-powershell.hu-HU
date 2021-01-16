---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325439"
---
# <span data-ttu-id="1d495-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1d495-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="1d495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d495-102">SYNOPSIS</span></span>
<span data-ttu-id="1d495-103">VMImage-ajánlattípusokat kap.</span><span class="sxs-lookup"><span data-stu-id="1d495-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="1d495-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d495-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d495-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d495-105">DESCRIPTION</span></span>
<span data-ttu-id="1d495-106">A **Get-AzVMImageOffer** parancsmag a VMImage-ajánlattípusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d495-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="1d495-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d495-107">EXAMPLES</span></span>

### <span data-ttu-id="1d495-108">1. példa: Ajánlattípusok lekérte egy közzétevőnek</span><span class="sxs-lookup"><span data-stu-id="1d495-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="1d495-109">Ez a parancs a közép-amerikai régió adott közzétevőjére vonatkozó ajánlattípusokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d495-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="1d495-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d495-110">PARAMETERS</span></span>

### <span data-ttu-id="1d495-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d495-111">-DefaultProfile</span></span>
<span data-ttu-id="1d495-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d495-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d495-113">-Location</span><span class="sxs-lookup"><span data-stu-id="1d495-113">-Location</span></span>
<span data-ttu-id="1d495-114">A VMImage helyének megadása.</span><span class="sxs-lookup"><span data-stu-id="1d495-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="1d495-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1d495-115">-PublisherName</span></span>
<span data-ttu-id="1d495-116">Egy VMImage-közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d495-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="1d495-117">Közzétevő beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d495-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1d495-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d495-118">CommonParameters</span></span>
<span data-ttu-id="1d495-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d495-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d495-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d495-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d495-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d495-121">INPUTS</span></span>

### <span data-ttu-id="1d495-122">System.String</span><span class="sxs-lookup"><span data-stu-id="1d495-122">System.String</span></span>

## <span data-ttu-id="1d495-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d495-123">OUTPUTS</span></span>

### <span data-ttu-id="1d495-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="1d495-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="1d495-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d495-125">NOTES</span></span>

## <span data-ttu-id="1d495-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d495-126">RELATED LINKS</span></span>

[<span data-ttu-id="1d495-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1d495-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="1d495-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1d495-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="1d495-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1d495-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="1d495-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1d495-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


