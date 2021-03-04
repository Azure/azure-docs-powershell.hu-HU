---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 8fe856b1b8b710c1db139474f15d432f32c2652a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933738"
---
# <span data-ttu-id="451e0-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="451e0-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="451e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="451e0-102">SYNOPSIS</span></span>
<span data-ttu-id="451e0-103">Regisztrál egy erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="451e0-103">Registers a resource provider.</span></span>

## <span data-ttu-id="451e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="451e0-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="451e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="451e0-105">DESCRIPTION</span></span>
<span data-ttu-id="451e0-106">A **Register-AzResourceProvider** parancsmag regisztrál egy Azure-erőforrásszolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="451e0-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="451e0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="451e0-107">EXAMPLES</span></span>

### <span data-ttu-id="451e0-108">1. példa: Szolgáltató regisztrálása</span><span class="sxs-lookup"><span data-stu-id="451e0-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="451e0-109">Ezzel regisztrálja a Microsoft.Network szolgáltatót a fiókjához.</span><span class="sxs-lookup"><span data-stu-id="451e0-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="451e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="451e0-110">PARAMETERS</span></span>

### <span data-ttu-id="451e0-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="451e0-111">-ApiVersion</span></span>
<span data-ttu-id="451e0-112">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="451e0-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="451e0-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="451e0-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="451e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451e0-114">-DefaultProfile</span></span>
<span data-ttu-id="451e0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="451e0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="451e0-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="451e0-116">-Pre</span></span>
<span data-ttu-id="451e0-117">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="451e0-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="451e0-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="451e0-118">-ProviderNamespace</span></span>
<span data-ttu-id="451e0-119">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="451e0-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="451e0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="451e0-120">-Confirm</span></span>
<span data-ttu-id="451e0-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="451e0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="451e0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="451e0-122">-WhatIf</span></span>
<span data-ttu-id="451e0-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="451e0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="451e0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="451e0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="451e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451e0-125">CommonParameters</span></span>
<span data-ttu-id="451e0-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451e0-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="451e0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451e0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="451e0-128">INPUTS</span></span>

### <span data-ttu-id="451e0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="451e0-129">System.String</span></span>

## <span data-ttu-id="451e0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="451e0-130">OUTPUTS</span></span>

### <span data-ttu-id="451e0-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="451e0-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="451e0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="451e0-132">NOTES</span></span>

## <span data-ttu-id="451e0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="451e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="451e0-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="451e0-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="451e0-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="451e0-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


