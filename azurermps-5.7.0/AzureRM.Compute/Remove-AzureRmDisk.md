---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493185"
---
# <span data-ttu-id="ba65d-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ba65d-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="ba65d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba65d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba65d-103">Lemez eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ba65d-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba65d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba65d-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba65d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba65d-105">DESCRIPTION</span></span>
<span data-ttu-id="ba65d-106">A **Remove-AzureRmDisk** parancsmag eltávolítja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="ba65d-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="ba65d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba65d-107">EXAMPLES</span></span>

### <span data-ttu-id="ba65d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ba65d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="ba65d-109">Ez a parancs eltávolítja a "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="ba65d-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ba65d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba65d-110">PARAMETERS</span></span>

### <span data-ttu-id="ba65d-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ba65d-111">-DiskName</span></span>
<span data-ttu-id="ba65d-112">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba65d-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ba65d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ba65d-113">-Force</span></span>
<span data-ttu-id="ba65d-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ba65d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba65d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba65d-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba65d-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba65d-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba65d-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba65d-117">-Confirm</span></span>
<span data-ttu-id="ba65d-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba65d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba65d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba65d-119">-WhatIf</span></span>
<span data-ttu-id="ba65d-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba65d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba65d-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba65d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba65d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba65d-122">CommonParameters</span></span>
<span data-ttu-id="ba65d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba65d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba65d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba65d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba65d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba65d-125">INPUTS</span></span>

### <span data-ttu-id="ba65d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ba65d-126">System.String</span></span>

## <span data-ttu-id="ba65d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba65d-127">OUTPUTS</span></span>

### <span data-ttu-id="ba65d-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ba65d-128">System.Object</span></span>

## <span data-ttu-id="ba65d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba65d-129">NOTES</span></span>

## <span data-ttu-id="ba65d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba65d-130">RELATED LINKS</span></span>

