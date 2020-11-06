---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 62acee0398c9530a54e02c2347bf384498b07196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503960"
---
# <span data-ttu-id="46c09-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="46c09-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="46c09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46c09-102">SYNOPSIS</span></span>
<span data-ttu-id="46c09-103">Minden hely és a támogatott erőforrás-szolgáltatók beolvasása minden helyhez.</span><span class="sxs-lookup"><span data-stu-id="46c09-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46c09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46c09-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46c09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46c09-105">DESCRIPTION</span></span>
<span data-ttu-id="46c09-106">A **Get-AzureRmLocation** parancsmag minden helyhez megkapja a minden helyet és a támogatott erőforrás-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="46c09-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="46c09-107">Példák</span><span class="sxs-lookup"><span data-stu-id="46c09-107">EXAMPLES</span></span>

### <span data-ttu-id="46c09-108">1. példa: a minden hely és a támogatott erőforrás-szolgáltatók beolvasása</span><span class="sxs-lookup"><span data-stu-id="46c09-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="46c09-109">Ez a parancs minden helyet és a támogatott erőforrás-szolgáltatókat beolvassa az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="46c09-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="46c09-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46c09-110">PARAMETERS</span></span>

### <span data-ttu-id="46c09-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="46c09-111">-ApiVersion</span></span>
<span data-ttu-id="46c09-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="46c09-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="46c09-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="46c09-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="46c09-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="46c09-114">-Pre</span></span>
<span data-ttu-id="46c09-115">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="46c09-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="46c09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c09-116">-DefaultProfile</span></span>
<span data-ttu-id="46c09-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46c09-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c09-118">CommonParameters</span></span>
<span data-ttu-id="46c09-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46c09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c09-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c09-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c09-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46c09-121">INPUTS</span></span>

## <span data-ttu-id="46c09-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46c09-122">OUTPUTS</span></span>

### <span data-ttu-id="46c09-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="46c09-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="46c09-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46c09-124">NOTES</span></span>

## <span data-ttu-id="46c09-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46c09-125">RELATED LINKS</span></span>

