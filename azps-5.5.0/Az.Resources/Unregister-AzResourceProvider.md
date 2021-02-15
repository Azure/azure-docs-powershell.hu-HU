---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145922"
---
# <span data-ttu-id="2d41b-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2d41b-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="2d41b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d41b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d41b-103">Erőforrás-szolgáltató regisztrációjának a visszaszava.</span><span class="sxs-lookup"><span data-stu-id="2d41b-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="2d41b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d41b-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d41b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d41b-105">DESCRIPTION</span></span>
<span data-ttu-id="2d41b-106">A **Unregister-AzResourceProvider** parancsmag nem regisztrál egy Azure-erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="2d41b-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="2d41b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d41b-107">EXAMPLES</span></span>

### <span data-ttu-id="2d41b-108">1. példa: Erőforrás-szolgáltató regisztrációjának megszűrése a ProviderNamespace szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="2d41b-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="2d41b-109">Ez a parancs a "Microsoft.support" erőforrásszolgáltatót nem regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="2d41b-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="2d41b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d41b-110">PARAMETERS</span></span>

### <span data-ttu-id="2d41b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2d41b-111">-ApiVersion</span></span>
<span data-ttu-id="2d41b-112">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d41b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2d41b-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="2d41b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2d41b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d41b-114">-DefaultProfile</span></span>
<span data-ttu-id="2d41b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d41b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d41b-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d41b-116">-Pre</span></span>
<span data-ttu-id="2d41b-117">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="2d41b-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2d41b-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="2d41b-118">-ProviderNamespace</span></span>
<span data-ttu-id="2d41b-119">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d41b-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="2d41b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d41b-120">-Confirm</span></span>
<span data-ttu-id="2d41b-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2d41b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d41b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d41b-122">-WhatIf</span></span>
<span data-ttu-id="2d41b-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2d41b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d41b-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d41b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d41b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d41b-125">CommonParameters</span></span>
<span data-ttu-id="2d41b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d41b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d41b-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d41b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d41b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d41b-128">INPUTS</span></span>

### <span data-ttu-id="2d41b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2d41b-129">System.String</span></span>

## <span data-ttu-id="2d41b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d41b-130">OUTPUTS</span></span>

### <span data-ttu-id="2d41b-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2d41b-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="2d41b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d41b-132">NOTES</span></span>

## <span data-ttu-id="2d41b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d41b-133">RELATED LINKS</span></span>

[<span data-ttu-id="2d41b-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2d41b-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="2d41b-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2d41b-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


