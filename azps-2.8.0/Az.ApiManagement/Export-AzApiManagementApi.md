---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 7b4163b18905fd0676543de1b0ead26d11c7096a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668136"
---
# <span data-ttu-id="2e111-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e111-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="2e111-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e111-102">SYNOPSIS</span></span>
<span data-ttu-id="2e111-103">API-t exportál egy fájlba.</span><span class="sxs-lookup"><span data-stu-id="2e111-103">Exports an API to a file.</span></span>

## <span data-ttu-id="2e111-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e111-104">SYNTAX</span></span>

### <span data-ttu-id="2e111-105">ExportToPipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e111-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e111-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="2e111-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e111-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e111-107">DESCRIPTION</span></span>
<span data-ttu-id="2e111-108">Az **export-AzApiManagementApi** parancsmag az Azure API-kezelési API-t egy olyan fájlba exportálja, amely az egyik támogatott formátumba kerül.</span><span class="sxs-lookup"><span data-stu-id="2e111-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="2e111-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2e111-109">EXAMPLES</span></span>

### <span data-ttu-id="2e111-110">1. példa: API exportálása webalkalmazás-Leírás nyelve (WADL) formátumban</span><span class="sxs-lookup"><span data-stu-id="2e111-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="2e111-111">Ez a parancs API-t exportál egy WADL-fájlba.</span><span class="sxs-lookup"><span data-stu-id="2e111-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="2e111-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e111-112">PARAMETERS</span></span>

### <span data-ttu-id="2e111-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2e111-113">-ApiId</span></span>
<span data-ttu-id="2e111-114">Az exportálandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e111-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="2e111-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2e111-115">-ApiRevision</span></span>
<span data-ttu-id="2e111-116">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e111-116">Identifier of API Revision.</span></span> <span data-ttu-id="2e111-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2e111-117">This parameter is optional.</span></span> <span data-ttu-id="2e111-118">Ha nem adja meg, akkor az Exportálás a jelenleg aktív API-verzióra történik.</span><span class="sxs-lookup"><span data-stu-id="2e111-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="2e111-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2e111-119">-Context</span></span>
<span data-ttu-id="2e111-120">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2e111-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e111-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e111-121">-DefaultProfile</span></span>
<span data-ttu-id="2e111-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e111-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e111-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2e111-123">-Force</span></span>
<span data-ttu-id="2e111-124">Jelzi, hogy ez a művelet felülírja a fájl nevét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="2e111-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="2e111-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e111-125">-PassThru</span></span>
<span data-ttu-id="2e111-126">Jelzi, hogy a művelet az API $False sikeres exportálásakor visszaadja $True</span><span class="sxs-lookup"><span data-stu-id="2e111-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="2e111-127">-Saven</span><span class="sxs-lookup"><span data-stu-id="2e111-127">-SaveAs</span></span>
<span data-ttu-id="2e111-128">Annak a fájlnak az elérési útvonalát adja meg, amelybe az exportált API-t menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="2e111-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="2e111-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="2e111-129">-SpecificationFormat</span></span>
<span data-ttu-id="2e111-130">Az API formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e111-130">Specifies the API format.</span></span>
<span data-ttu-id="2e111-131">psdx_paramvalues Wadl és hencegés.</span><span class="sxs-lookup"><span data-stu-id="2e111-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e111-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e111-132">-Confirm</span></span>
<span data-ttu-id="2e111-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e111-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e111-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e111-134">-WhatIf</span></span>
<span data-ttu-id="2e111-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e111-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e111-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e111-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e111-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e111-137">CommonParameters</span></span>
<span data-ttu-id="2e111-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e111-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e111-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e111-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e111-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e111-140">INPUTS</span></span>

### <span data-ttu-id="2e111-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e111-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e111-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2e111-142">System.String</span></span>

### <span data-ttu-id="2e111-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="2e111-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="2e111-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e111-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e111-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e111-145">OUTPUTS</span></span>

### <span data-ttu-id="2e111-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2e111-146">System.String</span></span>

## <span data-ttu-id="2e111-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e111-147">NOTES</span></span>

## <span data-ttu-id="2e111-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e111-148">RELATED LINKS</span></span>

[<span data-ttu-id="2e111-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e111-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2e111-150">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e111-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2e111-151">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e111-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="2e111-152">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e111-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="2e111-153">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e111-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


