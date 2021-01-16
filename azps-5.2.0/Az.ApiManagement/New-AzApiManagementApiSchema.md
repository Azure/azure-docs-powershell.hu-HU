---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349073"
---
# <span data-ttu-id="e8033-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e8033-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="e8033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8033-102">SYNOPSIS</span></span>
<span data-ttu-id="e8033-103">Az új API-séma létrehozása az ApiManagement szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="e8033-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="e8033-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8033-104">SYNTAX</span></span>

### <span data-ttu-id="e8033-105">SchemaDocumentInline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8033-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8033-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="e8033-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8033-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8033-107">DESCRIPTION</span></span>
<span data-ttu-id="e8033-108">Létrehozza az API új API-sémáját.</span><span class="sxs-lookup"><span data-stu-id="e8033-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="e8033-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8033-109">EXAMPLES</span></span>

### <span data-ttu-id="e8033-110">1. példa: Új séma létrehozása a Swagger Petstore extensive API-hoz</span><span class="sxs-lookup"><span data-stu-id="e8033-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="e8033-111">A **New-AzApiManagementApiSchema** parancsmag létrehozza vagy frissíti az `swagger-petstore-extensive` aPI sémáját.</span><span class="sxs-lookup"><span data-stu-id="e8033-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="e8033-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8033-112">PARAMETERS</span></span>

### <span data-ttu-id="e8033-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e8033-113">-ApiId</span></span>
<span data-ttu-id="e8033-114">Az api azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e8033-114">Identifier of api.</span></span> <span data-ttu-id="e8033-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e8033-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e8033-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e8033-116">-Context</span></span>
<span data-ttu-id="e8033-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e8033-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8033-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e8033-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8033-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8033-119">-DefaultProfile</span></span>
<span data-ttu-id="e8033-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8033-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8033-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="e8033-121">-SchemaDocument</span></span>
<span data-ttu-id="e8033-122">Api-sémadokumentum karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="e8033-122">Api schema document as a string.</span></span> <span data-ttu-id="e8033-123">Ez a paraméter kötelező, mert a -SchemaDocumentFile nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e8033-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8033-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="e8033-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="e8033-125">Az api-séma ContentType-típusa.</span><span class="sxs-lookup"><span data-stu-id="e8033-125">ContentType of the api Schema.</span></span> <span data-ttu-id="e8033-126">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e8033-126">This parameter is required.</span></span>

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

### <span data-ttu-id="e8033-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="e8033-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="e8033-128">Api-sémadokumentum fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e8033-128">Api schema document file path.</span></span> <span data-ttu-id="e8033-129">Ez a paraméter kötelező, mert nincs megadva a -SchemaDocument paraméter.</span><span class="sxs-lookup"><span data-stu-id="e8033-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8033-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="e8033-130">-SchemaId</span></span>
<span data-ttu-id="e8033-131">Az új séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e8033-131">Identifier of new schema.</span></span>
<span data-ttu-id="e8033-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e8033-132">This parameter is optional.</span></span>
<span data-ttu-id="e8033-133">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="e8033-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e8033-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8033-134">-Confirm</span></span>
<span data-ttu-id="e8033-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e8033-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8033-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8033-136">-WhatIf</span></span>
<span data-ttu-id="e8033-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e8033-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8033-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8033-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8033-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8033-139">CommonParameters</span></span>
<span data-ttu-id="e8033-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8033-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8033-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8033-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8033-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8033-142">INPUTS</span></span>

### <span data-ttu-id="e8033-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8033-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8033-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e8033-144">System.String</span></span>

## <span data-ttu-id="e8033-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8033-145">OUTPUTS</span></span>

### <span data-ttu-id="e8033-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e8033-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="e8033-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8033-147">NOTES</span></span>

## <span data-ttu-id="e8033-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8033-148">RELATED LINKS</span></span>

[<span data-ttu-id="e8033-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e8033-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="e8033-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e8033-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="e8033-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e8033-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
