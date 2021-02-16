---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153714"
---
# <span data-ttu-id="c9e70-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c9e70-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="c9e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e70-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e70-103">Információkat kap az Azure-szolgáltató funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="c9e70-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="c9e70-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9e70-104">SYNTAX</span></span>

### <span data-ttu-id="c9e70-105">ListAvailableParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9e70-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9e70-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="c9e70-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e70-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9e70-107">DESCRIPTION</span></span>
<span data-ttu-id="c9e70-108">A **Get-AzProviderFeature parancsmag** megkapja az Azure-szolgáltató szolgáltatásainak szolgáltatásnevét, szolgáltatónevét és regisztrációs állapotát.</span><span class="sxs-lookup"><span data-stu-id="c9e70-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="c9e70-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9e70-109">EXAMPLES</span></span>

### <span data-ttu-id="c9e70-110">1. példa: Az összes elérhető szolgáltatás igénybevéve</span><span class="sxs-lookup"><span data-stu-id="c9e70-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="c9e70-111">Ez a parancs az összes elérhető funkciót elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="c9e70-111">This command gets all available features.</span></span>

### <span data-ttu-id="c9e70-112">2. példa: Információ lekérte egy adott funkcióról</span><span class="sxs-lookup"><span data-stu-id="c9e70-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="c9e70-113">Ez a parancs információt kap a megadott szolgáltató AllowPreReleaseRegions nevű szolgáltatásával kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="c9e70-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="c9e70-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9e70-114">PARAMETERS</span></span>

### <span data-ttu-id="c9e70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e70-115">-DefaultProfile</span></span>
<span data-ttu-id="c9e70-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c9e70-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9e70-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="c9e70-117">-FeatureName</span></span>
<span data-ttu-id="c9e70-118">A lekért szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="c9e70-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="c9e70-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="c9e70-119">-ListAvailable</span></span>
<span data-ttu-id="c9e70-120">Azt jelzi, hogy ez a parancsmag az összes funkciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="c9e70-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="c9e70-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c9e70-121">-ProviderNamespace</span></span>
<span data-ttu-id="c9e70-122">Azt a névteret adja meg, amelyhez a parancsmag szolgáltatói szolgáltatásokat kap.</span><span class="sxs-lookup"><span data-stu-id="c9e70-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="c9e70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e70-123">CommonParameters</span></span>
<span data-ttu-id="c9e70-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e70-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9e70-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e70-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9e70-126">INPUTS</span></span>

### <span data-ttu-id="c9e70-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c9e70-127">System.String</span></span>

## <span data-ttu-id="c9e70-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9e70-128">OUTPUTS</span></span>

### <span data-ttu-id="c9e70-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c9e70-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="c9e70-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9e70-130">NOTES</span></span>

## <span data-ttu-id="c9e70-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9e70-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9e70-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c9e70-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


