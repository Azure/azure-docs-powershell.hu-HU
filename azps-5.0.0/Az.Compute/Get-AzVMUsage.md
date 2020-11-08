---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185614"
---
# <span data-ttu-id="c1f5c-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="c1f5c-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="c1f5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f5c-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="c1f5c-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c1f5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1f5c-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1f5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="c1f5c-106">A **Get-AzVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="c1f5c-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="c1f5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c1f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="c1f5c-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="c1f5c-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="c1f5c-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="c1f5c-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="c1f5c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1f5c-110">PARAMETERS</span></span>

### <span data-ttu-id="c1f5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f5c-111">-DefaultProfile</span></span>
<span data-ttu-id="c1f5c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1f5c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1f5c-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="c1f5c-113">-Location</span></span>
<span data-ttu-id="c1f5c-114">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="c1f5c-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="c1f5c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f5c-115">CommonParameters</span></span>
<span data-ttu-id="c1f5c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1f5c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f5c-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1f5c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f5c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1f5c-118">INPUTS</span></span>

### <span data-ttu-id="c1f5c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c1f5c-119">System.String</span></span>

## <span data-ttu-id="c1f5c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1f5c-120">OUTPUTS</span></span>

### <span data-ttu-id="c1f5c-121">Microsoft. Azure. commands. kiszámítás. modellek. PSUs</span><span class="sxs-lookup"><span data-stu-id="c1f5c-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="c1f5c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1f5c-122">NOTES</span></span>

## <span data-ttu-id="c1f5c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1f5c-123">RELATED LINKS</span></span>

[<span data-ttu-id="c1f5c-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c1f5c-124">Get-AzVM</span></span>](./Get-AzVM.md)


