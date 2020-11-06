---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503860"
---
# <span data-ttu-id="eb5da-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="eb5da-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="eb5da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb5da-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5da-103">A virtuális gépet blob-alapú lemezekkel egy virtuális gépre konvertálja, a kezelt lemezekkel.</span><span class="sxs-lookup"><span data-stu-id="eb5da-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb5da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb5da-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb5da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb5da-105">DESCRIPTION</span></span>
<span data-ttu-id="eb5da-106">A **ConvertTo-AzureRmVMManagedDisk** parancsmag a virtuális gépet blob-alapú lemezekkel egy olyan virtuális gépre konvertálja, amelyen kezelt lemezek vannak.</span><span class="sxs-lookup"><span data-stu-id="eb5da-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="eb5da-107">A művelet megkezdése előtt a virtuális gépet le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="eb5da-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="eb5da-108">Példák</span><span class="sxs-lookup"><span data-stu-id="eb5da-108">EXAMPLES</span></span>

### <span data-ttu-id="eb5da-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb5da-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="eb5da-110">Ez a parancs átalakítja az "VM01" nevű virtuális gép blob-alapú lemezeit a felügyelt lemezek "ResourceGroup01" csoportjába.</span><span class="sxs-lookup"><span data-stu-id="eb5da-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="eb5da-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb5da-111">PARAMETERS</span></span>

### <span data-ttu-id="eb5da-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5da-112">-ResourceGroupName</span></span>
<span data-ttu-id="eb5da-113">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb5da-113">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eb5da-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb5da-114">-VMName</span></span>
<span data-ttu-id="eb5da-115">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb5da-115">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="eb5da-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb5da-116">-Confirm</span></span>
<span data-ttu-id="eb5da-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb5da-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb5da-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5da-118">-WhatIf</span></span>
<span data-ttu-id="eb5da-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb5da-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb5da-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb5da-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb5da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5da-121">CommonParameters</span></span>
<span data-ttu-id="eb5da-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb5da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5da-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb5da-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5da-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5da-124">INPUTS</span></span>

### <span data-ttu-id="eb5da-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eb5da-125">System.String</span></span>

## <span data-ttu-id="eb5da-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5da-126">OUTPUTS</span></span>

### <span data-ttu-id="eb5da-127">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="eb5da-127">System.Object</span></span>

## <span data-ttu-id="eb5da-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb5da-128">NOTES</span></span>

## <span data-ttu-id="eb5da-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb5da-129">RELATED LINKS</span></span>

