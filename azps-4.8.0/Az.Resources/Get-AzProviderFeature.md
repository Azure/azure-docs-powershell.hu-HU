---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182686"
---
# <span data-ttu-id="be8bf-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="be8bf-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="be8bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="be8bf-103">Információkat kap az Azure Provider funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="be8bf-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="be8bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be8bf-104">SYNTAX</span></span>

### <span data-ttu-id="be8bf-105">ListAvailableParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be8bf-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be8bf-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="be8bf-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be8bf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="be8bf-107">DESCRIPTION</span></span>
<span data-ttu-id="be8bf-108">A **Get-AzProviderFeature** parancsmag a szolgáltatás nevét, a szolgáltató nevét és a regisztráció állapotát az Azure szolgáltató szolgáltatásaihoz kapja.</span><span class="sxs-lookup"><span data-stu-id="be8bf-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="be8bf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="be8bf-109">EXAMPLES</span></span>

### <span data-ttu-id="be8bf-110">Példa 1: az összes elérhető funkció beszerzése</span><span class="sxs-lookup"><span data-stu-id="be8bf-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="be8bf-111">Ez a parancs elérhetővé válik az összes elérhető funkció.</span><span class="sxs-lookup"><span data-stu-id="be8bf-111">This command gets all available features.</span></span>

### <span data-ttu-id="be8bf-112">2. példa: információk kérése egy adott funkcióról</span><span class="sxs-lookup"><span data-stu-id="be8bf-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="be8bf-113">Ez a parancs információkat kap a megadott szolgáltató AllowPreReleaseRegions nevű funkcióról.</span><span class="sxs-lookup"><span data-stu-id="be8bf-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="be8bf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be8bf-114">PARAMETERS</span></span>

### <span data-ttu-id="be8bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8bf-115">-DefaultProfile</span></span>
<span data-ttu-id="be8bf-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="be8bf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be8bf-117">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="be8bf-117">-FeatureName</span></span>
<span data-ttu-id="be8bf-118">A beolvasott funkció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be8bf-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="be8bf-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="be8bf-119">-ListAvailable</span></span>
<span data-ttu-id="be8bf-120">Azt jelzi, hogy ez a parancsmag minden szolgáltatást elérhető.</span><span class="sxs-lookup"><span data-stu-id="be8bf-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="be8bf-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="be8bf-121">-ProviderNamespace</span></span>
<span data-ttu-id="be8bf-122">Azt a névteret adja meg, amelynek a parancsmagja a szolgáltató funkcióit kapja.</span><span class="sxs-lookup"><span data-stu-id="be8bf-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="be8bf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8bf-123">CommonParameters</span></span>
<span data-ttu-id="be8bf-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be8bf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8bf-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="be8bf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8bf-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be8bf-126">INPUTS</span></span>

### <span data-ttu-id="be8bf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="be8bf-127">System.String</span></span>

## <span data-ttu-id="be8bf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be8bf-128">OUTPUTS</span></span>

### <span data-ttu-id="be8bf-129">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="be8bf-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="be8bf-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be8bf-130">NOTES</span></span>

## <span data-ttu-id="be8bf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be8bf-131">RELATED LINKS</span></span>

[<span data-ttu-id="be8bf-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="be8bf-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


