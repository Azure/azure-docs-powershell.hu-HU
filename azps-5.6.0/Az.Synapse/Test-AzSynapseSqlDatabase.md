---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e797cba0c05b6dbaee11d540b9efc3aca7e7efcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011254"
---
# <span data-ttu-id="63f54-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="63f54-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="63f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f54-102">SYNOPSIS</span></span>
<span data-ttu-id="63f54-103">Ellenőrzi, hogy létezik-e Synapse Analytics SQL-adatbázis.</span><span class="sxs-lookup"><span data-stu-id="63f54-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="63f54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63f54-104">SYNTAX</span></span>

### <span data-ttu-id="63f54-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63f54-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63f54-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63f54-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f54-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63f54-107">DESCRIPTION</span></span>
<span data-ttu-id="63f54-108">A **Test-AzSynapseSqlDatabase** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics SQL-adatbázis.</span><span class="sxs-lookup"><span data-stu-id="63f54-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="63f54-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63f54-109">EXAMPLES</span></span>

### <span data-ttu-id="63f54-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="63f54-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="63f54-111">Ez a parancs ellenőrzi a megadott SQL-adatbázis meglétét.</span><span class="sxs-lookup"><span data-stu-id="63f54-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="63f54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63f54-112">PARAMETERS</span></span>

### <span data-ttu-id="63f54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f54-113">-DefaultProfile</span></span>
<span data-ttu-id="63f54-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63f54-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f54-115">-Name</span><span class="sxs-lookup"><span data-stu-id="63f54-115">-Name</span></span>
<span data-ttu-id="63f54-116">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="63f54-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="63f54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f54-117">-ResourceGroupName</span></span>
<span data-ttu-id="63f54-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="63f54-118">Resource group name.</span></span>

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

### <span data-ttu-id="63f54-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="63f54-119">-WorkspaceName</span></span>
<span data-ttu-id="63f54-120">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="63f54-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="63f54-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="63f54-121">-WorkspaceObject</span></span>
<span data-ttu-id="63f54-122">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="63f54-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="63f54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f54-123">CommonParameters</span></span>
<span data-ttu-id="63f54-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f54-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63f54-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f54-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63f54-126">INPUTS</span></span>

### <span data-ttu-id="63f54-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="63f54-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="63f54-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63f54-128">OUTPUTS</span></span>

### <span data-ttu-id="63f54-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63f54-129">System.Boolean</span></span>

## <span data-ttu-id="63f54-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63f54-130">NOTES</span></span>

## <span data-ttu-id="63f54-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63f54-131">RELATED LINKS</span></span>
