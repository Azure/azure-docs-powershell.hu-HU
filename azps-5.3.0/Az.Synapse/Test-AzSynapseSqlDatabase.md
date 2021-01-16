---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470261"
---
# <span data-ttu-id="a4610-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4610-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="a4610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4610-102">SYNOPSIS</span></span>
<span data-ttu-id="a4610-103">Ellenőrzi, hogy létezik-e Synapse Analytics SQL-adatbázis.</span><span class="sxs-lookup"><span data-stu-id="a4610-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a4610-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4610-104">SYNTAX</span></span>

### <span data-ttu-id="a4610-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4610-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4610-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4610-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4610-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4610-107">DESCRIPTION</span></span>
<span data-ttu-id="a4610-108">A **Test-AzSynapseSqlDatabase** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics SQL-adatbázis.</span><span class="sxs-lookup"><span data-stu-id="a4610-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a4610-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4610-109">EXAMPLES</span></span>

### <span data-ttu-id="a4610-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a4610-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="a4610-111">Ez a parancs ellenőrzi a megadott SQL-adatbázis meglétét.</span><span class="sxs-lookup"><span data-stu-id="a4610-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="a4610-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4610-112">PARAMETERS</span></span>

### <span data-ttu-id="a4610-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4610-113">-DefaultProfile</span></span>
<span data-ttu-id="a4610-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4610-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4610-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a4610-115">-Name</span></span>
<span data-ttu-id="a4610-116">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a4610-116">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4610-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4610-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4610-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4610-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4610-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4610-119">-WorkspaceName</span></span>
<span data-ttu-id="a4610-120">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a4610-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4610-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a4610-121">-WorkspaceObject</span></span>
<span data-ttu-id="a4610-122">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="a4610-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4610-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4610-123">CommonParameters</span></span>
<span data-ttu-id="a4610-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4610-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4610-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4610-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4610-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4610-126">INPUTS</span></span>

### <span data-ttu-id="a4610-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4610-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a4610-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4610-128">OUTPUTS</span></span>

### <span data-ttu-id="a4610-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4610-129">System.Boolean</span></span>

## <span data-ttu-id="a4610-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4610-130">NOTES</span></span>

## <span data-ttu-id="a4610-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4610-131">RELATED LINKS</span></span>
