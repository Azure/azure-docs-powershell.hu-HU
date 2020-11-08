---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185145"
---
# <span data-ttu-id="e9510-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9510-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="e9510-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9510-102">SYNOPSIS</span></span>
<span data-ttu-id="e9510-103">A szinapszis-Analytics SQL-adatbázis meglétének ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="e9510-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e9510-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9510-104">SYNTAX</span></span>

### <span data-ttu-id="e9510-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9510-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9510-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9510-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9510-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9510-107">DESCRIPTION</span></span>
<span data-ttu-id="e9510-108">A **AzSynapseSqlDatabase** parancsmag a szinapszis-statisztika SQL-adatbázis létezését ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="e9510-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e9510-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e9510-109">EXAMPLES</span></span>

### <span data-ttu-id="e9510-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e9510-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="e9510-111">Ez a parancs ellenőrzi a megadott SQL-adatbázis létezését.</span><span class="sxs-lookup"><span data-stu-id="e9510-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="e9510-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9510-112">PARAMETERS</span></span>

### <span data-ttu-id="e9510-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9510-113">-DefaultProfile</span></span>
<span data-ttu-id="e9510-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9510-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9510-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e9510-115">-Name</span></span>
<span data-ttu-id="e9510-116">A szinapszis SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e9510-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e9510-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9510-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9510-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e9510-118">Resource group name.</span></span>

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

### <span data-ttu-id="e9510-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9510-119">-WorkspaceName</span></span>
<span data-ttu-id="e9510-120">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="e9510-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9510-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9510-121">-WorkspaceObject</span></span>
<span data-ttu-id="e9510-122">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e9510-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9510-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9510-123">CommonParameters</span></span>
<span data-ttu-id="e9510-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9510-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9510-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e9510-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9510-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9510-126">INPUTS</span></span>

### <span data-ttu-id="e9510-127">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9510-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e9510-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9510-128">OUTPUTS</span></span>

### <span data-ttu-id="e9510-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9510-129">System.Boolean</span></span>

## <span data-ttu-id="e9510-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9510-130">NOTES</span></span>

## <span data-ttu-id="e9510-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9510-131">RELATED LINKS</span></span>