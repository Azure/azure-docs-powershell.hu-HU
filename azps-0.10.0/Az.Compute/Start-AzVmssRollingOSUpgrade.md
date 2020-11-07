---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: f3ebb13438d88a65e763d81936704db859bc1e97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842478"
---
# <span data-ttu-id="c107d-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c107d-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="c107d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c107d-102">SYNOPSIS</span></span>
<span data-ttu-id="c107d-103">Elindul a folyamatos frissítés, hogy az összes virtuálisgép-készlet példányát a legújabb elérhető platform Image OS verzióba helyezze át.</span><span class="sxs-lookup"><span data-stu-id="c107d-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="c107d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c107d-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c107d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c107d-105">DESCRIPTION</span></span>
<span data-ttu-id="c107d-106">Elindul a folyamatos frissítés, hogy az összes virtuálisgép-készlet példányát a legújabb elérhető platform Image OS verzióba helyezze át.</span><span class="sxs-lookup"><span data-stu-id="c107d-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="c107d-107">Azok a példányok, amelyek már a legújabb elérhető operációsrendszer-verziót futtatják, nem érintettek.</span><span class="sxs-lookup"><span data-stu-id="c107d-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="c107d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c107d-108">EXAMPLES</span></span>

### <span data-ttu-id="c107d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c107d-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c107d-110">Ez a parancs elindítja a VM méretarányú VM-példányok folyamatos frissítését az "Group001" erőforráscsoport "VMSS001" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="c107d-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="c107d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c107d-111">PARAMETERS</span></span>

### <span data-ttu-id="c107d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c107d-112">-AsJob</span></span>
<span data-ttu-id="c107d-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c107d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c107d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c107d-114">-DefaultProfile</span></span>
<span data-ttu-id="c107d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c107d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c107d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c107d-116">-ResourceGroupName</span></span>
<span data-ttu-id="c107d-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c107d-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="c107d-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c107d-118">-VMScaleSetName</span></span>
<span data-ttu-id="c107d-119">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="c107d-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="c107d-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c107d-120">-Confirm</span></span>
<span data-ttu-id="c107d-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c107d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c107d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c107d-122">-WhatIf</span></span>
<span data-ttu-id="c107d-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c107d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c107d-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c107d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c107d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c107d-125">CommonParameters</span></span>
<span data-ttu-id="c107d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c107d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c107d-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c107d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c107d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c107d-128">INPUTS</span></span>

### <span data-ttu-id="c107d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c107d-129">System.String</span></span>

## <span data-ttu-id="c107d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c107d-130">OUTPUTS</span></span>

### <span data-ttu-id="c107d-131">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c107d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c107d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c107d-132">NOTES</span></span>

## <span data-ttu-id="c107d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c107d-133">RELATED LINKS</span></span>

