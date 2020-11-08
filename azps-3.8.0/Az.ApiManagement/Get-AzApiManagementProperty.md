---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: a1ca7766efc79d3d9db2d8feef94a2bb7aab9c36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011922"
---
# <span data-ttu-id="fe81b-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="fe81b-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="fe81b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe81b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe81b-103">Egy lista vagy egy adott tulajdonság (névvel ellátott érték) beolvasása</span><span class="sxs-lookup"><span data-stu-id="fe81b-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="fe81b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe81b-104">SYNTAX</span></span>

### <span data-ttu-id="fe81b-105">GetAllProperties (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe81b-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe81b-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="fe81b-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe81b-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="fe81b-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe81b-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="fe81b-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe81b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe81b-109">DESCRIPTION</span></span>
<span data-ttu-id="fe81b-110">A **Get-AzApiManagementProperty** parancsmag egy listát vagy egy adott tulajdonságot kap.</span><span class="sxs-lookup"><span data-stu-id="fe81b-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="fe81b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fe81b-111">EXAMPLES</span></span>

### <span data-ttu-id="fe81b-112">Példa 1: tulajdonság beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="fe81b-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="fe81b-113">Ez a parancs a tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe81b-113">This command gets the property details given the property name.</span></span>

## <span data-ttu-id="fe81b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe81b-114">PARAMETERS</span></span>

### <span data-ttu-id="fe81b-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fe81b-115">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe81b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe81b-116">-DefaultProfile</span></span>
<span data-ttu-id="fe81b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe81b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe81b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe81b-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe81b-119">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="fe81b-119">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe81b-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="fe81b-120">-Tag</span></span>
<span data-ttu-id="fe81b-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fe81b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe81b-122">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fe81b-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe81b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe81b-123">CommonParameters</span></span>
<span data-ttu-id="fe81b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe81b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe81b-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe81b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe81b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe81b-126">INPUTS</span></span>

### <span data-ttu-id="fe81b-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe81b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe81b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fe81b-128">System.String</span></span>

## <span data-ttu-id="fe81b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe81b-129">OUTPUTS</span></span>

### <span data-ttu-id="fe81b-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="fe81b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="fe81b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe81b-131">NOTES</span></span>

## <span data-ttu-id="fe81b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe81b-132">RELATED LINKS</span></span>
