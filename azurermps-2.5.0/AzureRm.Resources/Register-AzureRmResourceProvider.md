---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: c3459a07eb6f92e4ec30b5018efc41ff13e1c41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850234"
---
# <span data-ttu-id="497fe-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="497fe-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="497fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="497fe-102">SYNOPSIS</span></span>
<span data-ttu-id="497fe-103">Erőforrás-szolgáltató regisztrálása.</span><span class="sxs-lookup"><span data-stu-id="497fe-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="497fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="497fe-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="497fe-105">DESCRIPTION</span></span>
<span data-ttu-id="497fe-106">A **Register-AzureRmResourceProvider** parancsmag az Azure Resource providert regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="497fe-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="497fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="497fe-107">EXAMPLES</span></span>

### <span data-ttu-id="497fe-108">1. példa: szolgáltató regisztrálása</span><span class="sxs-lookup"><span data-stu-id="497fe-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="497fe-109">Ezzel a szolgáltatással regisztrálhatja a Microsoft. Network szolgáltatót a fiókjához.</span><span class="sxs-lookup"><span data-stu-id="497fe-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="497fe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="497fe-110">PARAMETERS</span></span>

### <span data-ttu-id="497fe-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="497fe-111">-ApiVersion</span></span>
<span data-ttu-id="497fe-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="497fe-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="497fe-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="497fe-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="497fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497fe-114">-DefaultProfile</span></span>
<span data-ttu-id="497fe-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="497fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="497fe-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="497fe-116">-Pre</span></span>
<span data-ttu-id="497fe-117">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="497fe-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="497fe-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="497fe-118">-ProviderNamespace</span></span>
<span data-ttu-id="497fe-119">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="497fe-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="497fe-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="497fe-120">-Confirm</span></span>
<span data-ttu-id="497fe-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="497fe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497fe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497fe-122">-WhatIf</span></span>
<span data-ttu-id="497fe-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="497fe-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497fe-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="497fe-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497fe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497fe-125">CommonParameters</span></span>
<span data-ttu-id="497fe-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="497fe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497fe-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497fe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497fe-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="497fe-128">INPUTS</span></span>

## <span data-ttu-id="497fe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="497fe-129">OUTPUTS</span></span>

## <span data-ttu-id="497fe-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="497fe-130">NOTES</span></span>

## <span data-ttu-id="497fe-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="497fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="497fe-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="497fe-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="497fe-133">Regisztráció törlése – AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="497fe-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


