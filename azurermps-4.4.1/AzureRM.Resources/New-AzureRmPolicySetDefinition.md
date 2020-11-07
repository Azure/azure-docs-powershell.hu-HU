---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9c860726993929a6618706037b5c53dff14a68ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679339"
---
# <span data-ttu-id="1f3e5-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1f3e5-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="1f3e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3e5-103">Házirend-készlet definícióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f3e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f3e5-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f3e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f3e5-105">DESCRIPTION</span></span>
<span data-ttu-id="1f3e5-106">A **New-AzureRmPolicySetDefinition** parancsmag létrehoz egy házirend-készlet definícióját.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="1f3e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f3e5-107">EXAMPLES</span></span>

### <span data-ttu-id="1f3e5-108">Példa 1: a házirend-készlet definíciójának létrehozása egy házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="1f3e5-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="1f3e5-109">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciós definíciót, amely a C:\VMPolicy.jsban megadott házirend-definíciókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="1f3e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f3e5-110">PARAMETERS</span></span>

### <span data-ttu-id="1f3e5-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f3e5-111">-ApiVersion</span></span>
<span data-ttu-id="1f3e5-112">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f3e5-113">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1f3e5-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1f3e5-114">-Description</span></span>
<span data-ttu-id="1f3e5-115">A házirend-készlet definíciójának leírása.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-115">The description for policy set definition.</span></span>

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

### <span data-ttu-id="1f3e5-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f3e5-116">-DisplayName</span></span>
<span data-ttu-id="1f3e5-117">A házirend-készlet definíciójának megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-117">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="1f3e5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f3e5-118">-Name</span></span>
<span data-ttu-id="1f3e5-119">A Policy set definition név.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-119">The policy set definition name.</span></span>

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

### <span data-ttu-id="1f3e5-120">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="1f3e5-120">-Parameter</span></span>
<span data-ttu-id="1f3e5-121">A Parameters deklaráció a házirend-készlet definíciójában.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-121">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="1f3e5-122">Ez lehet a Parameters deklarációt vagy a Parameters deklarációt karakterláncként tartalmazó fájlnév elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-122">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="1f3e5-123">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f3e5-123">-PolicyDefinition</span></span>
<span data-ttu-id="1f3e5-124">A házirend-készlet definíciója.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-124">The policy set definition.</span></span> <span data-ttu-id="1f3e5-125">Ez lehet egy elérési út a házirend-definíciókat tartalmazó fájlnévhez vagy a házirend-definíció karakterláncként való beállításához.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-125">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="1f3e5-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f3e5-126">-Pre</span></span>
<span data-ttu-id="1f3e5-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1f3e5-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f3e5-128">-Confirm</span></span>
<span data-ttu-id="1f3e5-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f3e5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3e5-130">-DefaultProfile</span></span>
<span data-ttu-id="1f3e5-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f3e5-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1f3e5-132">-Metadata</span></span>
<span data-ttu-id="1f3e5-133">A házirend-készlet definíciójának metaadatai.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-133">The metadata for policy set definition.</span></span> <span data-ttu-id="1f3e5-134">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="1f3e5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f3e5-135">-WhatIf</span></span>
<span data-ttu-id="1f3e5-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f3e5-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f3e5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f3e5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3e5-138">CommonParameters</span></span>
<span data-ttu-id="1f3e5-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f3e5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3e5-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f3e5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3e5-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f3e5-141">INPUTS</span></span>

### <span data-ttu-id="1f3e5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1f3e5-142">System.String</span></span>

## <span data-ttu-id="1f3e5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f3e5-143">OUTPUTS</span></span>

### <span data-ttu-id="1f3e5-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1f3e5-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f3e5-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f3e5-145">NOTES</span></span>

## <span data-ttu-id="1f3e5-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f3e5-146">RELATED LINKS</span></span>

