---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187883"
---
# <span data-ttu-id="3b563-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b563-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="3b563-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b563-102">SYNOPSIS</span></span>
<span data-ttu-id="3b563-103">Az új API-séma létrehozása a ApiManagement szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="3b563-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="3b563-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b563-104">SYNTAX</span></span>

### <span data-ttu-id="3b563-105">SchemaDocumentInline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b563-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b563-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="3b563-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b563-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b563-107">DESCRIPTION</span></span>
<span data-ttu-id="3b563-108">Létrehozza az API új API-sémáját.</span><span class="sxs-lookup"><span data-stu-id="3b563-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="3b563-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3b563-109">EXAMPLES</span></span>

### <span data-ttu-id="3b563-110">1. példa: új séma létrehozása a hencegő petstore kiterjedt API-hoz</span><span class="sxs-lookup"><span data-stu-id="3b563-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="3b563-111">A **New-AzApiManagementApiSchema** parancsmag létrehoz vagy frissít az aPI sémájáról `swagger-petstore-extensive` .</span><span class="sxs-lookup"><span data-stu-id="3b563-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="3b563-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b563-112">PARAMETERS</span></span>

### <span data-ttu-id="3b563-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3b563-113">-ApiId</span></span>
<span data-ttu-id="3b563-114">API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3b563-114">Identifier of api.</span></span> <span data-ttu-id="3b563-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3b563-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3b563-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3b563-116">-Context</span></span>
<span data-ttu-id="3b563-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="3b563-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b563-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3b563-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3b563-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b563-119">-DefaultProfile</span></span>
<span data-ttu-id="3b563-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b563-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b563-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="3b563-121">-SchemaDocument</span></span>
<span data-ttu-id="3b563-122">API-séma dokumentuma karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="3b563-122">Api schema document as a string.</span></span> <span data-ttu-id="3b563-123">Erre a paraméterre nincs szükség: a-SchemaDocumentFile nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="3b563-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="3b563-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="3b563-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="3b563-125">Az API-séma ContentType</span><span class="sxs-lookup"><span data-stu-id="3b563-125">ContentType of the api Schema.</span></span> <span data-ttu-id="3b563-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="3b563-126">This parameter is required.</span></span>

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

### <span data-ttu-id="3b563-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="3b563-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="3b563-128">Az API-séma szövegfájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3b563-128">Api schema document file path.</span></span> <span data-ttu-id="3b563-129">Erre a paraméterre nincs szükség: a-SchemaDocument nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="3b563-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="3b563-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="3b563-130">-SchemaId</span></span>
<span data-ttu-id="3b563-131">Az új séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3b563-131">Identifier of new schema.</span></span>
<span data-ttu-id="3b563-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3b563-132">This parameter is optional.</span></span>
<span data-ttu-id="3b563-133">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="3b563-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="3b563-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b563-134">-Confirm</span></span>
<span data-ttu-id="3b563-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b563-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b563-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b563-136">-WhatIf</span></span>
<span data-ttu-id="3b563-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b563-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b563-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b563-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b563-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b563-139">CommonParameters</span></span>
<span data-ttu-id="3b563-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b563-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b563-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b563-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b563-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b563-142">INPUTS</span></span>

### <span data-ttu-id="3b563-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b563-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b563-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3b563-144">System.String</span></span>

## <span data-ttu-id="3b563-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b563-145">OUTPUTS</span></span>

### <span data-ttu-id="3b563-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b563-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="3b563-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b563-147">NOTES</span></span>

## <span data-ttu-id="3b563-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b563-148">RELATED LINKS</span></span>

[<span data-ttu-id="3b563-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b563-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="3b563-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b563-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="3b563-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b563-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)