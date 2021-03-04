---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933530"
---
# <span data-ttu-id="068c8-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="068c8-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="068c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="068c8-102">SYNOPSIS</span></span>
<span data-ttu-id="068c8-103">Egy Synapse SQL-készletről készít biztonsági másolatot az Sql-készletről.</span><span class="sxs-lookup"><span data-stu-id="068c8-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="068c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="068c8-104">SYNTAX</span></span>

### <span data-ttu-id="068c8-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="068c8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="068c8-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="068c8-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="068c8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="068c8-107">DESCRIPTION</span></span>
<span data-ttu-id="068c8-108">A **Get-AzSynapseDroppedSqlPool** parancsmag egy megadott törölt SQL-készletről kap biztonsági másolatot, amely visszaállítható, illetve a munkaterületen visszaállítható összes törölt biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="068c8-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="068c8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="068c8-109">EXAMPLES</span></span>

### <span data-ttu-id="068c8-110">1. példa: Megadott megszakadt sqlpools lekérdezése sql-készletből</span><span class="sxs-lookup"><span data-stu-id="068c8-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="068c8-111">A parancsmag lekéri a mellőtett sqlpoolsokat egy sql-készlethez.</span><span class="sxs-lookup"><span data-stu-id="068c8-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="068c8-112">2. példa: Az összes átsiklott sqlpool létrehozása egy munkaterületen</span><span class="sxs-lookup"><span data-stu-id="068c8-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="068c8-113">Ez a parancs elérhetővé válik az sqlpoolból egy adott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="068c8-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="068c8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="068c8-114">PARAMETERS</span></span>

### <span data-ttu-id="068c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068c8-115">-DefaultProfile</span></span>
<span data-ttu-id="068c8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="068c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="068c8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="068c8-117">-Name</span></span>
<span data-ttu-id="068c8-118">A Synapse Sql-készlet.</span><span class="sxs-lookup"><span data-stu-id="068c8-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068c8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="068c8-119">-ResourceId</span></span>
<span data-ttu-id="068c8-120">Input a Dropped Sql Pool Resource Id.</span><span class="sxs-lookup"><span data-stu-id="068c8-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068c8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="068c8-121">-ResourceGroupName</span></span>
<span data-ttu-id="068c8-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="068c8-122">Resource group name.</span></span>

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

### <span data-ttu-id="068c8-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="068c8-123">-WorkspaceName</span></span>
<span data-ttu-id="068c8-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="068c8-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="068c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068c8-125">CommonParameters</span></span>
<span data-ttu-id="068c8-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="068c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068c8-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="068c8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068c8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="068c8-128">INPUTS</span></span>

### <span data-ttu-id="068c8-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="068c8-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="068c8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="068c8-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="068c8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="068c8-131">OUTPUTS</span></span>

### <span data-ttu-id="068c8-132">Microsoft.Azure.Commands.Synapse.Models.PSDSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="068c8-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="068c8-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="068c8-133">NOTES</span></span>

## <span data-ttu-id="068c8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="068c8-134">RELATED LINKS</span></span>
