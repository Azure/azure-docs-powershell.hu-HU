---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302243"
---
# <span data-ttu-id="aa33a-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="aa33a-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="aa33a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa33a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa33a-103">Listát vagy adott névvel ellátott értéket kap.</span><span class="sxs-lookup"><span data-stu-id="aa33a-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="aa33a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa33a-104">SYNTAX</span></span>

### <span data-ttu-id="aa33a-105">GetAllNamedValues (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa33a-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa33a-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="aa33a-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa33a-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="aa33a-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa33a-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="aa33a-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa33a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa33a-109">DESCRIPTION</span></span>
<span data-ttu-id="aa33a-110">A **Get-AzApiManagementNamedValue** parancsmag egy listát vagy egy adott névvel ellátott értéket kap.</span><span class="sxs-lookup"><span data-stu-id="aa33a-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="aa33a-111">Ha a névvel ellátott érték titkosként van megjelölve, az érték nem fog szerepelni az eredményben.</span><span class="sxs-lookup"><span data-stu-id="aa33a-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="aa33a-112">Ha titkos értéket szeretne kapni, használja a **Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="aa33a-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="aa33a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="aa33a-113">EXAMPLES</span></span>

### <span data-ttu-id="aa33a-114">Példa 1: elnevezett érték beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="aa33a-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="aa33a-115">Ez a parancs a névvel ellátott érték nevében adja meg az elnevezett érték adatait.</span><span class="sxs-lookup"><span data-stu-id="aa33a-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="aa33a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa33a-116">PARAMETERS</span></span>

### <span data-ttu-id="aa33a-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aa33a-117">-Context</span></span>
<span data-ttu-id="aa33a-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="aa33a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aa33a-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="aa33a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="aa33a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa33a-120">-DefaultProfile</span></span>
<span data-ttu-id="aa33a-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa33a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa33a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa33a-122">-Name</span></span>
<span data-ttu-id="aa33a-123">Megkeresi a névvel ellátott értékeket a karakterlánc nevét tartalmazó nevekkel.</span><span class="sxs-lookup"><span data-stu-id="aa33a-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="aa33a-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="aa33a-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa33a-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="aa33a-125">-NamedValueId</span></span>
<span data-ttu-id="aa33a-126">A névvel ellátott érték azonosítója</span><span class="sxs-lookup"><span data-stu-id="aa33a-126">Identifier of the named value.</span></span>
<span data-ttu-id="aa33a-127">Ha meg van adva a megnevezett érték, akkor az azonosító segítségével keresheti meg.</span><span class="sxs-lookup"><span data-stu-id="aa33a-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="aa33a-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="aa33a-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa33a-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="aa33a-129">-Tag</span></span>
<span data-ttu-id="aa33a-130">Megkeresi a címkéhez társított elnevezett értékeket.</span><span class="sxs-lookup"><span data-stu-id="aa33a-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="aa33a-131">Ha meg van adva, akkor a címkéhez társított összes tulajdonságot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="aa33a-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="aa33a-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="aa33a-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa33a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa33a-133">CommonParameters</span></span>
<span data-ttu-id="aa33a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa33a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa33a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa33a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa33a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa33a-136">INPUTS</span></span>

### <span data-ttu-id="aa33a-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa33a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa33a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="aa33a-138">System.String</span></span>

## <span data-ttu-id="aa33a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa33a-139">OUTPUTS</span></span>

### <span data-ttu-id="aa33a-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="aa33a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="aa33a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa33a-141">NOTES</span></span>

## <span data-ttu-id="aa33a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa33a-142">RELATED LINKS</span></span>
