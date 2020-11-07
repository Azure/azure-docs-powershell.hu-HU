---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680185"
---
# <span data-ttu-id="d693d-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="d693d-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="d693d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d693d-102">SYNOPSIS</span></span>
<span data-ttu-id="d693d-103">Beilleszti a virtuális gép alapvető számát a helyhez.</span><span class="sxs-lookup"><span data-stu-id="d693d-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d693d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d693d-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="d693d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d693d-105">DESCRIPTION</span></span>
<span data-ttu-id="d693d-106">A **Get-AzureRmVMUsage** parancsmag a Virtual Machine Core Count használatát kapja meg egy helyhez.</span><span class="sxs-lookup"><span data-stu-id="d693d-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d693d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d693d-107">EXAMPLES</span></span>

### <span data-ttu-id="d693d-108">Példa 1: egy hely alapvető számlálási használati területének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d693d-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="d693d-109">Ez a parancs a Virtual Machine Core Count használatát a közép-amerikai helyhez kapja.</span><span class="sxs-lookup"><span data-stu-id="d693d-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="d693d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d693d-110">PARAMETERS</span></span>

### <span data-ttu-id="d693d-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="d693d-111">-Location</span></span>
<span data-ttu-id="d693d-112">Azt a helyet adja meg, ahol ez a parancsmag a Virtual Machine Core Count használatát kapja.</span><span class="sxs-lookup"><span data-stu-id="d693d-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d693d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d693d-113">CommonParameters</span></span>
<span data-ttu-id="d693d-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d693d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d693d-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d693d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d693d-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d693d-116">INPUTS</span></span>

### <span data-ttu-id="d693d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="d693d-117">None</span></span>
<span data-ttu-id="d693d-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d693d-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d693d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d693d-119">OUTPUTS</span></span>

## <span data-ttu-id="d693d-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d693d-120">NOTES</span></span>

## <span data-ttu-id="d693d-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d693d-121">RELATED LINKS</span></span>

[<span data-ttu-id="d693d-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d693d-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


