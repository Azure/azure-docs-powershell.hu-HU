---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 6931f6d80d3e279259b599b782a505b2a21dd074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505199"
---
# <span data-ttu-id="bf470-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="bf470-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="bf470-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf470-102">SYNOPSIS</span></span>
<span data-ttu-id="bf470-103">A virtuális gépet blob-alapú lemezekkel egy virtuális gépre konvertálja, a kezelt lemezekkel.</span><span class="sxs-lookup"><span data-stu-id="bf470-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf470-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf470-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf470-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf470-105">DESCRIPTION</span></span>
<span data-ttu-id="bf470-106">A **ConvertTo-AzureRmVMManagedDisk** parancsmag a virtuális gépet blob-alapú lemezekkel egy olyan virtuális gépre konvertálja, amelyen kezelt lemezek vannak.</span><span class="sxs-lookup"><span data-stu-id="bf470-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="bf470-107">A művelet megkezdése előtt a virtuális gépet le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="bf470-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="bf470-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bf470-108">EXAMPLES</span></span>

### <span data-ttu-id="bf470-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf470-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="bf470-110">Ez a parancs átalakítja az "VM01" nevű virtuális gép blob-alapú lemezeit a felügyelt lemezek "ResourceGroup01" csoportjába.</span><span class="sxs-lookup"><span data-stu-id="bf470-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="bf470-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf470-111">PARAMETERS</span></span>

### <span data-ttu-id="bf470-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf470-112">-DefaultProfile</span></span>
<span data-ttu-id="bf470-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf470-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf470-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf470-114">-ResourceGroupName</span></span>
<span data-ttu-id="bf470-115">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf470-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bf470-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="bf470-116">-VMName</span></span>
<span data-ttu-id="bf470-117">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf470-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="bf470-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf470-118">-Confirm</span></span>
<span data-ttu-id="bf470-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf470-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf470-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf470-120">-WhatIf</span></span>
<span data-ttu-id="bf470-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf470-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf470-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf470-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf470-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf470-123">CommonParameters</span></span>
<span data-ttu-id="bf470-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf470-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf470-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf470-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf470-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf470-126">INPUTS</span></span>

### <span data-ttu-id="bf470-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bf470-127">System.String</span></span>

## <span data-ttu-id="bf470-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf470-128">OUTPUTS</span></span>

### <span data-ttu-id="bf470-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="bf470-129">System.Object</span></span>

## <span data-ttu-id="bf470-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf470-130">NOTES</span></span>

## <span data-ttu-id="bf470-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf470-131">RELATED LINKS</span></span>
