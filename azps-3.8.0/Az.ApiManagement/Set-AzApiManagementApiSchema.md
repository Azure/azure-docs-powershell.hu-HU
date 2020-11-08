---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 23881baf47536db4fa694cf2165b8550b7f8cd62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013863"
---
# <span data-ttu-id="07a97-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="07a97-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="07a97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07a97-102">SYNOPSIS</span></span>
<span data-ttu-id="07a97-103">API-séma módosítása</span><span class="sxs-lookup"><span data-stu-id="07a97-103">Modifies an API Schema</span></span>

## <span data-ttu-id="07a97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07a97-104">SYNTAX</span></span>

### <span data-ttu-id="07a97-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07a97-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a97-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07a97-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a97-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07a97-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a97-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="07a97-108">DESCRIPTION</span></span>
<span data-ttu-id="07a97-109">A **set-AzApiManagementApiSchema** parancsmag egy Azure API-kezelési API-sémát módosít.</span><span class="sxs-lookup"><span data-stu-id="07a97-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="07a97-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07a97-110">EXAMPLES</span></span>

### <span data-ttu-id="07a97-111">Példa 1: API-séma módosítása</span><span class="sxs-lookup"><span data-stu-id="07a97-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="07a97-112">A példa frissíti az API-sémát</span><span class="sxs-lookup"><span data-stu-id="07a97-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="07a97-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07a97-113">PARAMETERS</span></span>

### <span data-ttu-id="07a97-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="07a97-114">-ApiId</span></span>
<span data-ttu-id="07a97-115">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="07a97-115">Identifier of existing API.</span></span>
<span data-ttu-id="07a97-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="07a97-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="07a97-117">-Context</span></span>
<span data-ttu-id="07a97-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="07a97-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="07a97-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="07a97-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a97-120">-DefaultProfile</span></span>
<span data-ttu-id="07a97-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07a97-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a97-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07a97-122">-InputObject</span></span>
<span data-ttu-id="07a97-123">A PsApiManagementApiSchema példánya.</span><span class="sxs-lookup"><span data-stu-id="07a97-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="07a97-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="07a97-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07a97-125">-PassThru</span></span>
<span data-ttu-id="07a97-126">Ha meg van adva, akkor a Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementApi típusa a set API-t jelképezi.</span><span class="sxs-lookup"><span data-stu-id="07a97-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="07a97-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a97-127">-ResourceId</span></span>
<span data-ttu-id="07a97-128">Az ARM ResourceId diagnosztikai vagy API-sémája van.</span><span class="sxs-lookup"><span data-stu-id="07a97-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="07a97-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="07a97-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="07a97-130">-SchemaDocument</span></span>
<span data-ttu-id="07a97-131">API-séma dokumentuma karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="07a97-131">Api schema document as a string.</span></span> <span data-ttu-id="07a97-132">Erre a paraméterre nincs szükség: a-SchemaDocumentFile nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="07a97-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="07a97-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="07a97-134">Az API-séma ContentType</span><span class="sxs-lookup"><span data-stu-id="07a97-134">ContentType of the api Schema.</span></span> <span data-ttu-id="07a97-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="07a97-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="07a97-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="07a97-137">Az API-séma szövegfájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="07a97-137">Api schema document file path.</span></span> <span data-ttu-id="07a97-138">Erre a paraméterre nincs szükség: a-SchemaDocument nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="07a97-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="07a97-139">-SchemaId</span></span>
<span data-ttu-id="07a97-140">A meglévő séma azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07a97-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="07a97-141">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="07a97-141">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a97-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07a97-142">-Confirm</span></span>
<span data-ttu-id="07a97-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07a97-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a97-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a97-144">-WhatIf</span></span>
<span data-ttu-id="07a97-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07a97-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07a97-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07a97-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a97-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a97-147">CommonParameters</span></span>
<span data-ttu-id="07a97-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07a97-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a97-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07a97-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a97-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a97-150">INPUTS</span></span>

### <span data-ttu-id="07a97-151">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="07a97-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07a97-152">System. String</span><span class="sxs-lookup"><span data-stu-id="07a97-152">System.String</span></span>

### <span data-ttu-id="07a97-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="07a97-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="07a97-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="07a97-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="07a97-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a97-155">OUTPUTS</span></span>

### <span data-ttu-id="07a97-156">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07a97-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="07a97-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07a97-157">NOTES</span></span>

## <span data-ttu-id="07a97-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07a97-158">RELATED LINKS</span></span>

[<span data-ttu-id="07a97-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="07a97-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="07a97-160">Új – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="07a97-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="07a97-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="07a97-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

