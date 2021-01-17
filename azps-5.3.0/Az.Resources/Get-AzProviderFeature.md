---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466513"
---
# <span data-ttu-id="5b2be-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5b2be-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="5b2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b2be-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2be-103">Információkat kap az Azure-szolgáltató funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="5b2be-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="5b2be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b2be-104">SYNTAX</span></span>

### <span data-ttu-id="5b2be-105">ListAvailableParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b2be-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b2be-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="5b2be-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b2be-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b2be-107">DESCRIPTION</span></span>
<span data-ttu-id="5b2be-108">A **Get-AzProviderFeature parancsmag** megkapja az Azure-szolgáltató szolgáltatásainak szolgáltatásnevét, szolgáltatónevét és regisztrációs állapotát.</span><span class="sxs-lookup"><span data-stu-id="5b2be-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="5b2be-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b2be-109">EXAMPLES</span></span>

### <span data-ttu-id="5b2be-110">1. példa: Az összes elérhető szolgáltatás igénybevéve</span><span class="sxs-lookup"><span data-stu-id="5b2be-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="5b2be-111">Ez a parancs az összes elérhető funkciót elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="5b2be-111">This command gets all available features.</span></span>

### <span data-ttu-id="5b2be-112">2. példa: Információ lekérte egy adott funkcióról</span><span class="sxs-lookup"><span data-stu-id="5b2be-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="5b2be-113">Ez a parancs információt kap a megadott szolgáltató AllowPreReleaseRegions nevű szolgáltatásával kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="5b2be-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="5b2be-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b2be-114">PARAMETERS</span></span>

### <span data-ttu-id="5b2be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2be-115">-DefaultProfile</span></span>
<span data-ttu-id="5b2be-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5b2be-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b2be-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="5b2be-117">-FeatureName</span></span>
<span data-ttu-id="5b2be-118">A lekért szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="5b2be-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="5b2be-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="5b2be-119">-ListAvailable</span></span>
<span data-ttu-id="5b2be-120">Azt jelzi, hogy ez a parancsmag az összes funkciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="5b2be-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="5b2be-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5b2be-121">-ProviderNamespace</span></span>
<span data-ttu-id="5b2be-122">Azt a névteret adja meg, amelyhez a parancsmag szolgáltatói funkciókat kap.</span><span class="sxs-lookup"><span data-stu-id="5b2be-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="5b2be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2be-123">CommonParameters</span></span>
<span data-ttu-id="5b2be-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b2be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2be-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b2be-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2be-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b2be-126">INPUTS</span></span>

### <span data-ttu-id="5b2be-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5b2be-127">System.String</span></span>

## <span data-ttu-id="5b2be-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b2be-128">OUTPUTS</span></span>

### <span data-ttu-id="5b2be-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5b2be-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="5b2be-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b2be-130">NOTES</span></span>

## <span data-ttu-id="5b2be-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b2be-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b2be-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="5b2be-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


