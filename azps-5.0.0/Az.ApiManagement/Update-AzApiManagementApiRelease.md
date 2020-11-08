---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187856"
---
# <span data-ttu-id="ad9f4-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad9f4-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="ad9f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9f4-103">Egy adott API-kiadás frissítése</span><span class="sxs-lookup"><span data-stu-id="ad9f4-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="ad9f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad9f4-104">SYNTAX</span></span>

### <span data-ttu-id="ad9f4-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad9f4-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad9f4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad9f4-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad9f4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad9f4-107">DESCRIPTION</span></span>
<span data-ttu-id="ad9f4-108">Az **Update-AzApiManagementApiRelease** parancsmag egy Azure API-kezelési API-kiadást módosít.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="ad9f4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ad9f4-109">EXAMPLES</span></span>

### <span data-ttu-id="ad9f4-110">1. példa: az API-kiadás API-kiadásának frissítése</span><span class="sxs-lookup"><span data-stu-id="ad9f4-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="ad9f4-111">A parancs az `echo-api-release` új megjegyzéssel frissíti az API API-kiadását `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="ad9f4-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="ad9f4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad9f4-112">PARAMETERS</span></span>

### <span data-ttu-id="ad9f4-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ad9f4-113">-ApiId</span></span>
<span data-ttu-id="ad9f4-114">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-114">Identifier of existing API.</span></span>
<span data-ttu-id="ad9f4-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ad9f4-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ad9f4-116">-Context</span></span>
<span data-ttu-id="ad9f4-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad9f4-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ad9f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9f4-119">-DefaultProfile</span></span>
<span data-ttu-id="ad9f4-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad9f4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad9f4-121">-InputObject</span></span>
<span data-ttu-id="ad9f4-122">Példa: Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9f4-123">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="ad9f4-123">-Note</span></span>
<span data-ttu-id="ad9f4-124">API-kibocsátási megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-124">Api Release Notes.</span></span>
<span data-ttu-id="ad9f4-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad9f4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad9f4-126">-PassThru</span></span>
<span data-ttu-id="ad9f4-127">Ha a Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease típust adja meg, amely a set API-kiadást adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9f4-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="ad9f4-128">-ReleaseId</span></span>
<span data-ttu-id="ad9f4-129">Az API-felülvizsgálati ReleaseId azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="ad9f4-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-130">This parameter is required.</span></span>

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

### <span data-ttu-id="ad9f4-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad9f4-131">-Confirm</span></span>
<span data-ttu-id="ad9f4-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad9f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9f4-133">-WhatIf</span></span>
<span data-ttu-id="ad9f4-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad9f4-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad9f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9f4-136">CommonParameters</span></span>
<span data-ttu-id="ad9f4-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad9f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9f4-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad9f4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9f4-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad9f4-139">INPUTS</span></span>

### <span data-ttu-id="ad9f4-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad9f4-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad9f4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9f4-141">System.String</span></span>

### <span data-ttu-id="ad9f4-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad9f4-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ad9f4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad9f4-143">OUTPUTS</span></span>

### <span data-ttu-id="ad9f4-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad9f4-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ad9f4-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad9f4-145">NOTES</span></span>

## <span data-ttu-id="ad9f4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad9f4-146">RELATED LINKS</span></span>

[<span data-ttu-id="ad9f4-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad9f4-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="ad9f4-148">Új – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad9f4-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)