---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299936"
---
# <span data-ttu-id="efc68-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="efc68-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="efc68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efc68-102">SYNOPSIS</span></span>
<span data-ttu-id="efc68-103">API-t exportál egy fájlba.</span><span class="sxs-lookup"><span data-stu-id="efc68-103">Exports an API to a file.</span></span>

## <span data-ttu-id="efc68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efc68-104">SYNTAX</span></span>

### <span data-ttu-id="efc68-105">ExportToPipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efc68-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc68-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="efc68-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc68-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="efc68-107">DESCRIPTION</span></span>
<span data-ttu-id="efc68-108">Az **export-AzApiManagementApi** parancsmag az Azure API-kezelési API-t egy olyan fájlba exportálja, amely az egyik támogatott formátumba kerül.</span><span class="sxs-lookup"><span data-stu-id="efc68-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="efc68-109">Példák</span><span class="sxs-lookup"><span data-stu-id="efc68-109">EXAMPLES</span></span>

### <span data-ttu-id="efc68-110">1. példa: API exportálása webalkalmazás-Leírás nyelve (WADL) formátumban</span><span class="sxs-lookup"><span data-stu-id="efc68-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="efc68-111">Ez a parancs API-t exportál egy WADL-fájlba.</span><span class="sxs-lookup"><span data-stu-id="efc68-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="efc68-112">2. példa: API exportálása a OpenApi 3,0 specifikációs formátumban, JSON-dokumentumként</span><span class="sxs-lookup"><span data-stu-id="efc68-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="efc68-113">Ez a parancs egy API-definíciót exportál a nyílt API-formátumban JSON-dokumentumként</span><span class="sxs-lookup"><span data-stu-id="efc68-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="efc68-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efc68-114">PARAMETERS</span></span>

### <span data-ttu-id="efc68-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="efc68-115">-ApiId</span></span>
<span data-ttu-id="efc68-116">Az exportálandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="efc68-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="efc68-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="efc68-117">-ApiRevision</span></span>
<span data-ttu-id="efc68-118">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="efc68-118">Identifier of API Revision.</span></span> <span data-ttu-id="efc68-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="efc68-119">This parameter is optional.</span></span> <span data-ttu-id="efc68-120">Ha nem adja meg, akkor az Exportálás a jelenleg aktív API-verzióra történik.</span><span class="sxs-lookup"><span data-stu-id="efc68-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="efc68-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="efc68-121">-Context</span></span>
<span data-ttu-id="efc68-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="efc68-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="efc68-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc68-123">-DefaultProfile</span></span>
<span data-ttu-id="efc68-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efc68-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efc68-125">-Force</span><span class="sxs-lookup"><span data-stu-id="efc68-125">-Force</span></span>
<span data-ttu-id="efc68-126">Jelzi, hogy ez a művelet felülírja a fájl nevét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="efc68-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="efc68-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efc68-127">-PassThru</span></span>
<span data-ttu-id="efc68-128">Jelzi, hogy a művelet az API $False sikeres exportálásakor visszaadja $True</span><span class="sxs-lookup"><span data-stu-id="efc68-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="efc68-129">-Saven</span><span class="sxs-lookup"><span data-stu-id="efc68-129">-SaveAs</span></span>
<span data-ttu-id="efc68-130">Annak a fájlnak az elérési útvonalát adja meg, amelybe az exportált API-t menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="efc68-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="efc68-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="efc68-131">-SpecificationFormat</span></span>
<span data-ttu-id="efc68-132">Az API formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="efc68-132">Specifies the API format.</span></span>
<span data-ttu-id="efc68-133">psdx_paramvalues Wadl, WSDL, hencegés, OpenApi és OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="efc68-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="efc68-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="efc68-134">-Confirm</span></span>
<span data-ttu-id="efc68-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efc68-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc68-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc68-136">-WhatIf</span></span>
<span data-ttu-id="efc68-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="efc68-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc68-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efc68-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc68-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc68-139">CommonParameters</span></span>
<span data-ttu-id="efc68-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efc68-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc68-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="efc68-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc68-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efc68-142">INPUTS</span></span>

### <span data-ttu-id="efc68-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="efc68-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="efc68-144">System. String</span><span class="sxs-lookup"><span data-stu-id="efc68-144">System.String</span></span>

### <span data-ttu-id="efc68-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="efc68-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="efc68-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="efc68-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="efc68-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efc68-147">OUTPUTS</span></span>

### <span data-ttu-id="efc68-148">System. String</span><span class="sxs-lookup"><span data-stu-id="efc68-148">System.String</span></span>

## <span data-ttu-id="efc68-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efc68-149">NOTES</span></span>

## <span data-ttu-id="efc68-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efc68-150">RELATED LINKS</span></span>

[<span data-ttu-id="efc68-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="efc68-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="efc68-152">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="efc68-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="efc68-153">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="efc68-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="efc68-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="efc68-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="efc68-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="efc68-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


