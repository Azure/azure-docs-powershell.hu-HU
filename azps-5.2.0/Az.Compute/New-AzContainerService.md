---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349206"
---
# <span data-ttu-id="c49d3-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-101">New-AzContainerService</span></span>

## <span data-ttu-id="c49d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c49d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c49d3-103">Tárolószolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c49d3-103">Creates a container service.</span></span>

## <span data-ttu-id="c49d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c49d3-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c49d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c49d3-105">DESCRIPTION</span></span>
<span data-ttu-id="c49d3-106">A **New-AzContainerService** parancsmag létrehoz egy tárolószolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="c49d3-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="c49d3-107">Adjon meg egy tárolószolgáltatás-objektumot, amelyet létrehozhat a New-AzContainerServiceConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="c49d3-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="c49d3-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c49d3-108">EXAMPLES</span></span>

### <span data-ttu-id="c49d3-109">1. példa: Tárolószolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="c49d3-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="c49d3-110">Az első parancs létrehoz egy ResourceGroup17 nevű erőforráscsoportot a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="c49d3-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="c49d3-111">További információért lásd a New-AzResourceGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c49d3-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c49d3-112">A második parancs létrehoz egy tárolót, majd a $Container tárolja.</span><span class="sxs-lookup"><span data-stu-id="c49d3-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c49d3-113">További információért lásd a New-AzContainerServiceConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c49d3-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="c49d3-114">Az utolsó parancs létrehoz egy tárolószolgáltatást a $Container.</span><span class="sxs-lookup"><span data-stu-id="c49d3-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="c49d3-115">A szolgáltatás neve csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="c49d3-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="c49d3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c49d3-116">PARAMETERS</span></span>

### <span data-ttu-id="c49d3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c49d3-117">-AsJob</span></span>
<span data-ttu-id="c49d3-118">A RRun parancsmag a háttérben, és a feladat visszaküldése az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c49d3-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c49d3-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-119">-ContainerService</span></span>
<span data-ttu-id="c49d3-120">Egy tárolószolgáltatás-objektumot ad meg, amely az új szolgáltatás tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c49d3-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="c49d3-121">**ContainerService-objektum** beszerzéséhez használja a New-AzContainerServiceConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c49d3-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c49d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49d3-122">-DefaultProfile</span></span>
<span data-ttu-id="c49d3-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c49d3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c49d3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c49d3-124">-Name</span></span>
<span data-ttu-id="c49d3-125">A parancsmag által létrehozott tárolószolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="c49d3-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c49d3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49d3-126">-ResourceGroupName</span></span>
<span data-ttu-id="c49d3-127">Azt az erőforráscsoportot adja meg, amelyben ez a parancsmag telepíti a tárolószolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="c49d3-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="c49d3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c49d3-128">-Confirm</span></span>
<span data-ttu-id="c49d3-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c49d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c49d3-130">-WhatIf</span></span>
<span data-ttu-id="c49d3-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c49d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c49d3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c49d3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49d3-133">CommonParameters</span></span>
<span data-ttu-id="c49d3-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49d3-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c49d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49d3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c49d3-136">INPUTS</span></span>

### <span data-ttu-id="c49d3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c49d3-137">System.String</span></span>

### <span data-ttu-id="c49d3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="c49d3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c49d3-139">OUTPUTS</span></span>

### <span data-ttu-id="c49d3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="c49d3-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c49d3-141">NOTES</span></span>

## <span data-ttu-id="c49d3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c49d3-142">RELATED LINKS</span></span>

[<span data-ttu-id="c49d3-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="c49d3-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="c49d3-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="c49d3-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="c49d3-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c49d3-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


