---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334685"
---
# <span data-ttu-id="8c374-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="8c374-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="8c374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c374-102">SYNOPSIS</span></span>
<span data-ttu-id="8c374-103">Hozzáad egy tárolószolgáltatás ügynökkészlet-profilját.</span><span class="sxs-lookup"><span data-stu-id="8c374-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="8c374-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c374-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c374-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c374-105">DESCRIPTION</span></span>
<span data-ttu-id="8c374-106">Az **Add-AzContainerServiceAgentPoolProfile** parancsmag hozzáad egy tárolószolgáltatás-ügynökkészlet-profilt egy helyi tárolószolgáltatás-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8c374-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="8c374-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c374-107">EXAMPLES</span></span>

### <span data-ttu-id="8c374-108">1. példa: Profil hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8c374-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="8c374-109">Ez a parancs hozzáad egy tárolószolgáltatás ügynökkészlet-profilt a helyi tárolószolgáltatás-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8c374-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="8c374-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c374-110">PARAMETERS</span></span>

### <span data-ttu-id="8c374-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="8c374-111">-ContainerService</span></span>
<span data-ttu-id="8c374-112">Megadja azt a tárolószolgáltatás-objektumot, amelyhez ez a parancsmag hozzáad egy ügynökkészlet-profilt.</span><span class="sxs-lookup"><span data-stu-id="8c374-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="8c374-113">**ContainerService-objektum** beszerzéséhez használja a [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8c374-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="8c374-114">-Count</span><span class="sxs-lookup"><span data-stu-id="8c374-114">-Count</span></span>
<span data-ttu-id="8c374-115">A tárolókat tároló ügynökök számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c374-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="8c374-116">A paraméter elfogadható értékei: 1 és 100 között egész értékek.</span><span class="sxs-lookup"><span data-stu-id="8c374-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="8c374-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="8c374-117">The default value is 1.</span></span>

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

### <span data-ttu-id="8c374-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c374-118">-DefaultProfile</span></span>
<span data-ttu-id="8c374-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c374-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c374-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="8c374-120">-DnsPrefix</span></span>
<span data-ttu-id="8c374-121">Megadja azt a DNS-előtagot, amely alapján a parancsmag létrehozza az ügynökkészlet teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="8c374-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="8c374-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8c374-122">-Name</span></span>
<span data-ttu-id="8c374-123">Az ügynökkészlet-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c374-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="8c374-124">Ennek az értéknek egyedinek kell lennie az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="8c374-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="8c374-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="8c374-125">-VmSize</span></span>
<span data-ttu-id="8c374-126">Az ügynökök virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="8c374-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="8c374-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c374-127">-Confirm</span></span>
<span data-ttu-id="8c374-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c374-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c374-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c374-129">-WhatIf</span></span>
<span data-ttu-id="8c374-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c374-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c374-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c374-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c374-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c374-132">CommonParameters</span></span>
<span data-ttu-id="8c374-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c374-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c374-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c374-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c374-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c374-135">INPUTS</span></span>

### <span data-ttu-id="8c374-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="8c374-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="8c374-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8c374-137">System.String</span></span>

### <span data-ttu-id="8c374-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8c374-138">System.Int32</span></span>

## <span data-ttu-id="8c374-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c374-139">OUTPUTS</span></span>

### <span data-ttu-id="8c374-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="8c374-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="8c374-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c374-141">NOTES</span></span>

## <span data-ttu-id="8c374-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c374-142">RELATED LINKS</span></span>

[<span data-ttu-id="8c374-143">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8c374-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="8c374-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="8c374-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
