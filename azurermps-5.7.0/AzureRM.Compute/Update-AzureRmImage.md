---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492341"
---
# <span data-ttu-id="b084f-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b084f-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="b084f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b084f-102">SYNOPSIS</span></span>
<span data-ttu-id="b084f-103">Frissít egy képet.</span><span class="sxs-lookup"><span data-stu-id="b084f-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b084f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b084f-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b084f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b084f-105">DESCRIPTION</span></span>
<span data-ttu-id="b084f-106">Az **Update-AzureRmImage** parancsmag frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="b084f-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="b084f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b084f-107">EXAMPLES</span></span>

### <span data-ttu-id="b084f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b084f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="b084f-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="b084f-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b084f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b084f-110">PARAMETERS</span></span>

### <span data-ttu-id="b084f-111">-Kép</span><span class="sxs-lookup"><span data-stu-id="b084f-111">-Image</span></span>
<span data-ttu-id="b084f-112">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b084f-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b084f-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b084f-113">-ImageName</span></span>
<span data-ttu-id="b084f-114">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b084f-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b084f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b084f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b084f-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b084f-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b084f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b084f-117">-Confirm</span></span>
<span data-ttu-id="b084f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b084f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b084f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b084f-119">-WhatIf</span></span>
<span data-ttu-id="b084f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b084f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b084f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b084f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b084f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b084f-122">CommonParameters</span></span>
<span data-ttu-id="b084f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b084f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b084f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b084f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b084f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b084f-125">INPUTS</span></span>

### <span data-ttu-id="b084f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b084f-126">System.String</span></span>
<span data-ttu-id="b084f-127">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="b084f-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="b084f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b084f-128">OUTPUTS</span></span>

### <span data-ttu-id="b084f-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b084f-129">System.Object</span></span>

## <span data-ttu-id="b084f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b084f-130">NOTES</span></span>

## <span data-ttu-id="b084f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b084f-131">RELATED LINKS</span></span>

