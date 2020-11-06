---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500748"
---
# <span data-ttu-id="e9b56-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9b56-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="e9b56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9b56-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b56-103">Erőforrás-szolgáltatót kap.</span><span class="sxs-lookup"><span data-stu-id="e9b56-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9b56-104">SYNTAX</span></span>

### <span data-ttu-id="e9b56-105">ListAvailable (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9b56-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9b56-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="e9b56-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9b56-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9b56-107">DESCRIPTION</span></span>
<span data-ttu-id="e9b56-108">A **Get-AzureRmResourceProvider** parancsmag Azure-erőforrás-szolgáltatót kap.</span><span class="sxs-lookup"><span data-stu-id="e9b56-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="e9b56-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e9b56-109">EXAMPLES</span></span>

## <span data-ttu-id="e9b56-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9b56-110">PARAMETERS</span></span>

### <span data-ttu-id="e9b56-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e9b56-111">-ApiVersion</span></span>
<span data-ttu-id="e9b56-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b56-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e9b56-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="e9b56-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e9b56-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e9b56-114">-ListAvailable</span></span>
<span data-ttu-id="e9b56-115">Jelzi, hogy ez a művelet az összes elérhető erőforrás-szolgáltatót bekapja.</span><span class="sxs-lookup"><span data-stu-id="e9b56-115">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="e9b56-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="e9b56-116">-Location</span></span>
<span data-ttu-id="e9b56-117">Az erőforrás-szolgáltató helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b56-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="e9b56-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="e9b56-118">-Pre</span></span>
<span data-ttu-id="e9b56-119">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e9b56-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e9b56-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e9b56-120">-ProviderNamespace</span></span>
<span data-ttu-id="e9b56-121">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b56-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b56-122">-DefaultProfile</span></span>
<span data-ttu-id="e9b56-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9b56-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b56-124">CommonParameters</span></span>
<span data-ttu-id="e9b56-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9b56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b56-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b56-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b56-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b56-127">INPUTS</span></span>

## <span data-ttu-id="e9b56-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b56-128">OUTPUTS</span></span>

### <span data-ttu-id="e9b56-129">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9b56-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="e9b56-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9b56-130">NOTES</span></span>

## <span data-ttu-id="e9b56-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9b56-131">RELATED LINKS</span></span>

[<span data-ttu-id="e9b56-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9b56-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="e9b56-133">Regisztráció törlése – AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9b56-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


