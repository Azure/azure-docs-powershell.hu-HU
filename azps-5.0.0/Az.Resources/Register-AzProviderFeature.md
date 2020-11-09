---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303347"
---
# <span data-ttu-id="7030b-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7030b-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="7030b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7030b-102">SYNOPSIS</span></span>
<span data-ttu-id="7030b-103">A fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="7030b-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="7030b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7030b-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7030b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7030b-105">DESCRIPTION</span></span>
<span data-ttu-id="7030b-106">A **Register-AzProviderFeature** parancsmag a fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="7030b-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="7030b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7030b-107">EXAMPLES</span></span>

### <span data-ttu-id="7030b-108">1. példa: funkció regisztrálása</span><span class="sxs-lookup"><span data-stu-id="7030b-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="7030b-109">Ezzel felveszi a Microsoft. Network AllowApplicationSecurityGroups funkcióját a fiókjába.</span><span class="sxs-lookup"><span data-stu-id="7030b-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="7030b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7030b-110">PARAMETERS</span></span>

### <span data-ttu-id="7030b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7030b-111">-DefaultProfile</span></span>
<span data-ttu-id="7030b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7030b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7030b-113">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="7030b-113">-FeatureName</span></span>
<span data-ttu-id="7030b-114">Annak a funkciónak a neve, amely a parancsmagot regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="7030b-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="7030b-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7030b-115">-ProviderNamespace</span></span>
<span data-ttu-id="7030b-116">Azt a névteret adja meg, amelyre ez a parancsmag a szolgáltató szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="7030b-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="7030b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7030b-117">-Confirm</span></span>
<span data-ttu-id="7030b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7030b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7030b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7030b-119">-WhatIf</span></span>
<span data-ttu-id="7030b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7030b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7030b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7030b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7030b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7030b-122">CommonParameters</span></span>
<span data-ttu-id="7030b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7030b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7030b-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7030b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7030b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7030b-125">INPUTS</span></span>

### <span data-ttu-id="7030b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7030b-126">System.String</span></span>

## <span data-ttu-id="7030b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7030b-127">OUTPUTS</span></span>

### <span data-ttu-id="7030b-128">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7030b-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="7030b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7030b-129">NOTES</span></span>

## <span data-ttu-id="7030b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7030b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7030b-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7030b-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


