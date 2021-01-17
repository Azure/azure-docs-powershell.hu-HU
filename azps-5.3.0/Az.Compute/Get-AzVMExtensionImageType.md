---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477793"
---
# <span data-ttu-id="7acf1-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7acf1-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="7acf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7acf1-102">SYNOPSIS</span></span>
<span data-ttu-id="7acf1-103">Egy Azure-bővítmény típusát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7acf1-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="7acf1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7acf1-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7acf1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7acf1-105">DESCRIPTION</span></span>
<span data-ttu-id="7acf1-106">A **Get-AzVMExtensionImageType parancsmag** egy Azure-bővítmény típusát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7acf1-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="7acf1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7acf1-107">EXAMPLES</span></span>

### <span data-ttu-id="7acf1-108">1. példa: Bővítmény képtípusának lekérte</span><span class="sxs-lookup"><span data-stu-id="7acf1-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="7acf1-109">Ez a parancs a megadott közzétevő és hely kiterjesztés képtípusát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7acf1-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="7acf1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7acf1-110">PARAMETERS</span></span>

### <span data-ttu-id="7acf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acf1-111">-DefaultProfile</span></span>
<span data-ttu-id="7acf1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7acf1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7acf1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7acf1-113">-Location</span></span>
<span data-ttu-id="7acf1-114">A bővítmény helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7acf1-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="7acf1-115">Ez a parancsmag a paraméter által megadott helyen kapja meg egy bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="7acf1-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="7acf1-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7acf1-116">-PublisherName</span></span>
<span data-ttu-id="7acf1-117">Egy bővítmény közzétevőjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7acf1-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="7acf1-118">Bővítménykiadó beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7acf1-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="7acf1-119">Ez a parancsmag a paraméter által megadott közzétevőtől kapja meg a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="7acf1-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="7acf1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acf1-120">CommonParameters</span></span>
<span data-ttu-id="7acf1-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acf1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acf1-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7acf1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acf1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7acf1-123">INPUTS</span></span>

### <span data-ttu-id="7acf1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7acf1-124">System.String</span></span>

## <span data-ttu-id="7acf1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7acf1-125">OUTPUTS</span></span>

### <span data-ttu-id="7acf1-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7acf1-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="7acf1-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7acf1-127">NOTES</span></span>

## <span data-ttu-id="7acf1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7acf1-128">RELATED LINKS</span></span>

[<span data-ttu-id="7acf1-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7acf1-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="7acf1-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7acf1-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


