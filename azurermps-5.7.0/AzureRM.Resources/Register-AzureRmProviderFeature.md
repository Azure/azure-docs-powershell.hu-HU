---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494359"
---
# <span data-ttu-id="0c4be-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="0c4be-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="0c4be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c4be-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4be-103">A fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="0c4be-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c4be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c4be-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c4be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c4be-105">DESCRIPTION</span></span>
<span data-ttu-id="0c4be-106">A **Register-AzureRmProviderFeature** parancsmag a fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="0c4be-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="0c4be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c4be-107">EXAMPLES</span></span>

### <span data-ttu-id="0c4be-108">1. példa: funkció regisztrálása</span><span class="sxs-lookup"><span data-stu-id="0c4be-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="0c4be-109">Ezzel felveszi a Microsoft. Network AllowApplicationSecurityGroups funkcióját a fiókjába.</span><span class="sxs-lookup"><span data-stu-id="0c4be-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="0c4be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c4be-110">PARAMETERS</span></span>

### <span data-ttu-id="0c4be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4be-111">-DefaultProfile</span></span>
<span data-ttu-id="0c4be-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0c4be-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c4be-113">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="0c4be-113">-FeatureName</span></span>
<span data-ttu-id="0c4be-114">Annak a funkciónak a neve, amely a parancsmagot regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="0c4be-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="0c4be-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0c4be-115">-ProviderNamespace</span></span>
<span data-ttu-id="0c4be-116">Azt a névteret adja meg, amelyre ez a parancsmag a szolgáltató szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="0c4be-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="0c4be-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c4be-117">-Confirm</span></span>
<span data-ttu-id="0c4be-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c4be-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c4be-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c4be-119">-WhatIf</span></span>
<span data-ttu-id="0c4be-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c4be-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c4be-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c4be-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c4be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4be-122">CommonParameters</span></span>
<span data-ttu-id="0c4be-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c4be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4be-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c4be-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4be-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c4be-125">INPUTS</span></span>

### <span data-ttu-id="0c4be-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="0c4be-126">None</span></span>
<span data-ttu-id="0c4be-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0c4be-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c4be-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c4be-128">OUTPUTS</span></span>

### <span data-ttu-id="0c4be-129">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="0c4be-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="0c4be-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c4be-130">NOTES</span></span>

## <span data-ttu-id="0c4be-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c4be-131">RELATED LINKS</span></span>

[<span data-ttu-id="0c4be-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="0c4be-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


