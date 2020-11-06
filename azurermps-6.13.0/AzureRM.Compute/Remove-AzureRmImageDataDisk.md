---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 8ff2544aab072842ed851ae0c3768f57d180186d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494110"
---
# <span data-ttu-id="71640-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="71640-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="71640-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71640-102">SYNOPSIS</span></span>
<span data-ttu-id="71640-103">Egy képobjektumból eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="71640-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71640-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71640-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71640-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71640-105">DESCRIPTION</span></span>
<span data-ttu-id="71640-106">A **Remove-AzureRmImageDataDisk** parancsmag eltávolítja a képobjektumból az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="71640-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="71640-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71640-107">EXAMPLES</span></span>

### <span data-ttu-id="71640-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71640-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="71640-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="71640-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="71640-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71640-110">PARAMETERS</span></span>

### <span data-ttu-id="71640-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71640-111">-DefaultProfile</span></span>
<span data-ttu-id="71640-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71640-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71640-113">-Kép</span><span class="sxs-lookup"><span data-stu-id="71640-113">-Image</span></span>
<span data-ttu-id="71640-114">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="71640-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71640-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="71640-115">-Lun</span></span>
<span data-ttu-id="71640-116">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="71640-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71640-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71640-117">-Confirm</span></span>
<span data-ttu-id="71640-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71640-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71640-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71640-119">-WhatIf</span></span>
<span data-ttu-id="71640-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71640-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71640-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71640-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71640-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71640-122">CommonParameters</span></span>
<span data-ttu-id="71640-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71640-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71640-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71640-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71640-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71640-125">INPUTS</span></span>

### <span data-ttu-id="71640-126">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="71640-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="71640-127">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71640-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="71640-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71640-128">OUTPUTS</span></span>

### <span data-ttu-id="71640-129">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="71640-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="71640-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71640-130">NOTES</span></span>

## <span data-ttu-id="71640-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71640-131">RELATED LINKS</span></span>
