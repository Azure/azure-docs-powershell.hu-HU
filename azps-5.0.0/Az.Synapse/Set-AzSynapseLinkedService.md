---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186160"
---
# <span data-ttu-id="2270c-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="2270c-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="2270c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2270c-102">SYNOPSIS</span></span>
<span data-ttu-id="2270c-103">Az adattárolók vagy a Felhőbeli szolgáltatások összekapcsolása a munkaterületre</span><span class="sxs-lookup"><span data-stu-id="2270c-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="2270c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2270c-104">SYNTAX</span></span>

### <span data-ttu-id="2270c-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2270c-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2270c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="2270c-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2270c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2270c-107">DESCRIPTION</span></span>
<span data-ttu-id="2270c-108">A **set-AzSynapseLinkedService** parancsmag adattárolóhoz vagy felhőalapú szolgáltatáshoz csatolja a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="2270c-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="2270c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2270c-109">EXAMPLES</span></span>

### <span data-ttu-id="2270c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2270c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="2270c-111">Ez a parancs létrehoz egy ContosoLinkedService nevű hivatkozást a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="2270c-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2270c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="2270c-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="2270c-113">Ez a parancs létrehoz egy ContosoLinkedService nevű hivatkozást a ContosoWorkspace-alapú munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="2270c-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2270c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2270c-114">PARAMETERS</span></span>

### <span data-ttu-id="2270c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2270c-115">-AsJob</span></span>
<span data-ttu-id="2270c-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2270c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2270c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2270c-117">-DefaultProfile</span></span>
<span data-ttu-id="2270c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2270c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2270c-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2270c-119">-DefinitionFile</span></span>
<span data-ttu-id="2270c-120">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2270c-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2270c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2270c-121">-Name</span></span>
<span data-ttu-id="2270c-122">A kapcsolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="2270c-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2270c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2270c-123">-WorkspaceName</span></span>
<span data-ttu-id="2270c-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="2270c-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2270c-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2270c-125">-WorkspaceObject</span></span>
<span data-ttu-id="2270c-126">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2270c-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2270c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2270c-127">-Confirm</span></span>
<span data-ttu-id="2270c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2270c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2270c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2270c-129">-WhatIf</span></span>
<span data-ttu-id="2270c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2270c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2270c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2270c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2270c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2270c-132">CommonParameters</span></span>
<span data-ttu-id="2270c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2270c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2270c-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2270c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2270c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2270c-135">INPUTS</span></span>

### <span data-ttu-id="2270c-136">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2270c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2270c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2270c-137">OUTPUTS</span></span>

### <span data-ttu-id="2270c-138">Microsoft. Azure. commands. szinapszis. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="2270c-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="2270c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2270c-139">NOTES</span></span>

## <span data-ttu-id="2270c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2270c-140">RELATED LINKS</span></span>