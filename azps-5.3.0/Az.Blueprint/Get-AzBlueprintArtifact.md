---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480984"
---
# <span data-ttu-id="08ea3-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="08ea3-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="08ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="08ea3-103">Az összetevők lekérése a tervrajz-definícióból</span><span class="sxs-lookup"><span data-stu-id="08ea3-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="08ea3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08ea3-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08ea3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="08ea3-106">Az összetevők lekérése a tervrajz-definícióból</span><span class="sxs-lookup"><span data-stu-id="08ea3-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="08ea3-107">Ha nincs megadva tervrajz-definíciós verzió, a program beolvassa a vázlatverziót.</span><span class="sxs-lookup"><span data-stu-id="08ea3-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="08ea3-108">Abban az esetben, ha nincs piszkozat verzió, a legújabb közzétett tervdefiníciót ad vissza a program.</span><span class="sxs-lookup"><span data-stu-id="08ea3-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="08ea3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08ea3-109">EXAMPLES</span></span>

### <span data-ttu-id="08ea3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="08ea3-110">Example 1</span></span>
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

<span data-ttu-id="08ea3-111">Az összetevők lekérése egy tervrajz-definícióból.</span><span class="sxs-lookup"><span data-stu-id="08ea3-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="08ea3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08ea3-112">PARAMETERS</span></span>

### <span data-ttu-id="08ea3-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="08ea3-113">-Blueprint</span></span>
<span data-ttu-id="08ea3-114">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="08ea3-114">Blueprint object.</span></span>

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

### <span data-ttu-id="08ea3-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="08ea3-115">-BlueprintVersion</span></span>
<span data-ttu-id="08ea3-116">Annak a tervrajznak a verziója, amelyből ki lehet szerezni az ábrákat.</span><span class="sxs-lookup"><span data-stu-id="08ea3-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="08ea3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ea3-117">-DefaultProfile</span></span>
<span data-ttu-id="08ea3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08ea3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08ea3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="08ea3-119">-Name</span></span>
<span data-ttu-id="08ea3-120">Az összetevő neve</span><span class="sxs-lookup"><span data-stu-id="08ea3-120">Name of the artifact</span></span>

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

### <span data-ttu-id="08ea3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ea3-121">CommonParameters</span></span>
<span data-ttu-id="08ea3-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ea3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ea3-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08ea3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ea3-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08ea3-124">INPUTS</span></span>

### <span data-ttu-id="08ea3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="08ea3-125">System.String</span></span>

### <span data-ttu-id="08ea3-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="08ea3-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="08ea3-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="08ea3-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="08ea3-128">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="08ea3-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="08ea3-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="08ea3-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="08ea3-130">System.String[]</span><span class="sxs-lookup"><span data-stu-id="08ea3-130">System.String[]</span></span>

## <span data-ttu-id="08ea3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08ea3-131">OUTPUTS</span></span>

### <span data-ttu-id="08ea3-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="08ea3-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="08ea3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08ea3-133">NOTES</span></span>

## <span data-ttu-id="08ea3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08ea3-134">RELATED LINKS</span></span>
