---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186929"
---
# <span data-ttu-id="fa152-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="fa152-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="fa152-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa152-102">SYNOPSIS</span></span>
<span data-ttu-id="fa152-103">Új elnevezett érték létrehozása</span><span class="sxs-lookup"><span data-stu-id="fa152-103">Creates new Named Value.</span></span>

## <span data-ttu-id="fa152-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa152-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa152-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa152-105">DESCRIPTION</span></span>
<span data-ttu-id="fa152-106">A **New-AzApiManagementNamedValue** parancsmag az Azure API-kezelési **névvel ellátott értéket** hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fa152-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="fa152-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fa152-107">EXAMPLES</span></span>

### <span data-ttu-id="fa152-108">1. példa: névvel ellátott érték létrehozása, amely tartalmazza a címkéket</span><span class="sxs-lookup"><span data-stu-id="fa152-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="fa152-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="fa152-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="fa152-110">A második parancs névvel ellátott értéket hoz létre, és a karakterláncokat a tulajdonságban címkékként rendeli hozzá a $Tags.</span><span class="sxs-lookup"><span data-stu-id="fa152-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="fa152-111">2. példa: névvel ellátott érték létrehozása titkos értékkel</span><span class="sxs-lookup"><span data-stu-id="fa152-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="fa152-112">A parancs létrehoz egy **névvel ellátott értéket** , amely egy titkosított értékkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="fa152-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="fa152-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa152-113">PARAMETERS</span></span>

### <span data-ttu-id="fa152-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fa152-114">-Context</span></span>
<span data-ttu-id="fa152-115">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="fa152-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fa152-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fa152-116">This parameter is required.</span></span>

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

### <span data-ttu-id="fa152-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa152-117">-DefaultProfile</span></span>
<span data-ttu-id="fa152-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa152-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa152-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa152-119">-Name</span></span>
<span data-ttu-id="fa152-120">A névvel ellátott érték neve</span><span class="sxs-lookup"><span data-stu-id="fa152-120">Name of the named value.</span></span>
<span data-ttu-id="fa152-121">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="fa152-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="fa152-122">Lehet, hogy csak betűk, számjegyek, pont, kötőjel és aláhúzás karaktereket tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="fa152-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="fa152-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fa152-123">This parameter is required.</span></span>

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

### <span data-ttu-id="fa152-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="fa152-124">-NamedValueId</span></span>
<span data-ttu-id="fa152-125">Az új névvel ellátott érték azonosítója</span><span class="sxs-lookup"><span data-stu-id="fa152-125">Identifier of new named value.</span></span>
<span data-ttu-id="fa152-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fa152-126">This parameter is optional.</span></span>
<span data-ttu-id="fa152-127">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="fa152-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="fa152-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="fa152-128">-Secret</span></span>
<span data-ttu-id="fa152-129">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="fa152-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="fa152-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fa152-130">This parameter is optional.</span></span>
<span data-ttu-id="fa152-131">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="fa152-131">Default Value is false.</span></span>

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

### <span data-ttu-id="fa152-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="fa152-132">-Tag</span></span>
<span data-ttu-id="fa152-133">Névvel ellátott értékkel társított Címkék</span><span class="sxs-lookup"><span data-stu-id="fa152-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="fa152-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fa152-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="fa152-135">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="fa152-135">-Value</span></span>
<span data-ttu-id="fa152-136">A névvel ellátott érték értéke</span><span class="sxs-lookup"><span data-stu-id="fa152-136">Value of the named value.</span></span>
<span data-ttu-id="fa152-137">Tartalmazhatnak házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="fa152-137">Can contain policy expressions.</span></span>
<span data-ttu-id="fa152-138">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="fa152-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="fa152-139">Lehet, hogy nem üres vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="fa152-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="fa152-140">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fa152-140">This parameter is required.</span></span>

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

### <span data-ttu-id="fa152-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa152-141">-Confirm</span></span>
<span data-ttu-id="fa152-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa152-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa152-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa152-143">-WhatIf</span></span>
<span data-ttu-id="fa152-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa152-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa152-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa152-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa152-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa152-146">CommonParameters</span></span>
<span data-ttu-id="fa152-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa152-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa152-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa152-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa152-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa152-149">INPUTS</span></span>

### <span data-ttu-id="fa152-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fa152-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fa152-151">System. String</span><span class="sxs-lookup"><span data-stu-id="fa152-151">System.String</span></span>

### <span data-ttu-id="fa152-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa152-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fa152-153">System. string []</span><span class="sxs-lookup"><span data-stu-id="fa152-153">System.String[]</span></span>

## <span data-ttu-id="fa152-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa152-154">OUTPUTS</span></span>

### <span data-ttu-id="fa152-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="fa152-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="fa152-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa152-156">NOTES</span></span>

## <span data-ttu-id="fa152-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa152-157">RELATED LINKS</span></span>
