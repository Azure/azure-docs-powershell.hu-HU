---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679124"
---
# <span data-ttu-id="7b3f5-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b3f5-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="7b3f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3f5-103">API-t exportál egy fájlba.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b3f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b3f5-104">SYNTAX</span></span>

### <span data-ttu-id="7b3f5-105">Exportálás csővezetékbe (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b3f5-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b3f5-106">Exportálás fájlba</span><span class="sxs-lookup"><span data-stu-id="7b3f5-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b3f5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b3f5-107">DESCRIPTION</span></span>
<span data-ttu-id="7b3f5-108">Az **export-AzureRmApiManagementApi** parancsmag az Azure API-kezelési API-t egy olyan fájlba exportálja, amely az egyik támogatott formátumba kerül.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="7b3f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7b3f5-109">EXAMPLES</span></span>

### <span data-ttu-id="7b3f5-110">1. példa: API exportálása webalkalmazás-Leírás nyelve (WADL) formátumban</span><span class="sxs-lookup"><span data-stu-id="7b3f5-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="7b3f5-111">Ez a parancs API-t exportál egy WADL-fájlba.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="7b3f5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b3f5-112">PARAMETERS</span></span>

### <span data-ttu-id="7b3f5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7b3f5-113">-ApiId</span></span>
<span data-ttu-id="7b3f5-114">Az exportálandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="7b3f5-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7b3f5-115">-Context</span></span>
<span data-ttu-id="7b3f5-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7b3f5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7b3f5-117">-Force</span></span>
<span data-ttu-id="7b3f5-118">Jelzi, hogy ez a művelet felülírja a fájl nevét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3f5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b3f5-119">-PassThru</span></span>
<span data-ttu-id="7b3f5-120">Jelzi, hogy a művelet az API $False sikeres exportálásakor visszaadja $True</span><span class="sxs-lookup"><span data-stu-id="7b3f5-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3f5-121">-Saven</span><span class="sxs-lookup"><span data-stu-id="7b3f5-121">-SaveAs</span></span>
<span data-ttu-id="7b3f5-122">Annak a fájlnak az elérési útvonalát adja meg, amelybe az exportált API-t menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b3f5-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="7b3f5-123">-SpecificationFormat</span></span>
<span data-ttu-id="7b3f5-124">Az API formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-124">Specifies the API format.</span></span>
<span data-ttu-id="7b3f5-125">psdx_paramvalues Wadl és hencegés.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-125">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="7b3f5-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b3f5-126">-Confirm</span></span>
<span data-ttu-id="7b3f5-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b3f5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b3f5-128">-WhatIf</span></span>
<span data-ttu-id="7b3f5-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b3f5-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b3f5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3f5-131">-DefaultProfile</span></span>
<span data-ttu-id="7b3f5-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b3f5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3f5-133">CommonParameters</span></span>
<span data-ttu-id="7b3f5-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b3f5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3f5-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3f5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3f5-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b3f5-136">INPUTS</span></span>

## <span data-ttu-id="7b3f5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b3f5-137">OUTPUTS</span></span>

### <span data-ttu-id="7b3f5-138">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="7b3f5-138">String</span></span>
<span data-ttu-id="7b3f5-139">Ez a parancsmag az exportált API-tartalmat karakterláncként adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7b3f5-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="7b3f5-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b3f5-140">NOTES</span></span>

## <span data-ttu-id="7b3f5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b3f5-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b3f5-142">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b3f5-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b3f5-143">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b3f5-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b3f5-144">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b3f5-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b3f5-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b3f5-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="7b3f5-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b3f5-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


