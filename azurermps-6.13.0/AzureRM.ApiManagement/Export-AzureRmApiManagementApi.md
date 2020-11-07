---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672811"
---
# <span data-ttu-id="9164f-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9164f-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="9164f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9164f-102">SYNOPSIS</span></span>
<span data-ttu-id="9164f-103">API-t exportál egy fájlba.</span><span class="sxs-lookup"><span data-stu-id="9164f-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9164f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9164f-104">SYNTAX</span></span>

### <span data-ttu-id="9164f-105">ExportToPipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9164f-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9164f-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="9164f-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9164f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9164f-107">DESCRIPTION</span></span>
<span data-ttu-id="9164f-108">Az **export-AzureRmApiManagementApi** parancsmag az Azure API-kezelési API-t egy olyan fájlba exportálja, amely az egyik támogatott formátumba kerül.</span><span class="sxs-lookup"><span data-stu-id="9164f-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="9164f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9164f-109">EXAMPLES</span></span>

### <span data-ttu-id="9164f-110">1. példa: API exportálása webalkalmazás-Leírás nyelve (WADL) formátumban</span><span class="sxs-lookup"><span data-stu-id="9164f-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="9164f-111">Ez a parancs API-t exportál egy WADL-fájlba.</span><span class="sxs-lookup"><span data-stu-id="9164f-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="9164f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9164f-112">PARAMETERS</span></span>

### <span data-ttu-id="9164f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9164f-113">-ApiId</span></span>
<span data-ttu-id="9164f-114">Az exportálandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9164f-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="9164f-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9164f-115">-ApiRevision</span></span>
<span data-ttu-id="9164f-116">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="9164f-116">Identifier of API Revision.</span></span> <span data-ttu-id="9164f-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9164f-117">This parameter is optional.</span></span> <span data-ttu-id="9164f-118">Ha nem adja meg, akkor az Exportálás a jelenleg aktív API-verzióra történik.</span><span class="sxs-lookup"><span data-stu-id="9164f-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="9164f-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9164f-119">-Context</span></span>
<span data-ttu-id="9164f-120">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9164f-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9164f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9164f-121">-DefaultProfile</span></span>
<span data-ttu-id="9164f-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9164f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9164f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9164f-123">-Force</span></span>
<span data-ttu-id="9164f-124">Jelzi, hogy ez a művelet felülírja a fájl nevét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="9164f-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="9164f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9164f-125">-PassThru</span></span>
<span data-ttu-id="9164f-126">Jelzi, hogy a művelet az API $False sikeres exportálásakor visszaadja $True</span><span class="sxs-lookup"><span data-stu-id="9164f-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="9164f-127">-Saven</span><span class="sxs-lookup"><span data-stu-id="9164f-127">-SaveAs</span></span>
<span data-ttu-id="9164f-128">Annak a fájlnak az elérési útvonalát adja meg, amelybe az exportált API-t menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="9164f-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="9164f-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="9164f-129">-SpecificationFormat</span></span>
<span data-ttu-id="9164f-130">Az API formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9164f-130">Specifies the API format.</span></span>
<span data-ttu-id="9164f-131">psdx_paramvalues Wadl és hencegés.</span><span class="sxs-lookup"><span data-stu-id="9164f-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9164f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9164f-132">-Confirm</span></span>
<span data-ttu-id="9164f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9164f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9164f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9164f-134">-WhatIf</span></span>
<span data-ttu-id="9164f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9164f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9164f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9164f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9164f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9164f-137">CommonParameters</span></span>
<span data-ttu-id="9164f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9164f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9164f-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9164f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9164f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9164f-140">INPUTS</span></span>

### <span data-ttu-id="9164f-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9164f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9164f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9164f-142">System.String</span></span>

### <span data-ttu-id="9164f-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="9164f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="9164f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9164f-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9164f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9164f-145">OUTPUTS</span></span>

### <span data-ttu-id="9164f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9164f-146">System.String</span></span>
<span data-ttu-id="9164f-147">Ez a parancsmag az exportált API-tartalmat karakterláncként adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9164f-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="9164f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9164f-148">NOTES</span></span>

## <span data-ttu-id="9164f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9164f-149">RELATED LINKS</span></span>

[<span data-ttu-id="9164f-150">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9164f-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="9164f-151">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9164f-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="9164f-152">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9164f-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="9164f-153">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9164f-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="9164f-154">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9164f-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


