---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: e5dbaec83576e4fdcd61aa2672781571782aaa02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671213"
---
# <span data-ttu-id="a04ea-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a04ea-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="a04ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a04ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a04ea-103">Elindul a folyamatos frissítés, hogy az összes virtuálisgép-készlet példányát a legújabb elérhető platform Image OS verzióba helyezze át.</span><span class="sxs-lookup"><span data-stu-id="a04ea-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="a04ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a04ea-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a04ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a04ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a04ea-106">Elindul a folyamatos frissítés, hogy az összes virtuálisgép-készlet példányát a legújabb elérhető platform Image OS verzióba helyezze át.</span><span class="sxs-lookup"><span data-stu-id="a04ea-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="a04ea-107">Azok a példányok, amelyek már a legújabb elérhető operációsrendszer-verziót futtatják, nem érintettek.</span><span class="sxs-lookup"><span data-stu-id="a04ea-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="a04ea-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a04ea-108">EXAMPLES</span></span>

### <span data-ttu-id="a04ea-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a04ea-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a04ea-110">Ez a parancs elindítja a VM méretarányú VM-példányok folyamatos frissítését az "Group001" erőforráscsoport "VMSS001" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="a04ea-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="a04ea-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a04ea-111">PARAMETERS</span></span>

### <span data-ttu-id="a04ea-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a04ea-112">-AsJob</span></span>
<span data-ttu-id="a04ea-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a04ea-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a04ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04ea-114">-DefaultProfile</span></span>
<span data-ttu-id="a04ea-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a04ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a04ea-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04ea-116">-ResourceGroupName</span></span>
<span data-ttu-id="a04ea-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a04ea-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="a04ea-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a04ea-118">-VMScaleSetName</span></span>
<span data-ttu-id="a04ea-119">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="a04ea-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="a04ea-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a04ea-120">-Confirm</span></span>
<span data-ttu-id="a04ea-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a04ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a04ea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a04ea-122">-WhatIf</span></span>
<span data-ttu-id="a04ea-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a04ea-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a04ea-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a04ea-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a04ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04ea-125">CommonParameters</span></span>
<span data-ttu-id="a04ea-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a04ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04ea-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a04ea-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04ea-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a04ea-128">INPUTS</span></span>

### <span data-ttu-id="a04ea-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a04ea-129">System.String</span></span>

## <span data-ttu-id="a04ea-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a04ea-130">OUTPUTS</span></span>

### <span data-ttu-id="a04ea-131">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a04ea-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a04ea-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a04ea-132">NOTES</span></span>

## <span data-ttu-id="a04ea-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a04ea-133">RELATED LINKS</span></span>
