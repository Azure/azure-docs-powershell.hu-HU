---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672987"
---
# <span data-ttu-id="42410-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="42410-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="42410-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42410-102">SYNOPSIS</span></span>
<span data-ttu-id="42410-103">Frissít egy képet.</span><span class="sxs-lookup"><span data-stu-id="42410-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42410-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42410-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42410-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42410-105">DESCRIPTION</span></span>
<span data-ttu-id="42410-106">Az **Update-AzureRmImage** parancsmag frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="42410-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="42410-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42410-107">EXAMPLES</span></span>

### <span data-ttu-id="42410-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42410-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="42410-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="42410-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="42410-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42410-110">PARAMETERS</span></span>

### <span data-ttu-id="42410-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42410-111">-AsJob</span></span>
<span data-ttu-id="42410-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="42410-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42410-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42410-113">-DefaultProfile</span></span>
<span data-ttu-id="42410-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42410-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42410-115">-Kép</span><span class="sxs-lookup"><span data-stu-id="42410-115">-Image</span></span>
<span data-ttu-id="42410-116">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="42410-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="42410-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="42410-117">-ImageName</span></span>
<span data-ttu-id="42410-118">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42410-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="42410-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42410-119">-ResourceGroupName</span></span>
<span data-ttu-id="42410-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42410-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="42410-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42410-121">-Confirm</span></span>
<span data-ttu-id="42410-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42410-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42410-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42410-123">-WhatIf</span></span>
<span data-ttu-id="42410-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42410-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42410-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42410-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42410-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42410-126">CommonParameters</span></span>
<span data-ttu-id="42410-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42410-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42410-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42410-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42410-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42410-129">INPUTS</span></span>

### <span data-ttu-id="42410-130">System. String</span><span class="sxs-lookup"><span data-stu-id="42410-130">System.String</span></span>

### <span data-ttu-id="42410-131">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="42410-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="42410-132">Paraméterek: kép (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42410-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="42410-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42410-133">OUTPUTS</span></span>

### <span data-ttu-id="42410-134">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="42410-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="42410-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42410-135">NOTES</span></span>

## <span data-ttu-id="42410-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42410-136">RELATED LINKS</span></span>
