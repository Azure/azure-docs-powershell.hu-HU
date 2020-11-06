---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500732"
---
# <span data-ttu-id="d0501-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d0501-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="d0501-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0501-102">SYNOPSIS</span></span>
<span data-ttu-id="d0501-103">A fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="d0501-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0501-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0501-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0501-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0501-105">DESCRIPTION</span></span>
<span data-ttu-id="d0501-106">A **Register-AzureRmProviderFeature** parancsmag a fiók Azure Provider szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="d0501-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d0501-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0501-107">EXAMPLES</span></span>

## <span data-ttu-id="d0501-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0501-108">PARAMETERS</span></span>

### <span data-ttu-id="d0501-109">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="d0501-109">-FeatureName</span></span>
<span data-ttu-id="d0501-110">Annak a funkciónak a neve, amely a parancsmagot regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="d0501-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="d0501-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d0501-111">-ProviderNamespace</span></span>
<span data-ttu-id="d0501-112">Azt a névteret adja meg, amelyre ez a parancsmag a szolgáltató szolgáltatását regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="d0501-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="d0501-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0501-113">-Confirm</span></span>
<span data-ttu-id="d0501-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0501-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0501-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0501-115">-WhatIf</span></span>
<span data-ttu-id="d0501-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0501-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0501-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0501-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0501-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0501-118">-DefaultProfile</span></span>
<span data-ttu-id="d0501-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0501-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0501-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0501-120">CommonParameters</span></span>
<span data-ttu-id="d0501-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0501-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0501-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0501-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0501-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0501-123">INPUTS</span></span>

## <span data-ttu-id="d0501-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0501-124">OUTPUTS</span></span>

### <span data-ttu-id="d0501-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="d0501-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="d0501-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0501-126">NOTES</span></span>

## <span data-ttu-id="d0501-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0501-127">RELATED LINKS</span></span>

[<span data-ttu-id="d0501-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d0501-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


