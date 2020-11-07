---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842445"
---
# <span data-ttu-id="11fe1-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="11fe1-101">Update-AzImage</span></span>

## <span data-ttu-id="11fe1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="11fe1-103">Frissít egy képet.</span><span class="sxs-lookup"><span data-stu-id="11fe1-103">Updates an image.</span></span>

## <span data-ttu-id="11fe1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11fe1-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11fe1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11fe1-105">DESCRIPTION</span></span>
<span data-ttu-id="11fe1-106">Az **Update-AzImage** parancsmag frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="11fe1-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="11fe1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11fe1-107">EXAMPLES</span></span>

### <span data-ttu-id="11fe1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11fe1-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="11fe1-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="11fe1-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="11fe1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11fe1-110">PARAMETERS</span></span>

### <span data-ttu-id="11fe1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11fe1-111">-AsJob</span></span>
<span data-ttu-id="11fe1-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="11fe1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11fe1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fe1-113">-DefaultProfile</span></span>
<span data-ttu-id="11fe1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11fe1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11fe1-115">-Kép</span><span class="sxs-lookup"><span data-stu-id="11fe1-115">-Image</span></span>
<span data-ttu-id="11fe1-116">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="11fe1-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="11fe1-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="11fe1-117">-ImageName</span></span>
<span data-ttu-id="11fe1-118">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11fe1-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="11fe1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11fe1-119">-ResourceGroupName</span></span>
<span data-ttu-id="11fe1-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11fe1-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="11fe1-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11fe1-121">-Confirm</span></span>
<span data-ttu-id="11fe1-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11fe1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11fe1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11fe1-123">-WhatIf</span></span>
<span data-ttu-id="11fe1-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11fe1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11fe1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11fe1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11fe1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fe1-126">CommonParameters</span></span>
<span data-ttu-id="11fe1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11fe1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fe1-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11fe1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fe1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11fe1-129">INPUTS</span></span>

### <span data-ttu-id="11fe1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="11fe1-130">System.String</span></span>
<span data-ttu-id="11fe1-131">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="11fe1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="11fe1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11fe1-132">OUTPUTS</span></span>

### <span data-ttu-id="11fe1-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="11fe1-133">System.Object</span></span>

## <span data-ttu-id="11fe1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11fe1-134">NOTES</span></span>

## <span data-ttu-id="11fe1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11fe1-135">RELATED LINKS</span></span>

