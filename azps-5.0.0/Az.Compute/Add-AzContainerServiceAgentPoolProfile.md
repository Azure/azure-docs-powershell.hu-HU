---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299642"
---
# <span data-ttu-id="1adea-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1adea-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="1adea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1adea-102">SYNOPSIS</span></span>
<span data-ttu-id="1adea-103">Elhelyez egy tároló szolgáltatás-ügynök készlet-profilt.</span><span class="sxs-lookup"><span data-stu-id="1adea-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="1adea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1adea-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1adea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1adea-105">DESCRIPTION</span></span>
<span data-ttu-id="1adea-106">Az **Add-AzContainerServiceAgentPoolProfile** parancsmag a Container Service Agent Pool-profilját hozzáadja egy helyi tároló szolgáltatási objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="1adea-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="1adea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1adea-107">EXAMPLES</span></span>

### <span data-ttu-id="1adea-108">1. példa: profil hozzáadása</span><span class="sxs-lookup"><span data-stu-id="1adea-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="1adea-109">Ez a parancs hozzáadja a Container Service Agent Pool-profilját a local Container Service objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="1adea-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="1adea-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1adea-110">PARAMETERS</span></span>

### <span data-ttu-id="1adea-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="1adea-111">-ContainerService</span></span>
<span data-ttu-id="1adea-112">Annak a tároló-szolgáltatás objektumnak a megadása, amelyhez a parancsmag hozzáadja az Agent Pool-profilt.</span><span class="sxs-lookup"><span data-stu-id="1adea-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="1adea-113">**ContainerService** -objektum beolvasásához használja a [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1adea-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1adea-114">-Count</span><span class="sxs-lookup"><span data-stu-id="1adea-114">-Count</span></span>
<span data-ttu-id="1adea-115">A szállítótartályokat tároló ügynökök számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1adea-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="1adea-116">A paraméter elfogadható értékei a következők: 1 – 100-ig terjedő egész számok.</span><span class="sxs-lookup"><span data-stu-id="1adea-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="1adea-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="1adea-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adea-118">-DefaultProfile</span></span>
<span data-ttu-id="1adea-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1adea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1adea-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="1adea-120">-DnsPrefix</span></span>
<span data-ttu-id="1adea-121">Azt a DNS-előtagot adja meg, amelyet a parancsmag a teljes tartománynevet használja az ügynöki készlet számára.</span><span class="sxs-lookup"><span data-stu-id="1adea-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adea-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1adea-122">-Name</span></span>
<span data-ttu-id="1adea-123">Az Agent Pool-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1adea-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="1adea-124">Ennek az értéknek egyedinek kell lennie az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="1adea-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adea-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="1adea-125">-VmSize</span></span>
<span data-ttu-id="1adea-126">A meghatalmazottak virtuális gépei méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="1adea-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adea-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1adea-127">-Confirm</span></span>
<span data-ttu-id="1adea-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1adea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1adea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1adea-129">-WhatIf</span></span>
<span data-ttu-id="1adea-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1adea-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1adea-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1adea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1adea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adea-132">CommonParameters</span></span>
<span data-ttu-id="1adea-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1adea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adea-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1adea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adea-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1adea-135">INPUTS</span></span>

### <span data-ttu-id="1adea-136">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1adea-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="1adea-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1adea-137">System.String</span></span>

### <span data-ttu-id="1adea-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1adea-138">System.Int32</span></span>

## <span data-ttu-id="1adea-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1adea-139">OUTPUTS</span></span>

### <span data-ttu-id="1adea-140">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1adea-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1adea-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1adea-141">NOTES</span></span>

## <span data-ttu-id="1adea-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1adea-142">RELATED LINKS</span></span>

[<span data-ttu-id="1adea-143">Új – AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="1adea-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="1adea-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1adea-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
