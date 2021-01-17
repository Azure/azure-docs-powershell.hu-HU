---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479033"
---
# <span data-ttu-id="45635-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45635-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="45635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45635-102">SYNOPSIS</span></span>
<span data-ttu-id="45635-103">API exportálása fájlba.</span><span class="sxs-lookup"><span data-stu-id="45635-103">Exports an API to a file.</span></span>

## <span data-ttu-id="45635-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="45635-104">SYNTAX</span></span>

### <span data-ttu-id="45635-105">ExportToPipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45635-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45635-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="45635-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45635-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="45635-107">DESCRIPTION</span></span>
<span data-ttu-id="45635-108">Az **Export-AzApiManagementApi** parancsmag egy Azure API felügyeleti API-t exportál egy fájlba az egyik támogatott formátumban.</span><span class="sxs-lookup"><span data-stu-id="45635-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="45635-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="45635-109">EXAMPLES</span></span>

### <span data-ttu-id="45635-110">1. példa: API exportálása webalkalmazás-leírási nyelv (WADL) formátumban</span><span class="sxs-lookup"><span data-stu-id="45635-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="45635-111">Ez a parancs egy API-t exportál egy WADL-fájlba.</span><span class="sxs-lookup"><span data-stu-id="45635-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="45635-112">2. példa: API exportálása OpenApi 3.0 specifikációformátumban Json-dokumentumként</span><span class="sxs-lookup"><span data-stu-id="45635-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="45635-113">Ez a parancs egy API-definíciót exportál Open Api formátumban Json-dokumentumként</span><span class="sxs-lookup"><span data-stu-id="45635-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="45635-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45635-114">PARAMETERS</span></span>

### <span data-ttu-id="45635-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="45635-115">-ApiId</span></span>
<span data-ttu-id="45635-116">Az exportálni használt API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45635-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="45635-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="45635-117">-ApiRevision</span></span>
<span data-ttu-id="45635-118">Az API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45635-118">Identifier of API Revision.</span></span> <span data-ttu-id="45635-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="45635-119">This parameter is optional.</span></span> <span data-ttu-id="45635-120">Ha nincs megadva, az exportálás az aktuálisan aktív API-változatban történik.</span><span class="sxs-lookup"><span data-stu-id="45635-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="45635-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="45635-121">-Context</span></span>
<span data-ttu-id="45635-122">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="45635-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="45635-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45635-123">-DefaultProfile</span></span>
<span data-ttu-id="45635-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45635-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45635-125">-Force</span><span class="sxs-lookup"><span data-stu-id="45635-125">-Force</span></span>
<span data-ttu-id="45635-126">Azt jelzi, hogy ez a művelet felülírja az azonos nevű fájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="45635-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45635-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45635-127">-PassThru</span></span>
<span data-ttu-id="45635-128">Azt jelzi, hogy a művelet sikeres $True, ha az API-t sikeresen exportálta, $False műveletet.</span><span class="sxs-lookup"><span data-stu-id="45635-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45635-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="45635-129">-SaveAs</span></span>
<span data-ttu-id="45635-130">Megadja az exportált API mentésének elérési útját.</span><span class="sxs-lookup"><span data-stu-id="45635-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45635-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="45635-131">-SpecificationFormat</span></span>
<span data-ttu-id="45635-132">Az API formátumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="45635-132">Specifies the API format.</span></span>
<span data-ttu-id="45635-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi és OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="45635-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45635-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45635-134">-Confirm</span></span>
<span data-ttu-id="45635-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="45635-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45635-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45635-136">-WhatIf</span></span>
<span data-ttu-id="45635-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="45635-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45635-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45635-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45635-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45635-139">CommonParameters</span></span>
<span data-ttu-id="45635-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45635-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45635-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45635-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45635-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45635-142">INPUTS</span></span>

### <span data-ttu-id="45635-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45635-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45635-144">System.String</span><span class="sxs-lookup"><span data-stu-id="45635-144">System.String</span></span>

### <span data-ttu-id="45635-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="45635-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="45635-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45635-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45635-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45635-147">OUTPUTS</span></span>

### <span data-ttu-id="45635-148">System.String</span><span class="sxs-lookup"><span data-stu-id="45635-148">System.String</span></span>

## <span data-ttu-id="45635-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="45635-149">NOTES</span></span>

## <span data-ttu-id="45635-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45635-150">RELATED LINKS</span></span>

[<span data-ttu-id="45635-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45635-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="45635-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45635-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="45635-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45635-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="45635-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45635-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="45635-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45635-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


