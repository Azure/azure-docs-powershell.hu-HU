---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
ms.openlocfilehash: 563b8acadcf84359af740f504f3b25555a2e45f1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850169"
---
# <span data-ttu-id="7aca3-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7aca3-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="7aca3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7aca3-102">SYNOPSIS</span></span>
<span data-ttu-id="7aca3-103">A virtuális gépet blob-alapú lemezekkel egy virtuális gépre konvertálja, a kezelt lemezekkel.</span><span class="sxs-lookup"><span data-stu-id="7aca3-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aca3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7aca3-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aca3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7aca3-105">DESCRIPTION</span></span>
<span data-ttu-id="7aca3-106">A **ConvertTo-AzureRmVMManagedDisk** parancsmag a virtuális gépet blob-alapú lemezekkel egy olyan virtuális gépre konvertálja, amelyen kezelt lemezek vannak.</span><span class="sxs-lookup"><span data-stu-id="7aca3-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="7aca3-107">A művelet megkezdése előtt a virtuális gépet le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="7aca3-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="7aca3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7aca3-108">EXAMPLES</span></span>

### <span data-ttu-id="7aca3-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7aca3-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="7aca3-110">Ez a parancs átalakítja az "VM01" nevű virtuális gép blob-alapú lemezeit a felügyelt lemezek "ResourceGroup01" csoportjába.</span><span class="sxs-lookup"><span data-stu-id="7aca3-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="7aca3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7aca3-111">PARAMETERS</span></span>

### <span data-ttu-id="7aca3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7aca3-112">-AsJob</span></span>
<span data-ttu-id="7aca3-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7aca3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7aca3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aca3-114">-DefaultProfile</span></span>
<span data-ttu-id="7aca3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7aca3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aca3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aca3-116">-ResourceGroupName</span></span>
<span data-ttu-id="7aca3-117">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aca3-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7aca3-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="7aca3-118">-VMName</span></span>
<span data-ttu-id="7aca3-119">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aca3-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7aca3-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7aca3-120">-Confirm</span></span>
<span data-ttu-id="7aca3-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7aca3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aca3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aca3-122">-WhatIf</span></span>
<span data-ttu-id="7aca3-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7aca3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7aca3-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aca3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aca3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aca3-125">CommonParameters</span></span>
<span data-ttu-id="7aca3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7aca3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aca3-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aca3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aca3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aca3-128">INPUTS</span></span>

### <span data-ttu-id="7aca3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7aca3-129">System.String</span></span>

## <span data-ttu-id="7aca3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aca3-130">OUTPUTS</span></span>

### <span data-ttu-id="7aca3-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="7aca3-131">System.Object</span></span>

## <span data-ttu-id="7aca3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7aca3-132">NOTES</span></span>

## <span data-ttu-id="7aca3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aca3-133">RELATED LINKS</span></span>

