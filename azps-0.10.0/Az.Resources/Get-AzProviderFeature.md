---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 1296e1e135acce9d4840e625d96931f6ecc11625
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843433"
---
# <span data-ttu-id="f7628-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f7628-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="f7628-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7628-102">SYNOPSIS</span></span>
<span data-ttu-id="f7628-103">Információkat kap az Azure Provider funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="f7628-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="f7628-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7628-104">SYNTAX</span></span>

### <span data-ttu-id="f7628-105">ListAvailableParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7628-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7628-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="f7628-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7628-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7628-107">DESCRIPTION</span></span>
<span data-ttu-id="f7628-108">A **Get-AzProviderFeature** parancsmag a szolgáltatás nevét, a szolgáltató nevét és a regisztráció állapotát az Azure szolgáltató szolgáltatásaihoz kapja.</span><span class="sxs-lookup"><span data-stu-id="f7628-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="f7628-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f7628-109">EXAMPLES</span></span>

### <span data-ttu-id="f7628-110">Példa 1: az összes elérhető funkció beszerzése</span><span class="sxs-lookup"><span data-stu-id="f7628-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="f7628-111">Ez a parancs elérhetővé válik az összes elérhető funkció.</span><span class="sxs-lookup"><span data-stu-id="f7628-111">This command gets all available features.</span></span>

### <span data-ttu-id="f7628-112">2. példa: információk kérése egy adott funkcióról</span><span class="sxs-lookup"><span data-stu-id="f7628-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="f7628-113">Ez a parancs információkat kap a megadott szolgáltató AllowPreReleaseRegions nevű funkcióról.</span><span class="sxs-lookup"><span data-stu-id="f7628-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="f7628-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7628-114">PARAMETERS</span></span>

### <span data-ttu-id="f7628-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7628-115">-DefaultProfile</span></span>
<span data-ttu-id="f7628-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7628-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7628-117">-ÖsszetevőNeve</span><span class="sxs-lookup"><span data-stu-id="f7628-117">-FeatureName</span></span>
<span data-ttu-id="f7628-118">A beolvasott funkció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7628-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="f7628-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f7628-119">-ListAvailable</span></span>
<span data-ttu-id="f7628-120">Azt jelzi, hogy ez a parancsmag minden szolgáltatást elérhető.</span><span class="sxs-lookup"><span data-stu-id="f7628-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="f7628-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f7628-121">-ProviderNamespace</span></span>
<span data-ttu-id="f7628-122">Azt a névteret adja meg, amelynek a parancsmagja a szolgáltató funkcióit kapja.</span><span class="sxs-lookup"><span data-stu-id="f7628-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="f7628-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7628-123">CommonParameters</span></span>
<span data-ttu-id="f7628-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7628-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7628-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7628-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7628-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7628-126">INPUTS</span></span>

## <span data-ttu-id="f7628-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7628-127">OUTPUTS</span></span>

## <span data-ttu-id="f7628-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7628-128">NOTES</span></span>

## <span data-ttu-id="f7628-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7628-129">RELATED LINKS</span></span>

[<span data-ttu-id="f7628-130">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f7628-130">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


