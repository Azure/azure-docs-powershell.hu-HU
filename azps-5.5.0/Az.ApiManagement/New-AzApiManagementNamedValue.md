---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157594"
---
# <span data-ttu-id="9b0ad-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9b0ad-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="9b0ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0ad-103">Új elnevezett értéket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-103">Creates new Named Value.</span></span>

## <span data-ttu-id="9b0ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b0ad-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b0ad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b0ad-105">DESCRIPTION</span></span>
<span data-ttu-id="9b0ad-106">A **New-AzApiManagementNamedValue** parancsmag létrehoz egy Azure API Management **named Value értéket.**</span><span class="sxs-lookup"><span data-stu-id="9b0ad-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="9b0ad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b0ad-107">EXAMPLES</span></span>

### <span data-ttu-id="9b0ad-108">1. példa: Címkéket tartalmazó elnevezett érték létrehozása</span><span class="sxs-lookup"><span data-stu-id="9b0ad-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="9b0ad-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="9b0ad-110">A második parancs létrehoz egy elnevezett értéket, és a $Tags címkéként rendeli hozzá a tulajdonsághoz.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="9b0ad-111">2. példa: Elnevezett érték létrehozása titkos értékkel</span><span class="sxs-lookup"><span data-stu-id="9b0ad-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="9b0ad-112">Ez a parancs egy olyan **elnevezett értéket** hoz létre, amely titkosított értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="9b0ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b0ad-113">PARAMETERS</span></span>

### <span data-ttu-id="9b0ad-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9b0ad-114">-Context</span></span>
<span data-ttu-id="9b0ad-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9b0ad-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9b0ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0ad-117">-DefaultProfile</span></span>
<span data-ttu-id="9b0ad-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b0ad-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9b0ad-119">-Name</span></span>
<span data-ttu-id="9b0ad-120">A névvel megadott érték neve.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-120">Name of the named value.</span></span>
<span data-ttu-id="9b0ad-121">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="9b0ad-122">Csak betűket, számjegyeket, pontokat, kötőjeleket és aláhúzásjeleket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="9b0ad-123">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="9b0ad-124">-NamedValueId</span></span>
<span data-ttu-id="9b0ad-125">Az új elnevezett érték azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-125">Identifier of new named value.</span></span>
<span data-ttu-id="9b0ad-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-126">This parameter is optional.</span></span>
<span data-ttu-id="9b0ad-127">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-127">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="9b0ad-128">-Secret</span></span>
<span data-ttu-id="9b0ad-129">Meghatározza, hogy az érték titkos-e, és titkosítva kell-e lennie.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="9b0ad-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-130">This parameter is optional.</span></span>
<span data-ttu-id="9b0ad-131">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-131">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b0ad-132">-Tag</span></span>
<span data-ttu-id="9b0ad-133">Elnevezett értékhez társítható címkék.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="9b0ad-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-135">-Érték</span><span class="sxs-lookup"><span data-stu-id="9b0ad-135">-Value</span></span>
<span data-ttu-id="9b0ad-136">A névvel megadott érték értéke.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-136">Value of the named value.</span></span>
<span data-ttu-id="9b0ad-137">Tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-137">Can contain policy expressions.</span></span>
<span data-ttu-id="9b0ad-138">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="9b0ad-139">Lehet, hogy nem üres, vagy csak a szóközből áll.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="9b0ad-140">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b0ad-141">-Confirm</span></span>
<span data-ttu-id="9b0ad-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b0ad-143">-WhatIf</span></span>
<span data-ttu-id="9b0ad-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b0ad-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0ad-146">CommonParameters</span></span>
<span data-ttu-id="9b0ad-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0ad-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b0ad-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0ad-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b0ad-149">INPUTS</span></span>

### <span data-ttu-id="9b0ad-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b0ad-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b0ad-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9b0ad-151">System.String</span></span>

### <span data-ttu-id="9b0ad-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b0ad-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9b0ad-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9b0ad-153">System.String[]</span></span>

## <span data-ttu-id="9b0ad-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b0ad-154">OUTPUTS</span></span>

### <span data-ttu-id="9b0ad-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9b0ad-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="9b0ad-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b0ad-156">NOTES</span></span>

## <span data-ttu-id="9b0ad-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b0ad-157">RELATED LINKS</span></span>
