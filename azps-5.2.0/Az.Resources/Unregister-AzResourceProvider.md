---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345041"
---
# <span data-ttu-id="6daa9-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6daa9-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="6daa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6daa9-102">SYNOPSIS</span></span>
<span data-ttu-id="6daa9-103">Erőforrás-szolgáltató regisztrációjának a visszaszava.</span><span class="sxs-lookup"><span data-stu-id="6daa9-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="6daa9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6daa9-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6daa9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6daa9-105">DESCRIPTION</span></span>
<span data-ttu-id="6daa9-106">A **Unregister-AzResourceProvider** parancsmag nem regisztrál egy Azure-erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="6daa9-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="6daa9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6daa9-107">EXAMPLES</span></span>

### <span data-ttu-id="6daa9-108">1. példa: Erőforrás-szolgáltató regisztrációjának megszűrése a ProviderNamespace szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="6daa9-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="6daa9-109">Ez a parancs a "Microsoft.support" erőforrásszolgáltatót nem regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="6daa9-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="6daa9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6daa9-110">PARAMETERS</span></span>

### <span data-ttu-id="6daa9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6daa9-111">-ApiVersion</span></span>
<span data-ttu-id="6daa9-112">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="6daa9-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6daa9-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="6daa9-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6daa9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6daa9-114">-DefaultProfile</span></span>
<span data-ttu-id="6daa9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6daa9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6daa9-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="6daa9-116">-Pre</span></span>
<span data-ttu-id="6daa9-117">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="6daa9-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6daa9-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6daa9-118">-ProviderNamespace</span></span>
<span data-ttu-id="6daa9-119">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6daa9-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="6daa9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6daa9-120">-Confirm</span></span>
<span data-ttu-id="6daa9-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6daa9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6daa9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6daa9-122">-WhatIf</span></span>
<span data-ttu-id="6daa9-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6daa9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6daa9-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6daa9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6daa9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6daa9-125">CommonParameters</span></span>
<span data-ttu-id="6daa9-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6daa9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6daa9-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6daa9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6daa9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6daa9-128">INPUTS</span></span>

### <span data-ttu-id="6daa9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6daa9-129">System.String</span></span>

## <span data-ttu-id="6daa9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6daa9-130">OUTPUTS</span></span>

### <span data-ttu-id="6daa9-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6daa9-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="6daa9-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6daa9-132">NOTES</span></span>

## <span data-ttu-id="6daa9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6daa9-133">RELATED LINKS</span></span>

[<span data-ttu-id="6daa9-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6daa9-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="6daa9-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6daa9-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


