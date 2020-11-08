---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186110"
---
# <span data-ttu-id="b8e17-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b8e17-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b8e17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8e17-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e17-103">A Blueprint-fájlt JSON formátumban importálhatja a Blueprint objektumba, és mentheti azt a megadott előfizetés vagy kezelési csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="b8e17-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b8e17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8e17-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e17-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8e17-105">DESCRIPTION</span></span>
<span data-ttu-id="b8e17-106">A tervrajzok definícióját importálhatja a leletekkel.</span><span class="sxs-lookup"><span data-stu-id="b8e17-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="b8e17-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8e17-107">EXAMPLES</span></span>

### <span data-ttu-id="b8e17-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b8e17-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="b8e17-109">A terv definícióját importálhatja a leletekkel, és az előfizetésben is mentheti.</span><span class="sxs-lookup"><span data-stu-id="b8e17-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="b8e17-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8e17-110">PARAMETERS</span></span>

### <span data-ttu-id="b8e17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e17-111">-DefaultProfile</span></span>
<span data-ttu-id="b8e17-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8e17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e17-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b8e17-113">-Force</span></span>
<span data-ttu-id="b8e17-114">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8e17-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b8e17-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="b8e17-115">-IncludeSubFolders</span></span>
<span data-ttu-id="b8e17-116">Ha a True értékre van állítva, a program az almappákban található tárgyat is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="b8e17-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="b8e17-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b8e17-117">-InputPath</span></span>
<span data-ttu-id="b8e17-118">A sablonban lévő JSON-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="b8e17-118">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e17-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b8e17-119">-ManagementGroupId</span></span>
<span data-ttu-id="b8e17-120">A felügyeleti csoport azonosítóját, ahol a tervrajz definícióját menti vagy menti a program.</span><span class="sxs-lookup"><span data-stu-id="b8e17-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="b8e17-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8e17-121">-Name</span></span>
<span data-ttu-id="b8e17-122">Terv definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b8e17-122">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e17-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8e17-123">-PassThru</span></span>
<span data-ttu-id="b8e17-124">Ha be van állítva, a parancsmag egy olyan objektumot ad vissza, amely az importált terv definícióját jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b8e17-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="b8e17-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b8e17-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b8e17-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8e17-126">-SubscriptionId</span></span>
<span data-ttu-id="b8e17-127">Az előfizetési azonosító, amelyben a terv definíciója vagy mentésére kerül.</span><span class="sxs-lookup"><span data-stu-id="b8e17-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="b8e17-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8e17-128">-Confirm</span></span>
<span data-ttu-id="b8e17-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8e17-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e17-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e17-130">-WhatIf</span></span>
<span data-ttu-id="b8e17-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8e17-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8e17-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8e17-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e17-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e17-133">CommonParameters</span></span>
<span data-ttu-id="b8e17-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8e17-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e17-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8e17-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e17-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8e17-136">INPUTS</span></span>

### <span data-ttu-id="b8e17-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b8e17-137">System.String</span></span>

## <span data-ttu-id="b8e17-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8e17-138">OUTPUTS</span></span>

### <span data-ttu-id="b8e17-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b8e17-139">System.String</span></span>

## <span data-ttu-id="b8e17-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8e17-140">NOTES</span></span>

## <span data-ttu-id="b8e17-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8e17-141">RELATED LINKS</span></span>
