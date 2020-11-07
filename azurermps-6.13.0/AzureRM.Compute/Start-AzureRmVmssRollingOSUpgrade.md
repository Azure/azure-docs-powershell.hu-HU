---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 239397bc91e42c55d400caf00a83619c4665bbce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679593"
---
# <span data-ttu-id="7cb47-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7cb47-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="7cb47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cb47-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb47-103">Elindul a folyamatos frissítés, hogy az összes virtuálisgép-készlet példányát a legújabb elérhető platform Image OS verzióba helyezze át.</span><span class="sxs-lookup"><span data-stu-id="7cb47-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cb47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cb47-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb47-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cb47-105">DESCRIPTION</span></span>
<span data-ttu-id="7cb47-106">Elindul a folyamatos frissítés, hogy az összes virtuálisgép-készlet példányát a legújabb elérhető platform Image OS verzióba helyezze át.</span><span class="sxs-lookup"><span data-stu-id="7cb47-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="7cb47-107">Azok a példányok, amelyek már a legújabb elérhető operációsrendszer-verziót futtatják, nem érintettek.</span><span class="sxs-lookup"><span data-stu-id="7cb47-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="7cb47-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7cb47-108">EXAMPLES</span></span>

### <span data-ttu-id="7cb47-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7cb47-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7cb47-110">Ez a parancs elindítja a VM méretarányú VM-példányok folyamatos frissítését az "Group001" erőforráscsoport "VMSS001" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="7cb47-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="7cb47-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cb47-111">PARAMETERS</span></span>

### <span data-ttu-id="7cb47-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cb47-112">-AsJob</span></span>
<span data-ttu-id="7cb47-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7cb47-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cb47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb47-114">-DefaultProfile</span></span>
<span data-ttu-id="7cb47-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cb47-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cb47-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb47-116">-ResourceGroupName</span></span>
<span data-ttu-id="7cb47-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7cb47-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="7cb47-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7cb47-118">-VMScaleSetName</span></span>
<span data-ttu-id="7cb47-119">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="7cb47-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="7cb47-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cb47-120">-Confirm</span></span>
<span data-ttu-id="7cb47-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cb47-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb47-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb47-122">-WhatIf</span></span>
<span data-ttu-id="7cb47-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cb47-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb47-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cb47-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb47-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb47-125">CommonParameters</span></span>
<span data-ttu-id="7cb47-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cb47-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb47-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb47-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb47-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cb47-128">INPUTS</span></span>

### <span data-ttu-id="7cb47-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7cb47-129">System.String</span></span>

## <span data-ttu-id="7cb47-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cb47-130">OUTPUTS</span></span>

### <span data-ttu-id="7cb47-131">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7cb47-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7cb47-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cb47-132">NOTES</span></span>

## <span data-ttu-id="7cb47-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cb47-133">RELATED LINKS</span></span>
