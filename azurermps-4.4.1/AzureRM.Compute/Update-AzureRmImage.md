---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673124"
---
# <span data-ttu-id="6d579-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6d579-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="6d579-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d579-102">SYNOPSIS</span></span>
<span data-ttu-id="6d579-103">Frissít egy képet.</span><span class="sxs-lookup"><span data-stu-id="6d579-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d579-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d579-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d579-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d579-105">DESCRIPTION</span></span>
<span data-ttu-id="6d579-106">Az **Update-AzureRmImage** parancsmag frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="6d579-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="6d579-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6d579-107">EXAMPLES</span></span>

### <span data-ttu-id="6d579-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6d579-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="6d579-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="6d579-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6d579-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d579-110">PARAMETERS</span></span>

### <span data-ttu-id="6d579-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d579-111">-DefaultProfile</span></span>
<span data-ttu-id="6d579-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d579-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d579-113">-Kép</span><span class="sxs-lookup"><span data-stu-id="6d579-113">-Image</span></span>
<span data-ttu-id="6d579-114">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6d579-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d579-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6d579-115">-ImageName</span></span>
<span data-ttu-id="6d579-116">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d579-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d579-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d579-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d579-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d579-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d579-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d579-119">-Confirm</span></span>
<span data-ttu-id="6d579-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d579-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d579-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d579-121">-WhatIf</span></span>
<span data-ttu-id="6d579-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d579-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d579-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d579-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d579-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d579-124">CommonParameters</span></span>
<span data-ttu-id="6d579-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d579-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d579-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d579-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d579-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d579-127">INPUTS</span></span>

### <span data-ttu-id="6d579-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6d579-128">System.String</span></span>
<span data-ttu-id="6d579-129">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="6d579-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="6d579-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d579-130">OUTPUTS</span></span>

### <span data-ttu-id="6d579-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="6d579-131">System.Object</span></span>

## <span data-ttu-id="6d579-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d579-132">NOTES</span></span>

## <span data-ttu-id="6d579-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d579-133">RELATED LINKS</span></span>

