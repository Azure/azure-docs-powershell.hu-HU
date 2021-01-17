---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345077"
---
# <span data-ttu-id="44c2e-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="44c2e-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="44c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="44c2e-103">Az Azure-szolgáltatói szolgáltatások regisztrációjának a regisztrációját a fiókjában.</span><span class="sxs-lookup"><span data-stu-id="44c2e-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="44c2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44c2e-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44c2e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="44c2e-106">A **Unregister-AzProviderFeature** parancsmag megszüntet egy Azure-szolgáltatói funkciót a fiókjában.</span><span class="sxs-lookup"><span data-stu-id="44c2e-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="44c2e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44c2e-107">EXAMPLES</span></span>

### <span data-ttu-id="44c2e-108">1. példa: Funkció regisztrációjának visszaszava</span><span class="sxs-lookup"><span data-stu-id="44c2e-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="44c2e-109">Ezzel a fiókból nem regisztrálja a Microsoft.Network AllowApplicationSecurityGroups szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="44c2e-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="44c2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44c2e-110">PARAMETERS</span></span>

### <span data-ttu-id="44c2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c2e-111">-DefaultProfile</span></span>
<span data-ttu-id="44c2e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44c2e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c2e-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="44c2e-113">-FeatureName</span></span>
<span data-ttu-id="44c2e-114">A funkció neve.</span><span class="sxs-lookup"><span data-stu-id="44c2e-114">The feature name.</span></span>

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

### <span data-ttu-id="44c2e-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="44c2e-115">-ProviderNamespace</span></span>
<span data-ttu-id="44c2e-116">Az erőforrás-szolgáltató névtere.</span><span class="sxs-lookup"><span data-stu-id="44c2e-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="44c2e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44c2e-117">-Confirm</span></span>
<span data-ttu-id="44c2e-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44c2e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c2e-119">-WhatIf</span></span>
<span data-ttu-id="44c2e-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44c2e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c2e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44c2e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c2e-122">CommonParameters</span></span>
<span data-ttu-id="44c2e-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c2e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c2e-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44c2e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c2e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44c2e-125">INPUTS</span></span>

### <span data-ttu-id="44c2e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="44c2e-126">System.String</span></span>

## <span data-ttu-id="44c2e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44c2e-127">OUTPUTS</span></span>

### <span data-ttu-id="44c2e-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="44c2e-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="44c2e-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44c2e-129">NOTES</span></span>

## <span data-ttu-id="44c2e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44c2e-130">RELATED LINKS</span></span>