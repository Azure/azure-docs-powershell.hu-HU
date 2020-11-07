---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667418"
---
# <span data-ttu-id="3554a-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="3554a-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="3554a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3554a-102">SYNOPSIS</span></span>
<span data-ttu-id="3554a-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="3554a-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="3554a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3554a-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3554a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3554a-105">DESCRIPTION</span></span>
<span data-ttu-id="3554a-106">A **Get-AzVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="3554a-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="3554a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3554a-107">EXAMPLES</span></span>

### <span data-ttu-id="3554a-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="3554a-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="3554a-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="3554a-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="3554a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3554a-110">PARAMETERS</span></span>

### <span data-ttu-id="3554a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3554a-111">-DefaultProfile</span></span>
<span data-ttu-id="3554a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3554a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3554a-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="3554a-113">-Location</span></span>
<span data-ttu-id="3554a-114">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="3554a-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="3554a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3554a-115">CommonParameters</span></span>
<span data-ttu-id="3554a-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3554a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3554a-117">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3554a-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3554a-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3554a-118">INPUTS</span></span>

### <span data-ttu-id="3554a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3554a-119">System.String</span></span>

## <span data-ttu-id="3554a-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3554a-120">OUTPUTS</span></span>

### <span data-ttu-id="3554a-121">Microsoft. Azure. commands. kiszámítás. modellek. PSUs</span><span class="sxs-lookup"><span data-stu-id="3554a-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="3554a-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3554a-122">NOTES</span></span>

## <span data-ttu-id="3554a-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3554a-123">RELATED LINKS</span></span>

[<span data-ttu-id="3554a-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3554a-124">Get-AzVM</span></span>](./Get-AzVM.md)


