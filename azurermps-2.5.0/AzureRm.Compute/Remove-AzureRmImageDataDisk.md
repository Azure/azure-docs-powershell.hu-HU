---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b7e691d3bfea45fc8fc45725ddfe782418c12ab7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850077"
---
# <span data-ttu-id="5e186-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="5e186-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="5e186-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e186-102">SYNOPSIS</span></span>
<span data-ttu-id="5e186-103">Egy képobjektumból eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="5e186-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e186-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e186-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e186-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e186-105">DESCRIPTION</span></span>
<span data-ttu-id="5e186-106">A **Remove-AzureRmImageDataDisk** parancsmag eltávolítja a képobjektumból az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="5e186-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="5e186-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5e186-107">EXAMPLES</span></span>

### <span data-ttu-id="5e186-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e186-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="5e186-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="5e186-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5e186-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e186-110">PARAMETERS</span></span>

### <span data-ttu-id="5e186-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e186-111">-DefaultProfile</span></span>
<span data-ttu-id="5e186-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e186-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e186-113">-Kép</span><span class="sxs-lookup"><span data-stu-id="5e186-113">-Image</span></span>
<span data-ttu-id="5e186-114">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5e186-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e186-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="5e186-115">-Lun</span></span>
<span data-ttu-id="5e186-116">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e186-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="5e186-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e186-117">-Confirm</span></span>
<span data-ttu-id="5e186-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e186-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e186-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e186-119">-WhatIf</span></span>
<span data-ttu-id="5e186-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e186-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e186-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e186-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e186-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e186-122">CommonParameters</span></span>
<span data-ttu-id="5e186-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e186-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e186-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e186-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e186-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e186-125">INPUTS</span></span>

### <span data-ttu-id="5e186-126">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="5e186-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="5e186-127">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5e186-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5e186-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e186-128">OUTPUTS</span></span>

### <span data-ttu-id="5e186-129">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="5e186-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="5e186-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e186-130">NOTES</span></span>

## <span data-ttu-id="5e186-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e186-131">RELATED LINKS</span></span>

