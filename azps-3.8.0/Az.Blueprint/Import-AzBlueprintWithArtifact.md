---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 7a1778ce107e9753f78876aff3a2dfba19e138e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013686"
---
# <span data-ttu-id="e7f45-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="e7f45-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="e7f45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7f45-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f45-103">A Blueprint-fájlt JSON formátumban importálhatja a Blueprint objektumba, és mentheti azt a megadott előfizetés vagy kezelési csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="e7f45-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="e7f45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7f45-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7f45-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7f45-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f45-106">A tervrajzok definícióját importálhatja a leletekkel.</span><span class="sxs-lookup"><span data-stu-id="e7f45-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="e7f45-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e7f45-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f45-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7f45-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="e7f45-109">A terv definícióját importálhatja a leletekkel, és az előfizetésben is mentheti.</span><span class="sxs-lookup"><span data-stu-id="e7f45-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="e7f45-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7f45-110">PARAMETERS</span></span>

### <span data-ttu-id="e7f45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f45-111">-DefaultProfile</span></span>
<span data-ttu-id="e7f45-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7f45-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7f45-113">-Force</span></span>
<span data-ttu-id="e7f45-114">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7f45-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="e7f45-115">-IncludeSubFolders</span></span>
<span data-ttu-id="e7f45-116">Ha a True értékre van állítva, a program az almappákban található tárgyat is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="e7f45-116">When set to true, artifact in the subfolders will be included.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="e7f45-117">-InputPath</span></span>
<span data-ttu-id="e7f45-118">A sablonban lévő JSON-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="e7f45-118">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e7f45-119">-ManagementGroupId</span></span>
<span data-ttu-id="e7f45-120">A felügyeleti csoport azonosítóját, ahol a tervrajz definícióját menti vagy menti a program.</span><span class="sxs-lookup"><span data-stu-id="e7f45-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7f45-121">-Name</span></span>
<span data-ttu-id="e7f45-122">Terv definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="e7f45-122">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7f45-123">-SubscriptionId</span></span>
<span data-ttu-id="e7f45-124">Az előfizetési azonosító, amelyben a terv definíciója vagy mentésére kerül.</span><span class="sxs-lookup"><span data-stu-id="e7f45-124">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f45-125">CommonParameters</span></span>
<span data-ttu-id="e7f45-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7f45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7f45-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f45-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f45-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f45-128">INPUTS</span></span>

### <span data-ttu-id="e7f45-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f45-129">System.String</span></span>

## <span data-ttu-id="e7f45-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f45-130">OUTPUTS</span></span>

### <span data-ttu-id="e7f45-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f45-131">System.String</span></span>

## <span data-ttu-id="e7f45-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7f45-132">NOTES</span></span>

## <span data-ttu-id="e7f45-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7f45-133">RELATED LINKS</span></span>
