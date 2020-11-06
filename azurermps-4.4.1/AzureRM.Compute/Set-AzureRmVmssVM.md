---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493573"
---
# <span data-ttu-id="cb2f3-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="cb2f3-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="cb2f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2f3-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb2f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb2f3-104">SYNTAX</span></span>

### <span data-ttu-id="cb2f3-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb2f3-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2f3-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cb2f3-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2f3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb2f3-107">DESCRIPTION</span></span>
<span data-ttu-id="cb2f3-108">A **set-AzureRmVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="cb2f3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cb2f3-109">EXAMPLES</span></span>

## <span data-ttu-id="cb2f3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb2f3-110">PARAMETERS</span></span>

### <span data-ttu-id="cb2f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2f3-111">-DefaultProfile</span></span>
<span data-ttu-id="cb2f3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb2f3-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cb2f3-113">-InstanceId</span></span>
<span data-ttu-id="cb2f3-114">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb2f3-115">-Reimage</span><span class="sxs-lookup"><span data-stu-id="cb2f3-115">-Reimage</span></span>
<span data-ttu-id="cb2f3-116">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2f3-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="cb2f3-117">-ReimageAll</span></span>
<span data-ttu-id="cb2f3-118">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb2f3-120">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="cb2f3-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cb2f3-121">-VMScaleSetName</span></span>
<span data-ttu-id="cb2f3-122">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cb2f3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb2f3-123">-Confirm</span></span>
<span data-ttu-id="cb2f3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2f3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2f3-125">-WhatIf</span></span>
<span data-ttu-id="cb2f3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb2f3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb2f3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2f3-128">CommonParameters</span></span>
<span data-ttu-id="cb2f3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb2f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2f3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2f3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2f3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2f3-131">INPUTS</span></span>

## <span data-ttu-id="cb2f3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2f3-132">OUTPUTS</span></span>

## <span data-ttu-id="cb2f3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb2f3-133">NOTES</span></span>

## <span data-ttu-id="cb2f3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb2f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="cb2f3-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="cb2f3-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
