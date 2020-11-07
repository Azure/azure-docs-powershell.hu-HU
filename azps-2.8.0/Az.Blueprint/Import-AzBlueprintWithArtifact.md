---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667640"
---
# <span data-ttu-id="abbbd-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="abbbd-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="abbbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="abbbd-103">A Blueprint-fájlt JSON formátumban importálhatja a Blueprint objektumba, és mentheti azt a megadott előfizetés vagy kezelési csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="abbbd-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="abbbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abbbd-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abbbd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abbbd-105">DESCRIPTION</span></span>
<span data-ttu-id="abbbd-106">A tervrajzok definícióját importálhatja a leletekkel.</span><span class="sxs-lookup"><span data-stu-id="abbbd-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="abbbd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abbbd-107">EXAMPLES</span></span>

### <span data-ttu-id="abbbd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="abbbd-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="abbbd-109">A terv definícióját importálhatja a leletekkel, és az előfizetésben is mentheti.</span><span class="sxs-lookup"><span data-stu-id="abbbd-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="abbbd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abbbd-110">PARAMETERS</span></span>

### <span data-ttu-id="abbbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbbd-111">-DefaultProfile</span></span>
<span data-ttu-id="abbbd-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abbbd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abbbd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="abbbd-113">-Force</span></span>
<span data-ttu-id="abbbd-114">Ha a True értékre van állítva, akkor a végrehajtás nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abbbd-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="abbbd-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="abbbd-115">-InputPath</span></span>
<span data-ttu-id="abbbd-116">A sablonban lévő JSON-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="abbbd-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="abbbd-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="abbbd-117">-ManagementGroupId</span></span>
<span data-ttu-id="abbbd-118">A felügyeleti csoport azonosítóját, ahol a tervrajz definícióját menti vagy menti a program.</span><span class="sxs-lookup"><span data-stu-id="abbbd-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="abbbd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abbbd-119">-Name</span></span>
<span data-ttu-id="abbbd-120">Terv definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="abbbd-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="abbbd-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="abbbd-121">-SubscriptionId</span></span>
<span data-ttu-id="abbbd-122">Az előfizetési azonosító, amelyben a terv definíciója vagy mentésére kerül.</span><span class="sxs-lookup"><span data-stu-id="abbbd-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="abbbd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbbd-123">CommonParameters</span></span>
<span data-ttu-id="abbbd-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abbbd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="abbbd-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abbbd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbbd-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abbbd-126">INPUTS</span></span>

### <span data-ttu-id="abbbd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="abbbd-127">System.String</span></span>

## <span data-ttu-id="abbbd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abbbd-128">OUTPUTS</span></span>

### <span data-ttu-id="abbbd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="abbbd-129">System.String</span></span>

## <span data-ttu-id="abbbd-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abbbd-130">NOTES</span></span>

## <span data-ttu-id="abbbd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abbbd-131">RELATED LINKS</span></span>
