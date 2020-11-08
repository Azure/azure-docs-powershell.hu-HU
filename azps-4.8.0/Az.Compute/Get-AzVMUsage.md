---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018127"
---
# <span data-ttu-id="924e9-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="924e9-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="924e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="924e9-102">SYNOPSIS</span></span>
<span data-ttu-id="924e9-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="924e9-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="924e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="924e9-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="924e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="924e9-105">DESCRIPTION</span></span>
<span data-ttu-id="924e9-106">A **Get-AzVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="924e9-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="924e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="924e9-107">EXAMPLES</span></span>

### <span data-ttu-id="924e9-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="924e9-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="924e9-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="924e9-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="924e9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="924e9-110">PARAMETERS</span></span>

### <span data-ttu-id="924e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924e9-111">-DefaultProfile</span></span>
<span data-ttu-id="924e9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="924e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="924e9-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="924e9-113">-Location</span></span>
<span data-ttu-id="924e9-114">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="924e9-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="924e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924e9-115">CommonParameters</span></span>
<span data-ttu-id="924e9-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="924e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924e9-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="924e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924e9-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="924e9-118">INPUTS</span></span>

### <span data-ttu-id="924e9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="924e9-119">System.String</span></span>

## <span data-ttu-id="924e9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="924e9-120">OUTPUTS</span></span>

### <span data-ttu-id="924e9-121">Microsoft. Azure. commands. kiszámítás. modellek. PSUs</span><span class="sxs-lookup"><span data-stu-id="924e9-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="924e9-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="924e9-122">NOTES</span></span>

## <span data-ttu-id="924e9-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="924e9-123">RELATED LINKS</span></span>

[<span data-ttu-id="924e9-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="924e9-124">Get-AzVM</span></span>](./Get-AzVM.md)


