---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205735"
---
# <span data-ttu-id="2eb08-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2eb08-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2eb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eb08-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb08-103">Listát vagy adott elnevezett értéket kap.</span><span class="sxs-lookup"><span data-stu-id="2eb08-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="2eb08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2eb08-104">SYNTAX</span></span>

### <span data-ttu-id="2eb08-105">GetAllNamedValues (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2eb08-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2eb08-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="2eb08-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb08-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="2eb08-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb08-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="2eb08-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb08-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2eb08-109">DESCRIPTION</span></span>
<span data-ttu-id="2eb08-110">A **Get-AzApiManagementNamedValue** parancsmag kap egy listát vagy egy adott elnevezett értéket.</span><span class="sxs-lookup"><span data-stu-id="2eb08-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="2eb08-111">Az érték nem fog szerepelni az eredmény részleteiben, ha a névvel ellátott érték titkosként van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="2eb08-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="2eb08-112">Titkos érték bekeresése: **Get-AzApiManagementNamedValueSecretValue.**</span><span class="sxs-lookup"><span data-stu-id="2eb08-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="2eb08-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2eb08-113">EXAMPLES</span></span>

### <span data-ttu-id="2eb08-114">1. példa: Névvel megadott érték lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="2eb08-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="2eb08-115">Ez a parancs megkapja az elnevezett érték részleteit az elnevezett értéknév alapján.</span><span class="sxs-lookup"><span data-stu-id="2eb08-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="2eb08-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eb08-116">PARAMETERS</span></span>

### <span data-ttu-id="2eb08-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2eb08-117">-Context</span></span>
<span data-ttu-id="2eb08-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="2eb08-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2eb08-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="2eb08-119">This parameter is required.</span></span>

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

### <span data-ttu-id="2eb08-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb08-120">-DefaultProfile</span></span>
<span data-ttu-id="2eb08-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eb08-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb08-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb08-122">-Name</span></span>
<span data-ttu-id="2eb08-123">Név karakterláncot tartalmazó elnevezett értékeket keres.</span><span class="sxs-lookup"><span data-stu-id="2eb08-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="2eb08-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2eb08-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="2eb08-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="2eb08-125">-NamedValueId</span></span>
<span data-ttu-id="2eb08-126">A megnevezett érték azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2eb08-126">Identifier of the named value.</span></span>
<span data-ttu-id="2eb08-127">Ha meg van adva, akkor a névvel megadott értéket az azonosító alapján próbálja megtalálni.</span><span class="sxs-lookup"><span data-stu-id="2eb08-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="2eb08-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2eb08-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="2eb08-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="2eb08-129">-Tag</span></span>
<span data-ttu-id="2eb08-130">A címkékkel társított elnevezett értékeket megkeresi.</span><span class="sxs-lookup"><span data-stu-id="2eb08-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="2eb08-131">Ha meg van adva, akkor a címkével társított összes tulajdonságot visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2eb08-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="2eb08-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2eb08-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="2eb08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb08-133">CommonParameters</span></span>
<span data-ttu-id="2eb08-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb08-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eb08-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb08-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eb08-136">INPUTS</span></span>

### <span data-ttu-id="2eb08-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2eb08-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2eb08-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2eb08-138">System.String</span></span>

## <span data-ttu-id="2eb08-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eb08-139">OUTPUTS</span></span>

### <span data-ttu-id="2eb08-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2eb08-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="2eb08-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2eb08-141">NOTES</span></span>

## <span data-ttu-id="2eb08-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eb08-142">RELATED LINKS</span></span>
