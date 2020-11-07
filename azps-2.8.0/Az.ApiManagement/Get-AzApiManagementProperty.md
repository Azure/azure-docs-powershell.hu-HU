---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: 2c8fc24d252fce12e7adf9ee824db0e1b2c8b206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668098"
---
# <span data-ttu-id="87176-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="87176-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="87176-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87176-102">SYNOPSIS</span></span>
<span data-ttu-id="87176-103">Egy lista vagy egy adott tulajdonság (névvel ellátott érték) beolvasása</span><span class="sxs-lookup"><span data-stu-id="87176-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="87176-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87176-104">SYNTAX</span></span>

### <span data-ttu-id="87176-105">GetAllProperties (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87176-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87176-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="87176-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87176-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="87176-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87176-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="87176-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87176-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="87176-109">DESCRIPTION</span></span>
<span data-ttu-id="87176-110">A **Get-AzApiManagementProperty** parancsmag egy listát vagy egy adott tulajdonságot kap.</span><span class="sxs-lookup"><span data-stu-id="87176-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="87176-111">Példák</span><span class="sxs-lookup"><span data-stu-id="87176-111">EXAMPLES</span></span>

### <span data-ttu-id="87176-112">Példa 1: tulajdonság beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="87176-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="87176-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87176-113">PARAMETERS</span></span>

### <span data-ttu-id="87176-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="87176-114">-Context</span></span>
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

### <span data-ttu-id="87176-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87176-115">-DefaultProfile</span></span>
<span data-ttu-id="87176-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87176-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87176-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87176-117">-Name</span></span>
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

### <span data-ttu-id="87176-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="87176-118">-PropertyId</span></span>
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

### <span data-ttu-id="87176-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="87176-119">-Tag</span></span>
<span data-ttu-id="87176-120">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="87176-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="87176-121">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="87176-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="87176-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87176-122">CommonParameters</span></span>
<span data-ttu-id="87176-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87176-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87176-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87176-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87176-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87176-125">INPUTS</span></span>

### <span data-ttu-id="87176-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87176-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87176-127">System. String</span><span class="sxs-lookup"><span data-stu-id="87176-127">System.String</span></span>

## <span data-ttu-id="87176-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87176-128">OUTPUTS</span></span>

### <span data-ttu-id="87176-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="87176-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="87176-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87176-130">NOTES</span></span>

## <span data-ttu-id="87176-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87176-131">RELATED LINKS</span></span>
