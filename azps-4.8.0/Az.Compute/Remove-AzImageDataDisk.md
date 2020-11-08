---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024826"
---
# <span data-ttu-id="388b4-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="388b4-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="388b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="388b4-102">SYNOPSIS</span></span>
<span data-ttu-id="388b4-103">Egy képobjektumból eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="388b4-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="388b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="388b4-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="388b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="388b4-105">DESCRIPTION</span></span>
<span data-ttu-id="388b4-106">A **Remove-AzImageDataDisk** parancsmag eltávolítja a képobjektumból az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="388b4-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="388b4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="388b4-107">EXAMPLES</span></span>

### <span data-ttu-id="388b4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="388b4-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="388b4-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="388b4-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="388b4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="388b4-110">PARAMETERS</span></span>

### <span data-ttu-id="388b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388b4-111">-DefaultProfile</span></span>
<span data-ttu-id="388b4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="388b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388b4-113">-Kép</span><span class="sxs-lookup"><span data-stu-id="388b4-113">-Image</span></span>
<span data-ttu-id="388b4-114">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="388b4-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="388b4-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="388b4-115">-Lun</span></span>
<span data-ttu-id="388b4-116">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="388b4-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="388b4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="388b4-117">-Confirm</span></span>
<span data-ttu-id="388b4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="388b4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388b4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388b4-119">-WhatIf</span></span>
<span data-ttu-id="388b4-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="388b4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="388b4-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="388b4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388b4-122">CommonParameters</span></span>
<span data-ttu-id="388b4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="388b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388b4-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="388b4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388b4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="388b4-125">INPUTS</span></span>

### <span data-ttu-id="388b4-126">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="388b4-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="388b4-127">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="388b4-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="388b4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="388b4-128">OUTPUTS</span></span>

### <span data-ttu-id="388b4-129">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="388b4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="388b4-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="388b4-130">NOTES</span></span>

## <span data-ttu-id="388b4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="388b4-131">RELATED LINKS</span></span>
