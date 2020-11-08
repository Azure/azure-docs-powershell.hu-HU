---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186791"
---
# <span data-ttu-id="47562-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-101">New-AzContainerService</span></span>

## <span data-ttu-id="47562-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47562-102">SYNOPSIS</span></span>
<span data-ttu-id="47562-103">Tároló szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47562-103">Creates a container service.</span></span>

## <span data-ttu-id="47562-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47562-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47562-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47562-105">DESCRIPTION</span></span>
<span data-ttu-id="47562-106">A **New-AzContainerService** parancsmag létrehoz egy tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="47562-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="47562-107">Adja meg a tároló szolgáltatási objektumát, amelyet az New-AzContainerServiceConfig parancsmag használatával hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="47562-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="47562-108">Példák</span><span class="sxs-lookup"><span data-stu-id="47562-108">EXAMPLES</span></span>

### <span data-ttu-id="47562-109">Példa 1: tároló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="47562-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="47562-110">Az első parancs létrehoz egy ResourceGroup17 nevű erőforráscsoportot a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="47562-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="47562-111">További információt az New-AzResourceGroup parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="47562-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="47562-112">A második parancs létrehoz egy tárolót, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="47562-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="47562-113">További információt az New-AzContainerServiceConfig parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="47562-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="47562-114">A végleges parancs létrehoz egy tároló szolgáltatást a $Containerban tárolt tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="47562-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="47562-115">A szolgáltatás neve csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="47562-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="47562-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47562-116">PARAMETERS</span></span>

### <span data-ttu-id="47562-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47562-117">-AsJob</span></span>
<span data-ttu-id="47562-118">RRun parancsmag a háttérben, és egy feladat visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="47562-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="47562-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-119">-ContainerService</span></span>
<span data-ttu-id="47562-120">Az új szolgáltatás tulajdonságait tartalmazó tároló szolgáltatás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="47562-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="47562-121">**ContainerService** objektum beolvasásához használja az New-AzContainerServiceConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="47562-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="47562-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47562-122">-DefaultProfile</span></span>
<span data-ttu-id="47562-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47562-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47562-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47562-124">-Name</span></span>
<span data-ttu-id="47562-125">A parancsmag által létrehozott tároló szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47562-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="47562-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47562-126">-ResourceGroupName</span></span>
<span data-ttu-id="47562-127">Azt az erőforráscsoport-csoportot adja meg, amelyben a parancsmag telepíti a tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="47562-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="47562-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47562-128">-Confirm</span></span>
<span data-ttu-id="47562-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47562-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47562-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47562-130">-WhatIf</span></span>
<span data-ttu-id="47562-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47562-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47562-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47562-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47562-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47562-133">CommonParameters</span></span>
<span data-ttu-id="47562-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47562-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47562-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47562-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47562-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47562-136">INPUTS</span></span>

### <span data-ttu-id="47562-137">System. String</span><span class="sxs-lookup"><span data-stu-id="47562-137">System.String</span></span>

### <span data-ttu-id="47562-138">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="47562-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47562-139">OUTPUTS</span></span>

### <span data-ttu-id="47562-140">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="47562-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47562-141">NOTES</span></span>

## <span data-ttu-id="47562-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47562-142">RELATED LINKS</span></span>

[<span data-ttu-id="47562-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="47562-144">Új – AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="47562-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="47562-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="47562-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="47562-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


