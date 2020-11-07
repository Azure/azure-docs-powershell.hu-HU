---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849022"
---
# <span data-ttu-id="48515-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="48515-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="48515-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48515-102">SYNOPSIS</span></span>
<span data-ttu-id="48515-103">Az erőforrás-szolgáltató regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="48515-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48515-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48515-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48515-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48515-105">DESCRIPTION</span></span>
<span data-ttu-id="48515-106">A **unregister-AzureRmResourceProvider** parancsmag egy Azure Resource Provider bejegyzésének törlése.</span><span class="sxs-lookup"><span data-stu-id="48515-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="48515-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48515-107">EXAMPLES</span></span>

## <span data-ttu-id="48515-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48515-108">PARAMETERS</span></span>

### <span data-ttu-id="48515-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="48515-109">-ApiVersion</span></span>
<span data-ttu-id="48515-110">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="48515-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="48515-111">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="48515-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="48515-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48515-112">-DefaultProfile</span></span>
<span data-ttu-id="48515-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="48515-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48515-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="48515-114">-Pre</span></span>
<span data-ttu-id="48515-115">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="48515-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="48515-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="48515-116">-ProviderNamespace</span></span>
<span data-ttu-id="48515-117">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48515-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="48515-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48515-118">-Confirm</span></span>
<span data-ttu-id="48515-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48515-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48515-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48515-120">-WhatIf</span></span>
<span data-ttu-id="48515-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48515-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48515-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48515-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48515-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48515-123">CommonParameters</span></span>
<span data-ttu-id="48515-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48515-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48515-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48515-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48515-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48515-126">INPUTS</span></span>

## <span data-ttu-id="48515-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48515-127">OUTPUTS</span></span>

## <span data-ttu-id="48515-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48515-128">NOTES</span></span>

## <span data-ttu-id="48515-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48515-129">RELATED LINKS</span></span>

[<span data-ttu-id="48515-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="48515-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="48515-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="48515-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


