---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8dde17b43de9db13f1f61c909ee8c88b95761751
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842486"
---
# <span data-ttu-id="2a931-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2a931-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="2a931-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a931-102">SYNOPSIS</span></span>
<span data-ttu-id="2a931-103">Módosítja egy VMSS-példány állapotát.</span><span class="sxs-lookup"><span data-stu-id="2a931-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="2a931-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a931-104">SYNTAX</span></span>

### <span data-ttu-id="2a931-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a931-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a931-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2a931-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a931-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a931-107">DESCRIPTION</span></span>
<span data-ttu-id="2a931-108">A **set-AzVmssVM** parancsmag a virtuálisgép-készlet (VMSS) példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="2a931-108">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2a931-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2a931-109">EXAMPLES</span></span>

## <span data-ttu-id="2a931-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a931-110">PARAMETERS</span></span>

### <span data-ttu-id="2a931-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a931-111">-AsJob</span></span>
<span data-ttu-id="2a931-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2a931-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a931-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a931-113">-DefaultProfile</span></span>
<span data-ttu-id="2a931-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a931-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a931-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2a931-115">-InstanceId</span></span>
<span data-ttu-id="2a931-116">Annak az VMSS-példánynak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="2a931-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="2a931-117">-Reimage</span><span class="sxs-lookup"><span data-stu-id="2a931-117">-Reimage</span></span>
<span data-ttu-id="2a931-118">Jelzi, hogy ez a parancsmag átadja a VMSS-példányt.</span><span class="sxs-lookup"><span data-stu-id="2a931-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="2a931-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="2a931-119">-ReimageAll</span></span>
<span data-ttu-id="2a931-120">Jelzi, hogy a parancsmag a VMSS példány összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="2a931-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="2a931-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a931-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a931-122">A VMSS-példányt tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a931-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="2a931-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2a931-123">-VMScaleSetName</span></span>
<span data-ttu-id="2a931-124">A parancsmag által módosított VMSS-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a931-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2a931-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a931-125">-Confirm</span></span>
<span data-ttu-id="2a931-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a931-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a931-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a931-127">-WhatIf</span></span>
<span data-ttu-id="2a931-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a931-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a931-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a931-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a931-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a931-130">CommonParameters</span></span>
<span data-ttu-id="2a931-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a931-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a931-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a931-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a931-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a931-133">INPUTS</span></span>

### <span data-ttu-id="2a931-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="2a931-134">None</span></span>
<span data-ttu-id="2a931-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2a931-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a931-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a931-136">OUTPUTS</span></span>

### <span data-ttu-id="2a931-137">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2a931-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2a931-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a931-138">NOTES</span></span>

## <span data-ttu-id="2a931-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a931-139">RELATED LINKS</span></span>

[<span data-ttu-id="2a931-140">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2a931-140">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
