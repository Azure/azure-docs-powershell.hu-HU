---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672779"
---
# <span data-ttu-id="51270-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="51270-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="51270-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51270-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51270-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51270-103">SYNTAX</span></span>

### <span data-ttu-id="51270-104">Az összes tulajdonság beolvasása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51270-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51270-105">Get by Property ID</span><span class="sxs-lookup"><span data-stu-id="51270-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51270-106">Nevet tartalmazó tulajdonságok keresése</span><span class="sxs-lookup"><span data-stu-id="51270-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51270-107">Tulajdonságok keresése címke szerint</span><span class="sxs-lookup"><span data-stu-id="51270-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51270-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="51270-108">DESCRIPTION</span></span>

## <span data-ttu-id="51270-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51270-109">EXAMPLES</span></span>

### <span data-ttu-id="51270-110">1:</span><span class="sxs-lookup"><span data-stu-id="51270-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="51270-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51270-111">PARAMETERS</span></span>

### <span data-ttu-id="51270-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="51270-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51270-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51270-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51270-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="51270-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51270-115">-Címke</span><span class="sxs-lookup"><span data-stu-id="51270-115">-Tag</span></span>
<span data-ttu-id="51270-116">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="51270-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51270-117">Példa:</span><span class="sxs-lookup"><span data-stu-id="51270-117">For example:</span></span>

<span data-ttu-id="51270-118">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="51270-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51270-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51270-119">-DefaultProfile</span></span>
<span data-ttu-id="51270-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51270-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51270-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51270-121">CommonParameters</span></span>
<span data-ttu-id="51270-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51270-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51270-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51270-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51270-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51270-124">INPUTS</span></span>

## <span data-ttu-id="51270-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51270-125">OUTPUTS</span></span>

### <span data-ttu-id="51270-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="51270-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="51270-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="51270-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="51270-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51270-128">NOTES</span></span>

## <span data-ttu-id="51270-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51270-129">RELATED LINKS</span></span>

