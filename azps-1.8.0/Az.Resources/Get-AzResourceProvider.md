---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669413"
---
# <span data-ttu-id="11110-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="11110-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="11110-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11110-102">SYNOPSIS</span></span>
<span data-ttu-id="11110-103">Erőforrás-szolgáltatót kap.</span><span class="sxs-lookup"><span data-stu-id="11110-103">Gets a resource provider.</span></span>

## <span data-ttu-id="11110-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11110-104">SYNTAX</span></span>

### <span data-ttu-id="11110-105">ListAvailable (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11110-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11110-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="11110-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11110-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="11110-107">DESCRIPTION</span></span>
<span data-ttu-id="11110-108">A **Get-AzResourceProvider** parancsmag Azure-erőforrás-szolgáltatót kap.</span><span class="sxs-lookup"><span data-stu-id="11110-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="11110-109">Példák</span><span class="sxs-lookup"><span data-stu-id="11110-109">EXAMPLES</span></span>

## <span data-ttu-id="11110-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11110-110">PARAMETERS</span></span>

### <span data-ttu-id="11110-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="11110-111">-ApiVersion</span></span>
<span data-ttu-id="11110-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="11110-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="11110-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="11110-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="11110-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11110-114">-DefaultProfile</span></span>
<span data-ttu-id="11110-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11110-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11110-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="11110-116">-ListAvailable</span></span>
<span data-ttu-id="11110-117">Jelzi, hogy ez a művelet az összes elérhető erőforrás-szolgáltatót bekapja.</span><span class="sxs-lookup"><span data-stu-id="11110-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11110-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="11110-118">-Location</span></span>
<span data-ttu-id="11110-119">Az erőforrás-szolgáltató helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11110-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="11110-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="11110-120">-Pre</span></span>
<span data-ttu-id="11110-121">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="11110-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="11110-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="11110-122">-ProviderNamespace</span></span>
<span data-ttu-id="11110-123">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11110-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11110-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11110-124">CommonParameters</span></span>
<span data-ttu-id="11110-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11110-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11110-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11110-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11110-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11110-127">INPUTS</span></span>

### <span data-ttu-id="11110-128">System. string []</span><span class="sxs-lookup"><span data-stu-id="11110-128">System.String[]</span></span>

## <span data-ttu-id="11110-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11110-129">OUTPUTS</span></span>

### <span data-ttu-id="11110-130">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="11110-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="11110-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11110-131">NOTES</span></span>

## <span data-ttu-id="11110-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11110-132">RELATED LINKS</span></span>

[<span data-ttu-id="11110-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="11110-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="11110-134">Regisztráció törlése – AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="11110-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


