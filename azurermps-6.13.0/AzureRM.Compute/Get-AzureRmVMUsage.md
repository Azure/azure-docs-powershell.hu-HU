---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 22f77bfc5802527103dd0e391a11e16833696abd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499704"
---
# <span data-ttu-id="0166c-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="0166c-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="0166c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0166c-102">SYNOPSIS</span></span>
<span data-ttu-id="0166c-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="0166c-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0166c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0166c-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0166c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0166c-105">DESCRIPTION</span></span>
<span data-ttu-id="0166c-106">A **Get-AzureRmVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="0166c-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="0166c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0166c-107">EXAMPLES</span></span>

### <span data-ttu-id="0166c-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="0166c-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="0166c-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="0166c-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="0166c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0166c-110">PARAMETERS</span></span>

### <span data-ttu-id="0166c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0166c-111">-DefaultProfile</span></span>
<span data-ttu-id="0166c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0166c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0166c-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="0166c-113">-Location</span></span>
<span data-ttu-id="0166c-114">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="0166c-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="0166c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0166c-115">CommonParameters</span></span>
<span data-ttu-id="0166c-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0166c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0166c-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0166c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0166c-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0166c-118">INPUTS</span></span>

### <span data-ttu-id="0166c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0166c-119">System.String</span></span>

## <span data-ttu-id="0166c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0166c-120">OUTPUTS</span></span>

### <span data-ttu-id="0166c-121">Microsoft. Azure. commands. kiszámítás. modellek. PSUs</span><span class="sxs-lookup"><span data-stu-id="0166c-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="0166c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0166c-122">NOTES</span></span>

## <span data-ttu-id="0166c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0166c-123">RELATED LINKS</span></span>

[<span data-ttu-id="0166c-124">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0166c-124">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


