---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 182accdabc368e72451a0c1d9a1d78f1cf561730
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849510"
---
# <span data-ttu-id="dd73c-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="dd73c-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="dd73c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd73c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd73c-103">Információkat kap az Azure Provider funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="dd73c-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd73c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd73c-104">SYNTAX</span></span>

### <span data-ttu-id="dd73c-105">ListAvailableParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd73c-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd73c-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="dd73c-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd73c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd73c-107">DESCRIPTION</span></span>
<span data-ttu-id="dd73c-108">A **Get-AzureRmProviderFeature** parancsmag a szolgáltatás nevét, a szolgáltató nevét és a regisztráció állapotát az Azure szolgáltató szolgáltatásaihoz kapja.</span><span class="sxs-lookup"><span data-stu-id="dd73c-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="dd73c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd73c-109">EXAMPLES</span></span>

### <span data-ttu-id="dd73c-110">Példa 1: az összes elérhető funkció beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd73c-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="dd73c-111">Ez a parancs elérhetővé válik az összes elérhető funkció.</span><span class="sxs-lookup"><span data-stu-id="dd73c-111">This command gets all available features.</span></span>

### <span data-ttu-id="dd73c-112">2. példa: információk kérése egy adott funkcióról</span><span class="sxs-lookup"><span data-stu-id="dd73c-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="dd73c-113">Ez a parancs információkat kap a megadott szolgáltató AllowPreReleaseRegions nevű funkcióról.</span><span class="sxs-lookup"><span data-stu-id="dd73c-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="dd73c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd73c-114">PARAMETERS</span></span>

### <span data-ttu-id="dd73c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd73c-115">-DefaultProfile</span></span>
<span data-ttu-id="dd73c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dd73c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd73c-117">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="dd73c-117">-FeatureName</span></span>
<span data-ttu-id="dd73c-118">A beolvasott funkció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd73c-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="dd73c-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="dd73c-119">-ListAvailable</span></span>
<span data-ttu-id="dd73c-120">Azt jelzi, hogy ez a parancsmag minden szolgáltatást elérhető.</span><span class="sxs-lookup"><span data-stu-id="dd73c-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="dd73c-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="dd73c-121">-ProviderNamespace</span></span>
<span data-ttu-id="dd73c-122">Azt a névteret adja meg, amelynek a parancsmagja a szolgáltató funkcióit kapja.</span><span class="sxs-lookup"><span data-stu-id="dd73c-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="dd73c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd73c-123">CommonParameters</span></span>
<span data-ttu-id="dd73c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd73c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd73c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd73c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd73c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd73c-126">INPUTS</span></span>

## <span data-ttu-id="dd73c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd73c-127">OUTPUTS</span></span>

## <span data-ttu-id="dd73c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd73c-128">NOTES</span></span>

## <span data-ttu-id="dd73c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd73c-129">RELATED LINKS</span></span>

[<span data-ttu-id="dd73c-130">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="dd73c-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


