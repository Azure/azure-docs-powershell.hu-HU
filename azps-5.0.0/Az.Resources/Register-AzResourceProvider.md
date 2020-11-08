---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186557"
---
# <span data-ttu-id="e595d-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e595d-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="e595d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e595d-102">SYNOPSIS</span></span>
<span data-ttu-id="e595d-103">Erőforrás-szolgáltató regisztrálása.</span><span class="sxs-lookup"><span data-stu-id="e595d-103">Registers a resource provider.</span></span>

## <span data-ttu-id="e595d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e595d-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e595d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e595d-105">DESCRIPTION</span></span>
<span data-ttu-id="e595d-106">A **Register-AzResourceProvider** parancsmag az Azure Resource providert regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="e595d-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="e595d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e595d-107">EXAMPLES</span></span>

### <span data-ttu-id="e595d-108">1. példa: szolgáltató regisztrálása</span><span class="sxs-lookup"><span data-stu-id="e595d-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e595d-109">Ezzel a szolgáltatással regisztrálhatja a Microsoft. Network szolgáltatót a fiókjához.</span><span class="sxs-lookup"><span data-stu-id="e595d-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="e595d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e595d-110">PARAMETERS</span></span>

### <span data-ttu-id="e595d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e595d-111">-ApiVersion</span></span>
<span data-ttu-id="e595d-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e595d-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e595d-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="e595d-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e595d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e595d-114">-DefaultProfile</span></span>
<span data-ttu-id="e595d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e595d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e595d-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="e595d-116">-Pre</span></span>
<span data-ttu-id="e595d-117">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e595d-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e595d-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e595d-118">-ProviderNamespace</span></span>
<span data-ttu-id="e595d-119">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e595d-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e595d-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e595d-120">-Confirm</span></span>
<span data-ttu-id="e595d-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e595d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e595d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e595d-122">-WhatIf</span></span>
<span data-ttu-id="e595d-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e595d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e595d-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e595d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e595d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e595d-125">CommonParameters</span></span>
<span data-ttu-id="e595d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e595d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e595d-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e595d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e595d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e595d-128">INPUTS</span></span>

### <span data-ttu-id="e595d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e595d-129">System.String</span></span>

## <span data-ttu-id="e595d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e595d-130">OUTPUTS</span></span>

### <span data-ttu-id="e595d-131">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e595d-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="e595d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e595d-132">NOTES</span></span>

## <span data-ttu-id="e595d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e595d-133">RELATED LINKS</span></span>

[<span data-ttu-id="e595d-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e595d-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e595d-135">Regisztráció törlése – AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e595d-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)

