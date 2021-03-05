---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013733"
---
# <span data-ttu-id="e7616-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="e7616-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="e7616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7616-102">SYNOPSIS</span></span>
<span data-ttu-id="e7616-103">A virtuális gép alapszámának használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="e7616-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e7616-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7616-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7616-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7616-105">DESCRIPTION</span></span>
<span data-ttu-id="e7616-106">A **Get-AzVMUsage** parancsmag egy hely virtuális gép alapszám-használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7616-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e7616-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7616-107">EXAMPLES</span></span>

### <span data-ttu-id="e7616-108">1. példa: Alapszám használata egy helyhez</span><span class="sxs-lookup"><span data-stu-id="e7616-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="e7616-109">Ez a parancs a virtuális gép alapszámának használatát a Közép-AMERIKAI Egyesült Államokbeli helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="e7616-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="e7616-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7616-110">PARAMETERS</span></span>

### <span data-ttu-id="e7616-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7616-111">-DefaultProfile</span></span>
<span data-ttu-id="e7616-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7616-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7616-113">-Location</span><span class="sxs-lookup"><span data-stu-id="e7616-113">-Location</span></span>
<span data-ttu-id="e7616-114">Azt a helyet adja meg, ahol ez a parancsmag virtuális gépi alapszám-használatot kap.</span><span class="sxs-lookup"><span data-stu-id="e7616-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="e7616-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7616-115">CommonParameters</span></span>
<span data-ttu-id="e7616-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7616-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7616-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7616-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7616-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7616-118">INPUTS</span></span>

### <span data-ttu-id="e7616-119">System.String</span><span class="sxs-lookup"><span data-stu-id="e7616-119">System.String</span></span>

## <span data-ttu-id="e7616-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7616-120">OUTPUTS</span></span>

### <span data-ttu-id="e7616-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="e7616-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="e7616-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7616-122">NOTES</span></span>

## <span data-ttu-id="e7616-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7616-123">RELATED LINKS</span></span>

[<span data-ttu-id="e7616-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e7616-124">Get-AzVM</span></span>](./Get-AzVM.md)


