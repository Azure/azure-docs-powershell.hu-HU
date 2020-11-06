---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495498"
---
# <span data-ttu-id="f567d-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="f567d-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="f567d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f567d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f567d-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f567d-103">SYNTAX</span></span>

### <span data-ttu-id="f567d-104">GetAllProperties (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f567d-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f567d-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="f567d-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f567d-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="f567d-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f567d-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="f567d-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f567d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f567d-108">DESCRIPTION</span></span>

## <span data-ttu-id="f567d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f567d-109">EXAMPLES</span></span>

### <span data-ttu-id="f567d-110">Példa 1: tulajdonság beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="f567d-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="f567d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f567d-111">PARAMETERS</span></span>

### <span data-ttu-id="f567d-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f567d-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f567d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f567d-113">-DefaultProfile</span></span>
<span data-ttu-id="f567d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f567d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f567d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f567d-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f567d-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="f567d-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f567d-117">-Címke</span><span class="sxs-lookup"><span data-stu-id="f567d-117">-Tag</span></span>
<span data-ttu-id="f567d-118">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="f567d-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f567d-119">Példa:</span><span class="sxs-lookup"><span data-stu-id="f567d-119">For example:</span></span>

<span data-ttu-id="f567d-120">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f567d-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f567d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f567d-121">CommonParameters</span></span>
<span data-ttu-id="f567d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f567d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f567d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f567d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f567d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f567d-124">INPUTS</span></span>

### <span data-ttu-id="f567d-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="f567d-125">None</span></span>
<span data-ttu-id="f567d-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f567d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f567d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f567d-127">OUTPUTS</span></span>

### <span data-ttu-id="f567d-128">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="f567d-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="f567d-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="f567d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="f567d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f567d-130">NOTES</span></span>

## <span data-ttu-id="f567d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f567d-131">RELATED LINKS</span></span>

