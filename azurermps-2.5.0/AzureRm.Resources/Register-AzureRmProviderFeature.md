---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850242"
---
# <span data-ttu-id="c6313-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c6313-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="c6313-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6313-102">SYNOPSIS</span></span>
<span data-ttu-id="c6313-103">A fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c6313-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6313-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6313-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6313-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6313-105">DESCRIPTION</span></span>
<span data-ttu-id="c6313-106">A **Register-AzureRmProviderFeature** parancsmag a fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c6313-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="c6313-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6313-107">EXAMPLES</span></span>

### <span data-ttu-id="c6313-108">1. példa: funkció regisztrálása</span><span class="sxs-lookup"><span data-stu-id="c6313-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="c6313-109">Ezzel felveszi a Microsoft. Network AllowApplicationSecurityGroups funkcióját a fiókjába.</span><span class="sxs-lookup"><span data-stu-id="c6313-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="c6313-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6313-110">PARAMETERS</span></span>

### <span data-ttu-id="c6313-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6313-111">-DefaultProfile</span></span>
<span data-ttu-id="c6313-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c6313-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6313-113">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="c6313-113">-FeatureName</span></span>
<span data-ttu-id="c6313-114">Annak a funkciónak a neve, amely a parancsmagot regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c6313-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="c6313-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c6313-115">-ProviderNamespace</span></span>
<span data-ttu-id="c6313-116">Azt a névteret adja meg, amelyre ez a parancsmag a szolgáltató szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="c6313-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="c6313-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6313-117">-Confirm</span></span>
<span data-ttu-id="c6313-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6313-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6313-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6313-119">-WhatIf</span></span>
<span data-ttu-id="c6313-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6313-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6313-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6313-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6313-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6313-122">CommonParameters</span></span>
<span data-ttu-id="c6313-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6313-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6313-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6313-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6313-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6313-125">INPUTS</span></span>

## <span data-ttu-id="c6313-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6313-126">OUTPUTS</span></span>

## <span data-ttu-id="c6313-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6313-127">NOTES</span></span>

## <span data-ttu-id="c6313-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6313-128">RELATED LINKS</span></span>

[<span data-ttu-id="c6313-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c6313-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


