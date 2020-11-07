---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672546"
---
# <span data-ttu-id="711ce-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="711ce-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="711ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="711ce-102">SYNOPSIS</span></span>
<span data-ttu-id="711ce-103">Eltávolít egy képet.</span><span class="sxs-lookup"><span data-stu-id="711ce-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="711ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="711ce-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="711ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="711ce-105">DESCRIPTION</span></span>
<span data-ttu-id="711ce-106">A **Remove-AzureRmImage** parancsmag eltávolítja a képet.</span><span class="sxs-lookup"><span data-stu-id="711ce-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="711ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="711ce-107">EXAMPLES</span></span>

### <span data-ttu-id="711ce-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="711ce-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="711ce-109">Ez a parancs eltávolítja a "Image01" nevű képet a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="711ce-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="711ce-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="711ce-110">PARAMETERS</span></span>

### <span data-ttu-id="711ce-111">-Force</span><span class="sxs-lookup"><span data-stu-id="711ce-111">-Force</span></span>
<span data-ttu-id="711ce-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="711ce-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711ce-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="711ce-113">-ImageName</span></span>
<span data-ttu-id="711ce-114">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="711ce-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="711ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="711ce-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="711ce-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="711ce-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="711ce-117">-Confirm</span></span>
<span data-ttu-id="711ce-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="711ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711ce-119">-WhatIf</span></span>
<span data-ttu-id="711ce-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="711ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711ce-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="711ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="711ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711ce-122">CommonParameters</span></span>
<span data-ttu-id="711ce-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="711ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711ce-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="711ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711ce-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="711ce-125">INPUTS</span></span>

### <span data-ttu-id="711ce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="711ce-126">System.String</span></span>

## <span data-ttu-id="711ce-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="711ce-127">OUTPUTS</span></span>

### <span data-ttu-id="711ce-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="711ce-128">System.Object</span></span>

## <span data-ttu-id="711ce-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="711ce-129">NOTES</span></span>

## <span data-ttu-id="711ce-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="711ce-130">RELATED LINKS</span></span>

