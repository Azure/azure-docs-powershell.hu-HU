---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848378"
---
# <span data-ttu-id="80371-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="80371-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="80371-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80371-102">SYNOPSIS</span></span>
<span data-ttu-id="80371-103">Erőforrás-szolgáltatót kap.</span><span class="sxs-lookup"><span data-stu-id="80371-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80371-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80371-104">SYNTAX</span></span>

### <span data-ttu-id="80371-105">ListAvailable (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80371-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80371-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="80371-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80371-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="80371-107">DESCRIPTION</span></span>
<span data-ttu-id="80371-108">A **Get-AzureRmResourceProvider** parancsmag Azure-erőforrás-szolgáltatót kap.</span><span class="sxs-lookup"><span data-stu-id="80371-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="80371-109">Példák</span><span class="sxs-lookup"><span data-stu-id="80371-109">EXAMPLES</span></span>

## <span data-ttu-id="80371-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80371-110">PARAMETERS</span></span>

### <span data-ttu-id="80371-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="80371-111">-ApiVersion</span></span>
<span data-ttu-id="80371-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="80371-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="80371-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="80371-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="80371-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80371-114">-DefaultProfile</span></span>
<span data-ttu-id="80371-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="80371-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80371-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="80371-116">-ListAvailable</span></span>
<span data-ttu-id="80371-117">Jelzi, hogy ez a művelet az összes elérhető erőforrás-szolgáltatót bekapja.</span><span class="sxs-lookup"><span data-stu-id="80371-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="80371-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="80371-118">-Location</span></span>
<span data-ttu-id="80371-119">Az erőforrás-szolgáltató helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80371-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="80371-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="80371-120">-Pre</span></span>
<span data-ttu-id="80371-121">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="80371-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="80371-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="80371-122">-ProviderNamespace</span></span>
<span data-ttu-id="80371-123">Az erőforrás-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80371-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="80371-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80371-124">CommonParameters</span></span>
<span data-ttu-id="80371-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80371-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80371-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80371-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80371-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80371-127">INPUTS</span></span>

## <span data-ttu-id="80371-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80371-128">OUTPUTS</span></span>

## <span data-ttu-id="80371-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80371-129">NOTES</span></span>

## <span data-ttu-id="80371-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80371-130">RELATED LINKS</span></span>

[<span data-ttu-id="80371-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="80371-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="80371-132">Regisztráció törlése – AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="80371-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


