---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 875dd42cb0aefd6d6422d99463cd56ace720411a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678930"
---
# <span data-ttu-id="dfd76-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="dfd76-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="dfd76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfd76-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd76-103">Az erőforrás-szolgáltató regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="dfd76-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfd76-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd76-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfd76-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd76-106">A **unregister-AzureRmResourceProvider** parancsmag egy Azure Resource Provider bejegyzésének törlése.</span><span class="sxs-lookup"><span data-stu-id="dfd76-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="dfd76-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dfd76-107">EXAMPLES</span></span>

## <span data-ttu-id="dfd76-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfd76-108">PARAMETERS</span></span>

### <span data-ttu-id="dfd76-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dfd76-109">-ApiVersion</span></span>
<span data-ttu-id="dfd76-110">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfd76-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="dfd76-111">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="dfd76-111">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd76-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd76-112">-DefaultProfile</span></span>
<span data-ttu-id="dfd76-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dfd76-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd76-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="dfd76-114">-Pre</span></span>
<span data-ttu-id="dfd76-115">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="dfd76-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd76-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="dfd76-116">-ProviderNamespace</span></span>
<span data-ttu-id="dfd76-117">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfd76-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="dfd76-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfd76-118">-Confirm</span></span>
<span data-ttu-id="dfd76-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfd76-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd76-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd76-120">-WhatIf</span></span>
<span data-ttu-id="dfd76-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dfd76-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd76-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfd76-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd76-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd76-123">CommonParameters</span></span>
<span data-ttu-id="dfd76-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfd76-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd76-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd76-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd76-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfd76-126">INPUTS</span></span>

### <span data-ttu-id="dfd76-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="dfd76-127">None</span></span>
<span data-ttu-id="dfd76-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dfd76-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dfd76-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfd76-129">OUTPUTS</span></span>

### <span data-ttu-id="dfd76-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSResourceProvider]</span><span class="sxs-lookup"><span data-stu-id="dfd76-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="dfd76-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfd76-131">NOTES</span></span>

## <span data-ttu-id="dfd76-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfd76-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfd76-133">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="dfd76-133">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="dfd76-134">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="dfd76-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


