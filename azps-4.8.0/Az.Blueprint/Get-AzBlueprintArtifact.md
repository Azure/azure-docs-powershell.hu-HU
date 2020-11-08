---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024189"
---
# <span data-ttu-id="3a37b-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="3a37b-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="3a37b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a37b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a37b-103">A tervrajz-definícióból származó leletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="3a37b-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="3a37b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a37b-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a37b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a37b-105">DESCRIPTION</span></span>
<span data-ttu-id="3a37b-106">A tervrajz-definícióból származó leletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="3a37b-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="3a37b-107">Ha a Blueprint definition definition verzió nincs megadva, a Piszkozat verzió lekérése.</span><span class="sxs-lookup"><span data-stu-id="3a37b-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="3a37b-108">Abban az esetben, ha nincs Piszkozat verzió, a legújabb közzétett terv definícióját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="3a37b-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="3a37b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3a37b-109">EXAMPLES</span></span>

### <span data-ttu-id="3a37b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a37b-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="3a37b-111">A Blueprint-definícióból származó leletek lekérése</span><span class="sxs-lookup"><span data-stu-id="3a37b-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="3a37b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a37b-112">PARAMETERS</span></span>

### <span data-ttu-id="3a37b-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="3a37b-113">-Blueprint</span></span>
<span data-ttu-id="3a37b-114">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="3a37b-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a37b-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="3a37b-115">-BlueprintVersion</span></span>
<span data-ttu-id="3a37b-116">A terv változata a leletek beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="3a37b-116">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a37b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a37b-117">-DefaultProfile</span></span>
<span data-ttu-id="3a37b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a37b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a37b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a37b-119">-Name</span></span>
<span data-ttu-id="3a37b-120">A tárgy neve</span><span class="sxs-lookup"><span data-stu-id="3a37b-120">Name of the artifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a37b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a37b-121">CommonParameters</span></span>
<span data-ttu-id="3a37b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a37b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a37b-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a37b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a37b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a37b-124">INPUTS</span></span>

### <span data-ttu-id="3a37b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3a37b-125">System.String</span></span>

### <span data-ttu-id="3a37b-126">Microsoft. Azure. commands. Blueprint. models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="3a37b-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="3a37b-127">Microsoft. Azure. commands. Blueprint. models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="3a37b-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="3a37b-128">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3a37b-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3a37b-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a37b-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3a37b-130">System. string []</span><span class="sxs-lookup"><span data-stu-id="3a37b-130">System.String[]</span></span>

## <span data-ttu-id="3a37b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a37b-131">OUTPUTS</span></span>

### <span data-ttu-id="3a37b-132">Microsoft. Azure. commands. Blueprint. models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3a37b-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="3a37b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a37b-133">NOTES</span></span>

## <span data-ttu-id="3a37b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a37b-134">RELATED LINKS</span></span>
