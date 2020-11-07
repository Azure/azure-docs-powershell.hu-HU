---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: de2a213122f756d87255be6195759e467f64b428
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838106"
---
# <span data-ttu-id="4ad93-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4ad93-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="4ad93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ad93-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad93-103">Az erőforrás-szolgáltató regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="4ad93-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="4ad93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ad93-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ad93-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad93-106">A **unregister-AzResourceProvider** parancsmag egy Azure Resource Provider bejegyzésének törlése.</span><span class="sxs-lookup"><span data-stu-id="4ad93-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="4ad93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ad93-107">EXAMPLES</span></span>

## <span data-ttu-id="4ad93-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ad93-108">PARAMETERS</span></span>

### <span data-ttu-id="4ad93-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4ad93-109">-ApiVersion</span></span>
<span data-ttu-id="4ad93-110">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ad93-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4ad93-111">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="4ad93-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4ad93-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad93-112">-DefaultProfile</span></span>
<span data-ttu-id="4ad93-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ad93-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ad93-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="4ad93-114">-Pre</span></span>
<span data-ttu-id="4ad93-115">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4ad93-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4ad93-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4ad93-116">-ProviderNamespace</span></span>
<span data-ttu-id="4ad93-117">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ad93-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="4ad93-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ad93-118">-Confirm</span></span>
<span data-ttu-id="4ad93-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ad93-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad93-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad93-120">-WhatIf</span></span>
<span data-ttu-id="4ad93-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ad93-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad93-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ad93-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad93-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad93-123">CommonParameters</span></span>
<span data-ttu-id="4ad93-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ad93-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad93-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad93-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad93-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad93-126">INPUTS</span></span>

### <span data-ttu-id="4ad93-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4ad93-127">System.String</span></span>

## <span data-ttu-id="4ad93-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad93-128">OUTPUTS</span></span>

### <span data-ttu-id="4ad93-129">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4ad93-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="4ad93-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ad93-130">NOTES</span></span>

## <span data-ttu-id="4ad93-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ad93-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ad93-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4ad93-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="4ad93-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4ad93-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


