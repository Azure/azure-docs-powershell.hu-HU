---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 9727ef5520ed067a418e32a98e4a59bedefc84b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667316"
---
# <span data-ttu-id="ccb98-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="ccb98-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="ccb98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccb98-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb98-103">Egy képobjektumból eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="ccb98-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="ccb98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccb98-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb98-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccb98-105">DESCRIPTION</span></span>
<span data-ttu-id="ccb98-106">A **Remove-AzImageDataDisk** parancsmag eltávolítja a képobjektumból az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="ccb98-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="ccb98-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccb98-107">EXAMPLES</span></span>

### <span data-ttu-id="ccb98-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccb98-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="ccb98-109">Ez a parancs eltávolítja az 1-es számú logikai egység adatlemezét a "ResourceGroup01" erőforráscsoport "Image01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="ccb98-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ccb98-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccb98-110">PARAMETERS</span></span>

### <span data-ttu-id="ccb98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb98-111">-DefaultProfile</span></span>
<span data-ttu-id="ccb98-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccb98-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccb98-113">-Kép</span><span class="sxs-lookup"><span data-stu-id="ccb98-113">-Image</span></span>
<span data-ttu-id="ccb98-114">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ccb98-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="ccb98-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="ccb98-115">-Lun</span></span>
<span data-ttu-id="ccb98-116">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccb98-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="ccb98-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccb98-117">-Confirm</span></span>
<span data-ttu-id="ccb98-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccb98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb98-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb98-119">-WhatIf</span></span>
<span data-ttu-id="ccb98-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccb98-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccb98-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccb98-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb98-122">CommonParameters</span></span>
<span data-ttu-id="ccb98-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccb98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb98-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ccb98-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb98-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccb98-125">INPUTS</span></span>

### <span data-ttu-id="ccb98-126">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ccb98-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="ccb98-127">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ccb98-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ccb98-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccb98-128">OUTPUTS</span></span>

### <span data-ttu-id="ccb98-129">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ccb98-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ccb98-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccb98-130">NOTES</span></span>

## <span data-ttu-id="ccb98-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccb98-131">RELATED LINKS</span></span>
