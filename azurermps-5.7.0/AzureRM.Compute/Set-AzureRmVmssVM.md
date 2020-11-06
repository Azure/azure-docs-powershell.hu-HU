---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497684"
---
# <span data-ttu-id="c5dc6-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="c5dc6-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="c5dc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="c5dc6-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5dc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5dc6-104">SYNTAX</span></span>

### <span data-ttu-id="c5dc6-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5dc6-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5dc6-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c5dc6-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5dc6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="c5dc6-108">A **set-AzureRmVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c5dc6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c5dc6-109">EXAMPLES</span></span>

## <span data-ttu-id="c5dc6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5dc6-110">PARAMETERS</span></span>

### <span data-ttu-id="c5dc6-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c5dc6-111">-InstanceId</span></span>
<span data-ttu-id="c5dc6-112">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5dc6-113">-Reimage</span><span class="sxs-lookup"><span data-stu-id="c5dc6-113">-Reimage</span></span>
<span data-ttu-id="c5dc6-114">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dc6-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="c5dc6-115">-ReimageAll</span></span>
<span data-ttu-id="c5dc6-116">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dc6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5dc6-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5dc6-118">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="c5dc6-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c5dc6-119">-VMScaleSetName</span></span>
<span data-ttu-id="c5dc6-120">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c5dc6-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5dc6-121">-Confirm</span></span>
<span data-ttu-id="c5dc6-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5dc6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5dc6-123">-WhatIf</span></span>
<span data-ttu-id="c5dc6-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5dc6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5dc6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5dc6-126">CommonParameters</span></span>
<span data-ttu-id="c5dc6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5dc6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5dc6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5dc6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5dc6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5dc6-129">INPUTS</span></span>

### <span data-ttu-id="c5dc6-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5dc6-130">None</span></span>
<span data-ttu-id="c5dc6-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c5dc6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5dc6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5dc6-132">OUTPUTS</span></span>

## <span data-ttu-id="c5dc6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5dc6-133">NOTES</span></span>

## <span data-ttu-id="c5dc6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5dc6-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5dc6-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="c5dc6-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
