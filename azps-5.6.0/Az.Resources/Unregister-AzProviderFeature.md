---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 30c315240cf667db37c6c605cda093fe7811a3ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922346"
---
# <span data-ttu-id="d2249-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d2249-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="d2249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2249-102">SYNOPSIS</span></span>
<span data-ttu-id="d2249-103">Az Azure-szolgáltatói szolgáltatások regisztrációjának a regisztrációját a fiókjában.</span><span class="sxs-lookup"><span data-stu-id="d2249-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d2249-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2249-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2249-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2249-105">DESCRIPTION</span></span>
<span data-ttu-id="d2249-106">A **Unregister-AzProviderFeature** parancsmag megszüntet egy Azure-szolgáltatói funkciót a fiókjában.</span><span class="sxs-lookup"><span data-stu-id="d2249-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d2249-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2249-107">EXAMPLES</span></span>

### <span data-ttu-id="d2249-108">1. példa: Funkció regisztrációjának visszaszava</span><span class="sxs-lookup"><span data-stu-id="d2249-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="d2249-109">Ezzel a fiókból nem regisztrálja a Microsoft.Network AllowApplicationSecurityGroups funkcióját.</span><span class="sxs-lookup"><span data-stu-id="d2249-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="d2249-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2249-110">PARAMETERS</span></span>

### <span data-ttu-id="d2249-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2249-111">-DefaultProfile</span></span>
<span data-ttu-id="d2249-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2249-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2249-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="d2249-113">-FeatureName</span></span>
<span data-ttu-id="d2249-114">A funkció neve.</span><span class="sxs-lookup"><span data-stu-id="d2249-114">The feature name.</span></span>

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

### <span data-ttu-id="d2249-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d2249-115">-ProviderNamespace</span></span>
<span data-ttu-id="d2249-116">Az erőforrás-szolgáltató névtere.</span><span class="sxs-lookup"><span data-stu-id="d2249-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="d2249-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2249-117">-Confirm</span></span>
<span data-ttu-id="d2249-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2249-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2249-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2249-119">-WhatIf</span></span>
<span data-ttu-id="d2249-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2249-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2249-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2249-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2249-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2249-122">CommonParameters</span></span>
<span data-ttu-id="d2249-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2249-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2249-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2249-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2249-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2249-125">INPUTS</span></span>

### <span data-ttu-id="d2249-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d2249-126">System.String</span></span>

## <span data-ttu-id="d2249-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2249-127">OUTPUTS</span></span>

### <span data-ttu-id="d2249-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d2249-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="d2249-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2249-129">NOTES</span></span>

## <span data-ttu-id="d2249-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2249-130">RELATED LINKS</span></span>