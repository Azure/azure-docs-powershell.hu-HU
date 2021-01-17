---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337734"
---
# <span data-ttu-id="b76fa-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b76fa-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="b76fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b76fa-103">Regisztrál egy erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="b76fa-103">Registers a resource provider.</span></span>

## <span data-ttu-id="b76fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b76fa-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b76fa-105">DESCRIPTION</span></span>
<span data-ttu-id="b76fa-106">A **Register-AzResourceProvider** parancsmag regisztrál egy Azure-erőforrásszolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="b76fa-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="b76fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b76fa-107">EXAMPLES</span></span>

### <span data-ttu-id="b76fa-108">1. példa: Szolgáltató regisztrálása</span><span class="sxs-lookup"><span data-stu-id="b76fa-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="b76fa-109">Ezzel regisztrálja a Microsoft.Network szolgáltatót a fiókjához.</span><span class="sxs-lookup"><span data-stu-id="b76fa-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="b76fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b76fa-110">PARAMETERS</span></span>

### <span data-ttu-id="b76fa-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b76fa-111">-ApiVersion</span></span>
<span data-ttu-id="b76fa-112">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76fa-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b76fa-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="b76fa-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b76fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76fa-114">-DefaultProfile</span></span>
<span data-ttu-id="b76fa-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b76fa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b76fa-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="b76fa-116">-Pre</span></span>
<span data-ttu-id="b76fa-117">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="b76fa-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b76fa-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b76fa-118">-ProviderNamespace</span></span>
<span data-ttu-id="b76fa-119">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b76fa-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="b76fa-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b76fa-120">-Confirm</span></span>
<span data-ttu-id="b76fa-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b76fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76fa-122">-WhatIf</span></span>
<span data-ttu-id="b76fa-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b76fa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76fa-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b76fa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76fa-125">CommonParameters</span></span>
<span data-ttu-id="b76fa-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76fa-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b76fa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76fa-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b76fa-128">INPUTS</span></span>

### <span data-ttu-id="b76fa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b76fa-129">System.String</span></span>

## <span data-ttu-id="b76fa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b76fa-130">OUTPUTS</span></span>

### <span data-ttu-id="b76fa-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b76fa-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="b76fa-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b76fa-132">NOTES</span></span>

## <span data-ttu-id="b76fa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b76fa-133">RELATED LINKS</span></span>

[<span data-ttu-id="b76fa-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b76fa-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="b76fa-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b76fa-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


