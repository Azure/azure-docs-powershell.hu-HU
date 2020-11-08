---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 6cb27f66871038fa1849671391e1d7d9f8f3ccd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180915"
---
# <span data-ttu-id="31731-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="31731-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="31731-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31731-102">SYNOPSIS</span></span>
<span data-ttu-id="31731-103">Az Azure szolgáltató funkció regisztrációjának megszüntetése a fiókban.</span><span class="sxs-lookup"><span data-stu-id="31731-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="31731-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31731-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31731-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31731-105">DESCRIPTION</span></span>
<span data-ttu-id="31731-106">A **unregister-AzProviderFeature** parancsmag a fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="31731-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="31731-107">Példák</span><span class="sxs-lookup"><span data-stu-id="31731-107">EXAMPLES</span></span>

### <span data-ttu-id="31731-108">1. példa: funkció regisztrációjának megszüntetése</span><span class="sxs-lookup"><span data-stu-id="31731-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="31731-109">Ezzel a beállítással a Microsoft. Network AllowApplicationSecurityGroups funkciója regisztrálható a fiókjából.</span><span class="sxs-lookup"><span data-stu-id="31731-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="31731-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31731-110">PARAMETERS</span></span>

### <span data-ttu-id="31731-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31731-111">-DefaultProfile</span></span>
<span data-ttu-id="31731-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31731-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31731-113">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="31731-113">-FeatureName</span></span>
<span data-ttu-id="31731-114">A funkció neve.</span><span class="sxs-lookup"><span data-stu-id="31731-114">The feature name.</span></span>

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

### <span data-ttu-id="31731-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="31731-115">-ProviderNamespace</span></span>
<span data-ttu-id="31731-116">Az erőforrás-szolgáltató névtér.</span><span class="sxs-lookup"><span data-stu-id="31731-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="31731-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31731-117">-Confirm</span></span>
<span data-ttu-id="31731-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31731-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31731-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31731-119">-WhatIf</span></span>
<span data-ttu-id="31731-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31731-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31731-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31731-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31731-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31731-122">CommonParameters</span></span>
<span data-ttu-id="31731-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31731-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31731-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31731-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31731-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31731-125">INPUTS</span></span>

### <span data-ttu-id="31731-126">System. String</span><span class="sxs-lookup"><span data-stu-id="31731-126">System.String</span></span>

## <span data-ttu-id="31731-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31731-127">OUTPUTS</span></span>

### <span data-ttu-id="31731-128">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="31731-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="31731-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31731-129">NOTES</span></span>

## <span data-ttu-id="31731-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31731-130">RELATED LINKS</span></span>
