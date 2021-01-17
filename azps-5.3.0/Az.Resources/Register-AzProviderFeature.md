---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466431"
---
# <span data-ttu-id="6d6cc-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6d6cc-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="6d6cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6cc-103">Regisztrál egy Azure-szolgáltató funkciót a fiókjában.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="6d6cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d6cc-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d6cc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d6cc-105">DESCRIPTION</span></span>
<span data-ttu-id="6d6cc-106">A **Register-AzProviderFeature parancsmag** regisztrál egy Azure-szolgáltató funkciót a fiókjában.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="6d6cc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d6cc-107">EXAMPLES</span></span>

### <span data-ttu-id="6d6cc-108">1. példa: Funkció regisztrálása</span><span class="sxs-lookup"><span data-stu-id="6d6cc-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="6d6cc-109">Ez hozzáadja a Microsoft.Network AllowApplicationSecurityGroups funkcióját a fiókjához.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="6d6cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d6cc-110">PARAMETERS</span></span>

### <span data-ttu-id="6d6cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6cc-111">-DefaultProfile</span></span>
<span data-ttu-id="6d6cc-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6d6cc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d6cc-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="6d6cc-113">-FeatureName</span></span>
<span data-ttu-id="6d6cc-114">A parancsmag által regisztrált szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="6d6cc-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6d6cc-115">-ProviderNamespace</span></span>
<span data-ttu-id="6d6cc-116">Megadja azt a névteret, amelyhez ez a parancsmag szolgáltatói funkciót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="6d6cc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d6cc-117">-Confirm</span></span>
<span data-ttu-id="6d6cc-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6cc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6cc-119">-WhatIf</span></span>
<span data-ttu-id="6d6cc-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6cc-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6cc-122">CommonParameters</span></span>
<span data-ttu-id="6d6cc-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d6cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6cc-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d6cc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6cc-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d6cc-125">INPUTS</span></span>

### <span data-ttu-id="6d6cc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6d6cc-126">System.String</span></span>

## <span data-ttu-id="6d6cc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d6cc-127">OUTPUTS</span></span>

### <span data-ttu-id="6d6cc-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6d6cc-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="6d6cc-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d6cc-129">NOTES</span></span>

## <span data-ttu-id="6d6cc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d6cc-130">RELATED LINKS</span></span>

[<span data-ttu-id="6d6cc-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6d6cc-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


