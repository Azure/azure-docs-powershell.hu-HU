---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847342"
---
# <span data-ttu-id="0c414-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0c414-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="0c414-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c414-102">SYNOPSIS</span></span>
<span data-ttu-id="0c414-103">A virtuális gépet blob-alapú lemezekkel egy virtuális gépre konvertálja, a kezelt lemezekkel.</span><span class="sxs-lookup"><span data-stu-id="0c414-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="0c414-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c414-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c414-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c414-105">DESCRIPTION</span></span>
<span data-ttu-id="0c414-106">A **ConvertTo-AzVMManagedDisk** parancsmag a virtuális gépet blob-alapú lemezekkel egy olyan virtuális gépre konvertálja, amelyen kezelt lemezek vannak.</span><span class="sxs-lookup"><span data-stu-id="0c414-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="0c414-107">A művelet megkezdése előtt a virtuális gépet le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="0c414-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="0c414-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0c414-108">EXAMPLES</span></span>

### <span data-ttu-id="0c414-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c414-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="0c414-110">Ez a parancs átalakítja az "VM01" nevű virtuális gép blob-alapú lemezeit a felügyelt lemezek "ResourceGroup01" csoportjába.</span><span class="sxs-lookup"><span data-stu-id="0c414-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="0c414-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c414-111">PARAMETERS</span></span>

### <span data-ttu-id="0c414-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c414-112">-AsJob</span></span>
<span data-ttu-id="0c414-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0c414-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c414-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c414-114">-DefaultProfile</span></span>
<span data-ttu-id="0c414-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c414-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c414-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c414-116">-ResourceGroupName</span></span>
<span data-ttu-id="0c414-117">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c414-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c414-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="0c414-118">-VMName</span></span>
<span data-ttu-id="0c414-119">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c414-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c414-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c414-120">-Confirm</span></span>
<span data-ttu-id="0c414-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c414-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c414-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c414-122">-WhatIf</span></span>
<span data-ttu-id="0c414-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c414-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c414-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c414-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c414-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c414-125">CommonParameters</span></span>
<span data-ttu-id="0c414-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c414-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c414-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c414-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c414-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c414-128">INPUTS</span></span>

### <span data-ttu-id="0c414-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c414-129">System.String</span></span>

## <span data-ttu-id="0c414-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c414-130">OUTPUTS</span></span>

### <span data-ttu-id="0c414-131">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0c414-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0c414-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c414-132">NOTES</span></span>

## <span data-ttu-id="0c414-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c414-133">RELATED LINKS</span></span>
