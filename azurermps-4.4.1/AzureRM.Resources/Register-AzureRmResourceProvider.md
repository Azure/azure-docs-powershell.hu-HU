---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500723"
---
# <span data-ttu-id="f8643-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f8643-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="f8643-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8643-102">SYNOPSIS</span></span>
<span data-ttu-id="f8643-103">Erőforrás-szolgáltató regisztrálása.</span><span class="sxs-lookup"><span data-stu-id="f8643-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8643-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8643-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8643-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8643-105">DESCRIPTION</span></span>
<span data-ttu-id="f8643-106">A **Register-AzureRmResourceProvider** parancsmag az Azure Resource providert regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="f8643-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="f8643-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8643-107">EXAMPLES</span></span>

## <span data-ttu-id="f8643-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8643-108">PARAMETERS</span></span>

### <span data-ttu-id="f8643-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f8643-109">-ApiVersion</span></span>
<span data-ttu-id="f8643-110">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8643-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f8643-111">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="f8643-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f8643-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="f8643-112">-Pre</span></span>
<span data-ttu-id="f8643-113">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f8643-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f8643-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f8643-114">-ProviderNamespace</span></span>
<span data-ttu-id="f8643-115">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8643-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="f8643-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f8643-116">-Confirm</span></span>
<span data-ttu-id="f8643-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f8643-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8643-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8643-118">-WhatIf</span></span>
<span data-ttu-id="f8643-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f8643-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8643-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8643-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8643-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8643-121">-DefaultProfile</span></span>
<span data-ttu-id="f8643-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8643-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8643-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8643-123">CommonParameters</span></span>
<span data-ttu-id="f8643-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8643-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8643-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8643-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8643-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8643-126">INPUTS</span></span>

## <span data-ttu-id="f8643-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8643-127">OUTPUTS</span></span>

### <span data-ttu-id="f8643-128">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f8643-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="f8643-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8643-129">NOTES</span></span>

## <span data-ttu-id="f8643-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8643-130">RELATED LINKS</span></span>

[<span data-ttu-id="f8643-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f8643-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="f8643-132">Regisztráció törlése – AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f8643-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


