---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477777"
---
# <span data-ttu-id="1d0d3-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="1d0d3-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="1d0d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0d3-103">A virtuális gép alapszámának használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="1d0d3-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1d0d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d0d3-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d0d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d0d3-105">DESCRIPTION</span></span>
<span data-ttu-id="1d0d3-106">A **Get-AzVMUsage** parancsmag egy hely virtuális gép alapszám-használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d0d3-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1d0d3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d0d3-107">EXAMPLES</span></span>

### <span data-ttu-id="1d0d3-108">1. példa: Alapszám használata egy helyhez</span><span class="sxs-lookup"><span data-stu-id="1d0d3-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="1d0d3-109">Ez a parancs a virtuális gép alapszámának használatát kapja meg a Közép-AMERIKAI Egyesült Államokbeli helyhez.</span><span class="sxs-lookup"><span data-stu-id="1d0d3-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1d0d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d0d3-110">PARAMETERS</span></span>

### <span data-ttu-id="1d0d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0d3-111">-DefaultProfile</span></span>
<span data-ttu-id="1d0d3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d0d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d0d3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="1d0d3-113">-Location</span></span>
<span data-ttu-id="1d0d3-114">Azt a helyet adja meg, ahol ez a parancsmag virtuális gépi alapszám-használatot kap.</span><span class="sxs-lookup"><span data-stu-id="1d0d3-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d0d3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0d3-115">CommonParameters</span></span>
<span data-ttu-id="1d0d3-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0d3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0d3-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d0d3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0d3-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d0d3-118">INPUTS</span></span>

### <span data-ttu-id="1d0d3-119">System.String</span><span class="sxs-lookup"><span data-stu-id="1d0d3-119">System.String</span></span>

## <span data-ttu-id="1d0d3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d0d3-120">OUTPUTS</span></span>

### <span data-ttu-id="1d0d3-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="1d0d3-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="1d0d3-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d0d3-122">NOTES</span></span>

## <span data-ttu-id="1d0d3-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d0d3-123">RELATED LINKS</span></span>

[<span data-ttu-id="1d0d3-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1d0d3-124">Get-AzVM</span></span>](./Get-AzVM.md)


