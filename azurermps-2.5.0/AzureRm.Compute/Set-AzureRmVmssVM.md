---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850894"
---
# <span data-ttu-id="b85db-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="b85db-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="b85db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b85db-102">SYNOPSIS</span></span>
<span data-ttu-id="b85db-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="b85db-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b85db-104">SYNTAX</span></span>

### <span data-ttu-id="b85db-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b85db-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85db-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b85db-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85db-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b85db-107">DESCRIPTION</span></span>
<span data-ttu-id="b85db-108">A **set-AzureRmVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="b85db-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b85db-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b85db-109">EXAMPLES</span></span>

## <span data-ttu-id="b85db-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b85db-110">PARAMETERS</span></span>

### <span data-ttu-id="b85db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b85db-111">-AsJob</span></span>
<span data-ttu-id="b85db-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b85db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b85db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85db-113">-DefaultProfile</span></span>
<span data-ttu-id="b85db-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b85db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85db-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b85db-115">-InstanceId</span></span>
<span data-ttu-id="b85db-116">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="b85db-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="b85db-117">-Reimage</span><span class="sxs-lookup"><span data-stu-id="b85db-117">-Reimage</span></span>
<span data-ttu-id="b85db-118">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="b85db-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85db-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="b85db-119">-ReimageAll</span></span>
<span data-ttu-id="b85db-120">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="b85db-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85db-121">-ResourceGroupName</span></span>
<span data-ttu-id="b85db-122">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b85db-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="b85db-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b85db-123">-VMScaleSetName</span></span>
<span data-ttu-id="b85db-124">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b85db-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b85db-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b85db-125">-Confirm</span></span>
<span data-ttu-id="b85db-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b85db-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85db-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85db-127">-WhatIf</span></span>
<span data-ttu-id="b85db-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b85db-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b85db-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b85db-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85db-130">CommonParameters</span></span>
<span data-ttu-id="b85db-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b85db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85db-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85db-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85db-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b85db-133">INPUTS</span></span>

### <span data-ttu-id="b85db-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="b85db-134">None</span></span>
<span data-ttu-id="b85db-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b85db-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b85db-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b85db-136">OUTPUTS</span></span>

### <span data-ttu-id="b85db-137">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b85db-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b85db-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b85db-138">NOTES</span></span>

## <span data-ttu-id="b85db-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b85db-139">RELATED LINKS</span></span>

[<span data-ttu-id="b85db-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="b85db-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
