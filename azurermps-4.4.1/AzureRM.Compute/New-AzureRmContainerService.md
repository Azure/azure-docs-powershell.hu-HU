---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: d908f99e9a1eaa191b45ed08cdb69ebf40b21756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672072"
---
# <span data-ttu-id="ac1c5-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ac1c5-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="ac1c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1c5-103">Tároló szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac1c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac1c5-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac1c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ac1c5-106">A **New-AzureRmContainerService** parancsmag létrehoz egy tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="ac1c5-107">Adja meg a tároló szolgáltatási objektumát, amelyet az New-AzureRmContainerServiceConfig parancsmag használatával hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="ac1c5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ac1c5-108">EXAMPLES</span></span>

### <span data-ttu-id="ac1c5-109">Példa 1: tároló szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac1c5-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="ac1c5-110">Az első parancs létrehoz egy ResourceGroup17 nevű erőforráscsoportot a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="ac1c5-111">További információt az New-AzureRmResourceGroup parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="ac1c5-112">A második parancs létrehoz egy tárolót, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="ac1c5-113">További információt az New-AzureRmContainerServiceConfig parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="ac1c5-114">A végleges parancs létrehoz egy tároló szolgáltatást a $Containerban tárolt tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="ac1c5-115">A szolgáltatás neve csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="ac1c5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac1c5-116">PARAMETERS</span></span>

### <span data-ttu-id="ac1c5-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="ac1c5-117">-ContainerService</span></span>
<span data-ttu-id="ac1c5-118">Az új szolgáltatás tulajdonságait tartalmazó tároló szolgáltatás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="ac1c5-119">**ContainerService** objektum beolvasásához használja az New-AzureRmContainerServiceConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1c5-120">-DefaultProfile</span></span>
<span data-ttu-id="ac1c5-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac1c5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac1c5-122">-Name</span></span>
<span data-ttu-id="ac1c5-123">A parancsmag által létrehozott tároló szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-123">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac1c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac1c5-125">Azt az erőforráscsoport-csoportot adja meg, amelyben a parancsmag telepíti a tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-125">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="ac1c5-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac1c5-126">-Confirm</span></span>
<span data-ttu-id="ac1c5-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1c5-128">-WhatIf</span></span>
<span data-ttu-id="ac1c5-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ac1c5-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac1c5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1c5-131">CommonParameters</span></span>
<span data-ttu-id="ac1c5-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac1c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1c5-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac1c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1c5-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac1c5-134">INPUTS</span></span>

## <span data-ttu-id="ac1c5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac1c5-135">OUTPUTS</span></span>

## <span data-ttu-id="ac1c5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac1c5-136">NOTES</span></span>

## <span data-ttu-id="ac1c5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac1c5-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac1c5-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ac1c5-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="ac1c5-139">Új – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="ac1c5-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="ac1c5-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ac1c5-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="ac1c5-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ac1c5-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


