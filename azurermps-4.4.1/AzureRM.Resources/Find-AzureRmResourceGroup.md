---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494703"
---
# <span data-ttu-id="92498-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92498-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="92498-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92498-102">SYNOPSIS</span></span>
<span data-ttu-id="92498-103">Erőforráscsoportok keresése</span><span class="sxs-lookup"><span data-stu-id="92498-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92498-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92498-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92498-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92498-105">DESCRIPTION</span></span>
<span data-ttu-id="92498-106">A **Find-AzureRmResourceGroup** parancsmag a megadott paraméterekkel keres erőforrás-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="92498-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="92498-107">Példák</span><span class="sxs-lookup"><span data-stu-id="92498-107">EXAMPLES</span></span>

### <span data-ttu-id="92498-108">Példa 1: a minden erőforráscsoport keresése</span><span class="sxs-lookup"><span data-stu-id="92498-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="92498-109">Ez a parancs minden erőforráscsoport számára megkeresi a csoportot.</span><span class="sxs-lookup"><span data-stu-id="92498-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="92498-110">2. példa: erőforráscsoportok keresése címke neve szerint</span><span class="sxs-lookup"><span data-stu-id="92498-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="92498-111">Ez a parancs a testtag nevű címkét tartalmazó összes erőforráscsoportot megkeresi.</span><span class="sxs-lookup"><span data-stu-id="92498-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="92498-112">3. példa: erőforráscsoportok keresése a név és az érték címke szerint</span><span class="sxs-lookup"><span data-stu-id="92498-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="92498-113">Ez a parancs minden olyan erőforráscsoportot megkeresi, amely a testtag nevű címkével és a testval értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="92498-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="92498-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92498-114">PARAMETERS</span></span>

### <span data-ttu-id="92498-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="92498-115">-ApiVersion</span></span>
<span data-ttu-id="92498-116">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92498-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="92498-117">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="92498-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="92498-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="92498-118">-Pre</span></span>
<span data-ttu-id="92498-119">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="92498-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="92498-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="92498-120">-Tag</span></span>
<span data-ttu-id="92498-121">A címke adatait kivonatoló táblázatként adja meg az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="92498-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="92498-122">Használja az alábbi formátumokat:</span><span class="sxs-lookup"><span data-stu-id="92498-122">Use the following formats:</span></span>

<span data-ttu-id="92498-123">@ {tagName = $null} vagy @ {tagName = "tagValue"}.</span><span class="sxs-lookup"><span data-stu-id="92498-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92498-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92498-124">-DefaultProfile</span></span>
<span data-ttu-id="92498-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92498-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92498-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92498-126">CommonParameters</span></span>
<span data-ttu-id="92498-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92498-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92498-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92498-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92498-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92498-129">INPUTS</span></span>

## <span data-ttu-id="92498-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92498-130">OUTPUTS</span></span>

### <span data-ttu-id="92498-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="92498-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="92498-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92498-132">NOTES</span></span>

## <span data-ttu-id="92498-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92498-133">RELATED LINKS</span></span>

