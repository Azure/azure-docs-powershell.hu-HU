---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850865"
---
# <span data-ttu-id="b6f6a-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b6f6a-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="b6f6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f6a-103">Frissít egy képet.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6f6a-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f6a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f6a-106">Az **Update-AzureRmImage** parancsmag frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="b6f6a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6f6a-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f6a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6f6a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="b6f6a-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b6f6a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6f6a-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f6a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6f6a-111">-AsJob</span></span>
<span data-ttu-id="b6f6a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b6f6a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f6a-113">-DefaultProfile</span></span>
<span data-ttu-id="b6f6a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f6a-115">-Kép</span><span class="sxs-lookup"><span data-stu-id="b6f6a-115">-Image</span></span>
<span data-ttu-id="b6f6a-116">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f6a-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b6f6a-117">-ImageName</span></span>
<span data-ttu-id="b6f6a-118">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b6f6a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f6a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6f6a-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b6f6a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6f6a-121">-Confirm</span></span>
<span data-ttu-id="b6f6a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f6a-123">-WhatIf</span></span>
<span data-ttu-id="b6f6a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f6a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6f6a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f6a-126">CommonParameters</span></span>
<span data-ttu-id="b6f6a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6f6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f6a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f6a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6f6a-129">INPUTS</span></span>

### <span data-ttu-id="b6f6a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f6a-130">System.String</span></span>
<span data-ttu-id="b6f6a-131">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b6f6a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b6f6a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6f6a-132">OUTPUTS</span></span>

### <span data-ttu-id="b6f6a-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b6f6a-133">System.Object</span></span>

## <span data-ttu-id="b6f6a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6f6a-134">NOTES</span></span>

## <span data-ttu-id="b6f6a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6f6a-135">RELATED LINKS</span></span>

