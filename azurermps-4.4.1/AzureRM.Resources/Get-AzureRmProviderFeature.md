---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500775"
---
# <span data-ttu-id="5a50d-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5a50d-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="5a50d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a50d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a50d-103">Információkat kap az Azure Provider funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="5a50d-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a50d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a50d-104">SYNTAX</span></span>

### <span data-ttu-id="5a50d-105">ListAvailableParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a50d-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a50d-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="5a50d-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a50d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a50d-107">DESCRIPTION</span></span>
<span data-ttu-id="5a50d-108">A **Get-AzureRmProviderFeature** parancsmag a szolgáltatás nevét, a szolgáltató nevét és a regisztráció állapotát az Azure szolgáltató szolgáltatásaihoz kapja.</span><span class="sxs-lookup"><span data-stu-id="5a50d-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="5a50d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5a50d-109">EXAMPLES</span></span>

### <span data-ttu-id="5a50d-110">Példa 1: az összes elérhető funkció beszerzése</span><span class="sxs-lookup"><span data-stu-id="5a50d-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="5a50d-111">Ez a parancs elérhetővé válik az összes elérhető funkció.</span><span class="sxs-lookup"><span data-stu-id="5a50d-111">This command gets all available features.</span></span>

### <span data-ttu-id="5a50d-112">2. példa: információk kérése egy adott funkcióról</span><span class="sxs-lookup"><span data-stu-id="5a50d-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="5a50d-113">Ez a parancs információkat kap a megadott szolgáltató AllowPreReleaseRegions nevű funkcióról.</span><span class="sxs-lookup"><span data-stu-id="5a50d-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="5a50d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a50d-114">PARAMETERS</span></span>

### <span data-ttu-id="5a50d-115">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="5a50d-115">-FeatureName</span></span>
<span data-ttu-id="5a50d-116">A beolvasott funkció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a50d-116">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a50d-117">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="5a50d-117">-ListAvailable</span></span>
<span data-ttu-id="5a50d-118">Azt jelzi, hogy ez a parancsmag minden szolgáltatást elérhető.</span><span class="sxs-lookup"><span data-stu-id="5a50d-118">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a50d-119">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5a50d-119">-ProviderNamespace</span></span>
<span data-ttu-id="5a50d-120">Azt a névteret adja meg, amelynek a parancsmagja a szolgáltató funkcióit kapja.</span><span class="sxs-lookup"><span data-stu-id="5a50d-120">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a50d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a50d-121">-DefaultProfile</span></span>
<span data-ttu-id="5a50d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a50d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a50d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a50d-123">CommonParameters</span></span>
<span data-ttu-id="5a50d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a50d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a50d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a50d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a50d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a50d-126">INPUTS</span></span>

## <span data-ttu-id="5a50d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a50d-127">OUTPUTS</span></span>

### <span data-ttu-id="5a50d-128">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="5a50d-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="5a50d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a50d-129">NOTES</span></span>

## <span data-ttu-id="5a50d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a50d-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a50d-131">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5a50d-131">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


