---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017463"
---
# <span data-ttu-id="88937-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="88937-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="88937-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88937-102">SYNOPSIS</span></span>
<span data-ttu-id="88937-103">A szinapszis-Analytics SQL-készlet létezésének ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="88937-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="88937-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88937-104">SYNTAX</span></span>

### <span data-ttu-id="88937-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88937-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88937-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88937-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88937-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="88937-107">DESCRIPTION</span></span>
<span data-ttu-id="88937-108">A **AzSynapseSqlPool** parancsmag a szinapszis-Analytics SQL-készlet fennállását vizsgálja.</span><span class="sxs-lookup"><span data-stu-id="88937-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="88937-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88937-109">EXAMPLES</span></span>

### <span data-ttu-id="88937-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88937-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="88937-111">Ez a parancs ellenőrzi a megadott SQL-készlet létezését.</span><span class="sxs-lookup"><span data-stu-id="88937-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="88937-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88937-112">PARAMETERS</span></span>

### <span data-ttu-id="88937-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88937-113">-DefaultProfile</span></span>
<span data-ttu-id="88937-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88937-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88937-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88937-115">-Name</span></span>
<span data-ttu-id="88937-116">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="88937-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="88937-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88937-117">-ResourceGroupName</span></span>
<span data-ttu-id="88937-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="88937-118">Resource group name.</span></span>

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

### <span data-ttu-id="88937-119">-Verzió</span><span class="sxs-lookup"><span data-stu-id="88937-119">-Version</span></span>
<span data-ttu-id="88937-120">A szinapszis SQL Pool verziója.</span><span class="sxs-lookup"><span data-stu-id="88937-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="88937-121">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="88937-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88937-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88937-122">-WorkspaceName</span></span>
<span data-ttu-id="88937-123">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="88937-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="88937-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88937-124">-WorkspaceObject</span></span>
<span data-ttu-id="88937-125">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="88937-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="88937-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88937-126">CommonParameters</span></span>
<span data-ttu-id="88937-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88937-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88937-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88937-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88937-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88937-129">INPUTS</span></span>

### <span data-ttu-id="88937-130">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="88937-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="88937-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88937-131">OUTPUTS</span></span>

### <span data-ttu-id="88937-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="88937-132">System.Object</span></span>
## <span data-ttu-id="88937-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88937-133">NOTES</span></span>

## <span data-ttu-id="88937-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88937-134">RELATED LINKS</span></span>
