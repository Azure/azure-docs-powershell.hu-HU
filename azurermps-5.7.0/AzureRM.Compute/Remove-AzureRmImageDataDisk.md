---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493183"
---
# <span data-ttu-id="ff070-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="ff070-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="ff070-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff070-102">SYNOPSIS</span></span>
<span data-ttu-id="ff070-103">Egy képobjektumból eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="ff070-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff070-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff070-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff070-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff070-105">DESCRIPTION</span></span>
<span data-ttu-id="ff070-106">A **Remove-AzureRmImageDataDisk** parancsmag eltávolítja a képobjektumból az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="ff070-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="ff070-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff070-107">EXAMPLES</span></span>

### <span data-ttu-id="ff070-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff070-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="ff070-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="ff070-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ff070-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff070-110">PARAMETERS</span></span>

### <span data-ttu-id="ff070-111">-Kép</span><span class="sxs-lookup"><span data-stu-id="ff070-111">-Image</span></span>
<span data-ttu-id="ff070-112">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ff070-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff070-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="ff070-113">-Lun</span></span>
<span data-ttu-id="ff070-114">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff070-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff070-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff070-115">-Confirm</span></span>
<span data-ttu-id="ff070-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff070-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff070-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff070-117">-WhatIf</span></span>
<span data-ttu-id="ff070-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff070-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff070-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff070-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff070-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff070-120">CommonParameters</span></span>
<span data-ttu-id="ff070-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff070-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff070-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff070-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff070-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff070-123">INPUTS</span></span>

### <span data-ttu-id="ff070-124">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="ff070-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="ff070-125">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ff070-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ff070-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff070-126">OUTPUTS</span></span>

### <span data-ttu-id="ff070-127">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="ff070-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="ff070-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff070-128">NOTES</span></span>

## <span data-ttu-id="ff070-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff070-129">RELATED LINKS</span></span>

