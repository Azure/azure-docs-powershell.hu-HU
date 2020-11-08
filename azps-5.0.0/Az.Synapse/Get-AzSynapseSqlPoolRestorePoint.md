---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185749"
---
# <span data-ttu-id="e6b87-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e6b87-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="e6b87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6b87-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b87-103">Beolvassa a különböző visszaállítási pontokat, amelyekből a szinapszis-statisztika SQL-készlete állítható vissza.</span><span class="sxs-lookup"><span data-stu-id="e6b87-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="e6b87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6b87-104">SYNTAX</span></span>

### <span data-ttu-id="e6b87-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6b87-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b87-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b87-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b87-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b87-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6b87-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b87-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6b87-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6b87-109">DESCRIPTION</span></span>
<span data-ttu-id="e6b87-110">A **Get-AzSynapseSqlPoolRestorePoint** parancsmag kikeresi az Azure szinapszis-statisztika SQL-készletének különböző visszaállítási pontjait.</span><span class="sxs-lookup"><span data-stu-id="e6b87-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="e6b87-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e6b87-111">EXAMPLES</span></span>

### <span data-ttu-id="e6b87-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6b87-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e6b87-113">Ez a parancs a ContosoSqlPool nevű Azure szinapszis Analytics SQL-készlet minden elérhető visszaállítási pontját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="e6b87-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="e6b87-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6b87-114">PARAMETERS</span></span>

### <span data-ttu-id="e6b87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b87-115">-DefaultProfile</span></span>
<span data-ttu-id="e6b87-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6b87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b87-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6b87-117">-InputObject</span></span>
<span data-ttu-id="e6b87-118">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e6b87-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b87-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6b87-119">-Name</span></span>
<span data-ttu-id="e6b87-120">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="e6b87-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b87-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b87-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6b87-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e6b87-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b87-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b87-123">-ResourceId</span></span>
<span data-ttu-id="e6b87-124">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6b87-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b87-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6b87-125">-WorkspaceName</span></span>
<span data-ttu-id="e6b87-126">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="e6b87-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b87-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6b87-127">-WorkspaceObject</span></span>
<span data-ttu-id="e6b87-128">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e6b87-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b87-129">CommonParameters</span></span>
<span data-ttu-id="e6b87-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6b87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b87-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6b87-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b87-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b87-132">INPUTS</span></span>

### <span data-ttu-id="e6b87-133">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6b87-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e6b87-134">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e6b87-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e6b87-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b87-135">OUTPUTS</span></span>

### <span data-ttu-id="e6b87-136">Microsoft. Azure. Management. szinapszis. models. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="e6b87-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="e6b87-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6b87-137">NOTES</span></span>

## <span data-ttu-id="e6b87-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6b87-138">RELATED LINKS</span></span>
