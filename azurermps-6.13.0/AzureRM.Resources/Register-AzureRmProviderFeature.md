---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: 6be1d4f755d11c6c0cbd32488b59f4e141278633
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493950"
---
# <span data-ttu-id="c7913-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c7913-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="c7913-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7913-102">SYNOPSIS</span></span>
<span data-ttu-id="c7913-103">A fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c7913-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7913-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7913-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7913-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7913-105">DESCRIPTION</span></span>
<span data-ttu-id="c7913-106">A **Register-AzureRmProviderFeature** parancsmag a fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c7913-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="c7913-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7913-107">EXAMPLES</span></span>

### <span data-ttu-id="c7913-108">1. példa: funkció regisztrálása</span><span class="sxs-lookup"><span data-stu-id="c7913-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="c7913-109">Ezzel felveszi a Microsoft. Network AllowApplicationSecurityGroups funkcióját a fiókjába.</span><span class="sxs-lookup"><span data-stu-id="c7913-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="c7913-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7913-110">PARAMETERS</span></span>

### <span data-ttu-id="c7913-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7913-111">-DefaultProfile</span></span>
<span data-ttu-id="c7913-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7913-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7913-113">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="c7913-113">-FeatureName</span></span>
<span data-ttu-id="c7913-114">Annak a funkciónak a neve, amely a parancsmagot regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c7913-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="c7913-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c7913-115">-ProviderNamespace</span></span>
<span data-ttu-id="c7913-116">Azt a névteret adja meg, amelyre ez a parancsmag a szolgáltató szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c7913-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="c7913-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7913-117">-Confirm</span></span>
<span data-ttu-id="c7913-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7913-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7913-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7913-119">-WhatIf</span></span>
<span data-ttu-id="c7913-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7913-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7913-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7913-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7913-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7913-122">CommonParameters</span></span>
<span data-ttu-id="c7913-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7913-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7913-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7913-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7913-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7913-125">INPUTS</span></span>

## <span data-ttu-id="c7913-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7913-126">OUTPUTS</span></span>

## <span data-ttu-id="c7913-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7913-127">NOTES</span></span>

## <span data-ttu-id="c7913-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7913-128">RELATED LINKS</span></span>

[<span data-ttu-id="c7913-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c7913-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


